# nexconn-sdk-node

OpenAPI specification aligned with the current Nexconn public documentation, PDF source documents, and generated SDK requirements.

- API version: 0.1.0
- Package version: 0.1.0
- Generator version: 7.14.0

## Requirements

- Node.js 14+
- TypeScript 4.7+

## Installation

```sh
npm install "git+https://gitlab2.rongcloud.net/public-server/nexconn-server-sdk-node.git#dev"
```

If you publish releases later, prefer installing a tagged version instead of tracking a branch.

Then import the package:

```typescript
import { Configuration, UserManagementApi } from 'nexconn-sdk-node';
```

## Quick Start

The example below uses the SDK's built-in signing support to inject `App-Key / Nonce / Timestamp / Signature / X-Request-ID` automatically.

```typescript
import { Configuration, UserManagementApi, AccessTokenIssueRequest, ApiException } from 'nexconn-sdk-node';

const configuration = new Configuration();
configuration.setNexconnCredentials(
    'YOUR_APP_KEY',
    'YOUR_APP_SECRET',
);

// Optional: override the default nonce generator.
// configuration.setNonceGenerator(() => 'custom-nonce');

// Required: configure primary/backup domains before sending requests.
configuration.setPrimaryBackupDomains(
    process.env.NEXCONN_PRIMARY_API_DOMAIN!,
    process.env.NEXCONN_SECONDARY_API_DOMAIN!,
);
// configuration.setErrorSwitchingThreshold(1);
// configuration.setAutoFailoverEnabled(true);

const userManagementApi = new UserManagementApi(configuration);

const request: AccessTokenIssueRequest = {
    userId: 'user_123',
    name: 'Alice',
    avatarUrl: 'https://example.com/avatar.png',
};

try {
    const { data } = await userManagementApi.issueAccessToken(request);
    console.log(data);
} catch (e) {
    if (e instanceof ApiException) {
        console.error(`API error: ${e.errorCode} ${e.errorMessage}`);
    } else {
        throw e;
    }
}
```

## Error Handling

The SDK throws typed `ApiException` subclasses based on the HTTP status code. Each exception automatically parses the response body to expose the business `errorCode` and `errorMessage`.

```typescript
import {
    ApiException,
    BadRequestException,
    UnauthorizedException,
    ForbiddenException,
    NotFoundException,
    ConflictException,
    TooManyRequestsException,
    ServiceException,
} from 'nexconn-sdk-node';

try {
    const { data } = await groupApi.createGroup(request);
} catch (e) {
    if (e instanceof BadRequestException) {
        // HTTP 400 — invalid parameters
        console.error(`Bad request: ${e.errorCode} ${e.errorMessage}`);
    } else if (e instanceof UnauthorizedException) {
        // HTTP 401 — check your AppKey / AppSecret
    } else if (e instanceof ForbiddenException) {
        // HTTP 403 — permission denied
    } else if (e instanceof NotFoundException) {
        // HTTP 404 — resource not found
    } else if (e instanceof ConflictException) {
        // HTTP 409 — resource already exists
        console.error(`Conflict: errorCode=${e.errorCode}`);
    } else if (e instanceof TooManyRequestsException) {
        // HTTP 429 — rate limited, retry later
    } else if (e instanceof ServiceException) {
        // HTTP 5xx — server error, may retry
    } else if (e instanceof ApiException) {
        // Other HTTP errors
        console.error(`HTTP ${e.httpStatus}: ${e.responseBody}`);
    } else {
        console.error(e);
    }
}
```

All exception subclasses provide the following properties:

| Property | Description |
|----------|-------------|
| `httpStatus` | HTTP status code |
| `errorCode` | Business error code from response body `code` field (`-1` if unparseable) |
| `errorMessage` | Business error message from response body `errorMessage` field |
| `responseBody` | Raw response body string |
| `responseHeaders` | Response headers |

## Features

- Automatic Nexconn request signing when `setNexconnCredentials()` is configured
- Built-in multi-domain failover support via `setPrimaryBackupDomains()`
- Default `User-Agent`: `nexconn-sdk-node/0.1.0`
- Automatic `X-Request-ID` generation

## Configuration of Server URL

The SDK does not embed any default API domain. You must call `setPrimaryBackupDomains()` before sending requests.

## Documentation for API Endpoints

All requests use the primary/backup domains configured by the caller.

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ChannelManagementApi* | [**addTagToChannels**](docs/ChannelManagementApi.md#addtagtochannels) | **POST** /v4/channel/tag/add | Add tag to channel
*ChannelManagementApi* | [**addUserChannelTags**](docs/ChannelManagementApi.md#adduserchanneltags) | **POST** /v4/user/channel/tag/add | Add user channel tag
*ChannelManagementApi* | [**getChannelAttribute**](docs/ChannelManagementApi.md#getchannelattribute) | **POST** /v4/channel/attribute/get | Get channel attributes
*ChannelManagementApi* | [**getChannelPushNotification**](docs/ChannelManagementApi.md#getchannelpushnotification) | **POST** /v4/channel/push/get | Get channel DND
*ChannelManagementApi* | [**getChannelTypeNotification**](docs/ChannelManagementApi.md#getchanneltypenotification) | **POST** /v4/channel-type/push/get | Get DND by channel type
*ChannelManagementApi* | [**listChannelsByTag**](docs/ChannelManagementApi.md#listchannelsbytag) | **POST** /v4/channel/tag/list | Get channels by tag
*ChannelManagementApi* | [**listUserChannelTags**](docs/ChannelManagementApi.md#listuserchanneltags) | **POST** /v4/user/channel/tag/list | List user channel tags
*ChannelManagementApi* | [**removeTagFromChannels**](docs/ChannelManagementApi.md#removetagfromchannels) | **POST** /v4/channel/tag/delete | Remove tag from channel
*ChannelManagementApi* | [**removeUserChannelTags**](docs/ChannelManagementApi.md#removeuserchanneltags) | **POST** /v4/user/channel/tag/remove | Remove user channel tag
*ChannelManagementApi* | [**setChannelPin**](docs/ChannelManagementApi.md#setchannelpin) | **POST** /v4/channel/pin/set | Pin a channel
*ChannelManagementApi* | [**setChannelPushNotification**](docs/ChannelManagementApi.md#setchannelpushnotification) | **POST** /v4/channel/push/set | Set channel DND
*ChannelManagementApi* | [**setChannelTypeNotification**](docs/ChannelManagementApi.md#setchanneltypenotification) | **POST** /v4/channel-type/push/set | Set DND by channel type
*CommunityChannelManagementApi* | [**addCommunityChannelUserGroupUsers**](docs/CommunityChannelManagementApi.md#addcommunitychannelusergroupusers) | **POST** /v4/community-channel/user-group/user/add | Add community channel user group users
*CommunityChannelManagementApi* | [**addCommunityChannelUserGroups**](docs/CommunityChannelManagementApi.md#addcommunitychannelusergroups) | **POST** /v4/community-channel/user-group/add | Add community channel user groups
*CommunityChannelManagementApi* | [**addPrivateSubchannelMembers**](docs/CommunityChannelManagementApi.md#addprivatesubchannelmembers) | **POST** /v4/community-channel/private-subchannel/member/add | Add private subchannel members
*CommunityChannelManagementApi* | [**bindCommunityChannelUserGroup**](docs/CommunityChannelManagementApi.md#bindcommunitychannelusergroup) | **POST** /v4/community-channel/channel/user-group/bind | Bind community channel user group
*CommunityChannelManagementApi* | [**checkCommunityChannelMemberExist**](docs/CommunityChannelManagementApi.md#checkcommunitychannelmemberexist) | **POST** /v4/community-channel/member/exist | Check community channel member exist
*CommunityChannelManagementApi* | [**createCommunityChannel**](docs/CommunityChannelManagementApi.md#createcommunitychannel) | **POST** /v4/community-channel/create | Create community channel
*CommunityChannelManagementApi* | [**createCommunitySubchannel**](docs/CommunityChannelManagementApi.md#createcommunitysubchannel) | **POST** /v4/community-channel/subchannel/create | Create community subchannel
*CommunityChannelManagementApi* | [**deleteCommunitySubchannel**](docs/CommunityChannelManagementApi.md#deletecommunitysubchannel) | **POST** /v4/community-channel/subchannel/delete | Delete community subchannel
*CommunityChannelManagementApi* | [**dismissCommunityChannel**](docs/CommunityChannelManagementApi.md#dismisscommunitychannel) | **POST** /v4/community-channel/dismiss | Dismiss community channel
*CommunityChannelManagementApi* | [**joinCommunityChannel**](docs/CommunityChannelManagementApi.md#joincommunitychannel) | **POST** /v4/community-channel/join | Join community channel
*CommunityChannelManagementApi* | [**listCommunityChannelHistoryMessages**](docs/CommunityChannelManagementApi.md#listcommunitychannelhistorymessages) | **POST** /v4/community-channel/history-message/list | List community-channel history messages
*CommunityChannelManagementApi* | [**listCommunityChannelSubchannelUserGroups**](docs/CommunityChannelManagementApi.md#listcommunitychannelsubchannelusergroups) | **POST** /v4/community-channel/channel/user-group/list | List community channel subchannel user groups
*CommunityChannelManagementApi* | [**listCommunityChannelUserGroupSubchannels**](docs/CommunityChannelManagementApi.md#listcommunitychannelusergroupsubchannels) | **POST** /v4/community-channel/user-group/subchannel/list | List community channel user group subchannels
*CommunityChannelManagementApi* | [**listCommunityChannelUserGroups**](docs/CommunityChannelManagementApi.md#listcommunitychannelusergroups) | **POST** /v4/community-channel/user-group/list | List community channel user groups
*CommunityChannelManagementApi* | [**listCommunityChannelUserUserGroups**](docs/CommunityChannelManagementApi.md#listcommunitychanneluserusergroups) | **POST** /v4/community-channel/user/user-group/list | List community channel user user groups
*CommunityChannelManagementApi* | [**listCommunitySubchannels**](docs/CommunityChannelManagementApi.md#listcommunitysubchannels) | **POST** /v4/community-channel/subchannel/list | List community subchannels
*CommunityChannelManagementApi* | [**listCommunityUserSubchannels**](docs/CommunityChannelManagementApi.md#listcommunityusersubchannels) | **POST** /v4/community-channel/user/subchannel/list | List community user subchannels
*CommunityChannelManagementApi* | [**listPrivateSubchannelMembers**](docs/CommunityChannelManagementApi.md#listprivatesubchannelmembers) | **POST** /v4/community-channel/private-subchannel/member/list | List private subchannel members
*CommunityChannelManagementApi* | [**quitCommunityChannel**](docs/CommunityChannelManagementApi.md#quitcommunitychannel) | **POST** /v4/community-channel/leave | Leave community channel
*CommunityChannelManagementApi* | [**removeCommunityChannelUserGroupUsers**](docs/CommunityChannelManagementApi.md#removecommunitychannelusergroupusers) | **POST** /v4/community-channel/user-group/user/remove | Remove community channel user group users
*CommunityChannelManagementApi* | [**removeCommunityChannelUserGroups**](docs/CommunityChannelManagementApi.md#removecommunitychannelusergroups) | **POST** /v4/community-channel/user-group/remove | Delete community channel user groups
*CommunityChannelManagementApi* | [**removePrivateSubchannelMembers**](docs/CommunityChannelManagementApi.md#removeprivatesubchannelmembers) | **POST** /v4/community-channel/private-subchannel/member/remove | Remove private subchannel members
*CommunityChannelManagementApi* | [**unbindCommunityChannelUserGroup**](docs/CommunityChannelManagementApi.md#unbindcommunitychannelusergroup) | **POST** /v4/community-channel/channel/user-group/unbind | Unbind community channel user group
*CommunityChannelManagementApi* | [**updateCommunityChannelInfo**](docs/CommunityChannelManagementApi.md#updatecommunitychannelinfo) | **POST** /v4/community-channel/update | Update community channel info
*CommunityChannelManagementApi* | [**updateCommunitySubchannelType**](docs/CommunityChannelManagementApi.md#updatecommunitysubchanneltype) | **POST** /v4/community-channel/subchannel-type/update | Update community subchannel type
*CommunityChannelModerationApi* | [**addCommunityChannelAllowedSenderList**](docs/CommunityChannelModerationApi.md#addcommunitychannelallowedsenderlist) | **POST** /v4/community-channel/allowed-sender-list/add | Add community channel allowed sender list
*CommunityChannelModerationApi* | [**addCommunityChannelMutedUsers**](docs/CommunityChannelModerationApi.md#addcommunitychannelmutedusers) | **POST** /v4/community-channel/mute-list/add | Add community-channel muted users
*CommunityChannelModerationApi* | [**getCommunityChannelFreezeList**](docs/CommunityChannelModerationApi.md#getcommunitychannelfreezelist) | **POST** /v4/community-channel/freeze-list/get | Get community channel freeze status
*CommunityChannelModerationApi* | [**listCommunityChannelAllowedSenderList**](docs/CommunityChannelModerationApi.md#listcommunitychannelallowedsenderlist) | **POST** /v4/community-channel/allowed-sender-list/get | List community channel allowed sender list
*CommunityChannelModerationApi* | [**listCommunityChannelMutedUsers**](docs/CommunityChannelModerationApi.md#listcommunitychannelmutedusers) | **POST** /v4/community-channel/mute-list/get | List community-channel muted users
*CommunityChannelModerationApi* | [**removeCommunityChannelAllowedSenderList**](docs/CommunityChannelModerationApi.md#removecommunitychannelallowedsenderlist) | **POST** /v4/community-channel/allowed-sender-list/remove | Remove community channel allowed sender list
*CommunityChannelModerationApi* | [**removeCommunityChannelMutedUsers**](docs/CommunityChannelModerationApi.md#removecommunitychannelmutedusers) | **POST** /v4/community-channel/mute-list/remove | Remove community-channel muted users
*CommunityChannelModerationApi* | [**setCommunityChannelFreezeList**](docs/CommunityChannelModerationApi.md#setcommunitychannelfreezelist) | **POST** /v4/community-channel/freeze-list/set | Set community channel freeze list
*FriendshipApi* | [**addFriend**](docs/FriendshipApi.md#addfriend) | **POST** /v4/friend/add | Add friend
*FriendshipApi* | [**getFriendPermission**](docs/FriendshipApi.md#getfriendpermission) | **POST** /v4/friend/permission/get | Get friend permission
*FriendshipApi* | [**getFriendRelationships**](docs/FriendshipApi.md#getfriendrelationships) | **POST** /v4/friend/relationship/get | Get friend relationships
*FriendshipApi* | [**listFriends**](docs/FriendshipApi.md#listfriends) | **POST** /v4/friend/list | List friends
*FriendshipApi* | [**removeAllFriends**](docs/FriendshipApi.md#removeallfriends) | **POST** /v4/friend/remove-all | Clean all friends
*FriendshipApi* | [**removeFriends**](docs/FriendshipApi.md#removefriends) | **POST** /v4/friend/remove | Delete friends
*FriendshipApi* | [**setFriendPermission**](docs/FriendshipApi.md#setfriendpermission) | **POST** /v4/friend/permission/set | Set friend permission
*FriendshipApi* | [**setFriendProfile**](docs/FriendshipApi.md#setfriendprofile) | **POST** /v4/friend/profile/set | Set friend profile
*GroupChannelManagementApi* | [**addGroupChannelAdmins**](docs/GroupChannelManagementApi.md#addgroupchanneladmins) | **POST** /v4/group-channel/admin/add | Add group admins
*GroupChannelManagementApi* | [**addGroupChannelMemberFavorites**](docs/GroupChannelManagementApi.md#addgroupchannelmemberfavorites) | **POST** /v4/group-channel/member/favorites/add | Add favorite group members
*GroupChannelManagementApi* | [**batchGetGroupChannelMembers**](docs/GroupChannelManagementApi.md#batchgetgroupchannelmembers) | **POST** /v4/group-channel/member/batch/get | Get specific group members
*GroupChannelManagementApi* | [**batchGetGroupChannelProfiles**](docs/GroupChannelManagementApi.md#batchgetgroupchannelprofiles) | **POST** /v4/group-channel/profile/list | List group profiles
*GroupChannelManagementApi* | [**createGroupChannel**](docs/GroupChannelManagementApi.md#creategroupchannel) | **POST** /v4/group-channel/create | Create a group
*GroupChannelManagementApi* | [**deleteGroupChannelAlias**](docs/GroupChannelManagementApi.md#deletegroupchannelalias) | **POST** /v4/group-channel/alias/delete | Delete group alias
*GroupChannelManagementApi* | [**dismissGroupChannel**](docs/GroupChannelManagementApi.md#dismissgroupchannel) | **POST** /v4/group-channel/dismiss | Dismiss a group
*GroupChannelManagementApi* | [**getGroupChannelAlias**](docs/GroupChannelManagementApi.md#getgroupchannelalias) | **POST** /v4/group-channel/alias/get | Get group alias
*GroupChannelManagementApi* | [**joinGroupChannel**](docs/GroupChannelManagementApi.md#joingroupchannel) | **POST** /v4/group-channel/join | Join a group
*GroupChannelManagementApi* | [**kickUserFromAllGroupChannels**](docs/GroupChannelManagementApi.md#kickuserfromallgroupchannels) | **POST** /v4/group-channel/member/kickout-all | Remove a user from all groups
*GroupChannelManagementApi* | [**listGroupChannelMemberFavorites**](docs/GroupChannelManagementApi.md#listgroupchannelmemberfavorites) | **POST** /v4/group-channel/member/favorites/list | List favorite group members
*GroupChannelManagementApi* | [**listGroupChannelMembers**](docs/GroupChannelManagementApi.md#listgroupchannelmembers) | **POST** /v4/group-channel/member/list | Query group members
*GroupChannelManagementApi* | [**listGroupChannels**](docs/GroupChannelManagementApi.md#listgroupchannels) | **POST** /v4/group-channel/list | List group channels
*GroupChannelManagementApi* | [**listUserJoinedGroupChannels**](docs/GroupChannelManagementApi.md#listuserjoinedgroupchannels) | **POST** /v4/group-channel/joined/list | Query user\&#39;s groups
*GroupChannelManagementApi* | [**quitGroupChannel**](docs/GroupChannelManagementApi.md#quitgroupchannel) | **POST** /v4/group-channel/leave | Leave a group
*GroupChannelManagementApi* | [**removeGroupChannelAdmins**](docs/GroupChannelManagementApi.md#removegroupchanneladmins) | **POST** /v4/group-channel/admin/remove | Remove group admins
*GroupChannelManagementApi* | [**removeGroupChannelMemberFavorites**](docs/GroupChannelManagementApi.md#removegroupchannelmemberfavorites) | **POST** /v4/group-channel/member/favorites/remove | Remove favorite group members
*GroupChannelManagementApi* | [**setGroupChannelAlias**](docs/GroupChannelManagementApi.md#setgroupchannelalias) | **POST** /v4/group-channel/alias/set | Set group alias
*GroupChannelManagementApi* | [**setGroupChannelMember**](docs/GroupChannelManagementApi.md#setgroupchannelmember) | **POST** /v4/group-channel/member/set | Set group member profile
*GroupChannelManagementApi* | [**transferGroupChannelOwner**](docs/GroupChannelManagementApi.md#transfergroupchannelowner) | **POST** /v4/group-channel/transfer/owner | Transfer group ownership
*GroupChannelManagementApi* | [**updateGroupChannelProfile**](docs/GroupChannelManagementApi.md#updategroupchannelprofile) | **POST** /v4/group-channel/profile/update | Update group info
*GroupChannelModerationApi* | [**addGroupChannelAllowedSenderList**](docs/GroupChannelModerationApi.md#addgroupchannelallowedsenderlist) | **POST** /v4/group-channel/allowed-sender-list/add | Add to allowed senders list
*GroupChannelModerationApi* | [**addGroupChannelFreezeList**](docs/GroupChannelModerationApi.md#addgroupchannelfreezelist) | **POST** /v4/group-channel/freeze-list/add | Freeze a group
*GroupChannelModerationApi* | [**addGroupChannelUserMuteList**](docs/GroupChannelModerationApi.md#addgroupchannelusermutelist) | **POST** /v4/group-channel/user/mute-list/add | Mute a group member
*GroupChannelModerationApi* | [**getGroupChannelAllowedSenderList**](docs/GroupChannelModerationApi.md#getgroupchannelallowedsenderlist) | **POST** /v4/group-channel/allowed-sender-list/get | Query allowed senders list
*GroupChannelModerationApi* | [**getGroupChannelFreezeList**](docs/GroupChannelModerationApi.md#getgroupchannelfreezelist) | **POST** /v4/group-channel/freeze-list/get | Query group freeze status
*GroupChannelModerationApi* | [**getGroupChannelUserMuteList**](docs/GroupChannelModerationApi.md#getgroupchannelusermutelist) | **POST** /v4/group-channel/user/mute-list/get | List muted group members
*GroupChannelModerationApi* | [**removeGroupChannelAllowedSenderList**](docs/GroupChannelModerationApi.md#removegroupchannelallowedsenderlist) | **POST** /v4/group-channel/allowed-sender-list/remove | Remove from allowed senders list
*GroupChannelModerationApi* | [**removeGroupChannelFreezeList**](docs/GroupChannelModerationApi.md#removegroupchannelfreezelist) | **POST** /v4/group-channel/freeze-list/remove | Unfreeze a group
*GroupChannelModerationApi* | [**removeGroupChannelUserMuteList**](docs/GroupChannelModerationApi.md#removegroupchannelusermutelist) | **POST** /v4/group-channel/user/mute-list/remove | Unmute a group member
*MessageManagementApi* | [**broadcastOpenChannelMessage**](docs/MessageManagementApi.md#broadcastopenchannelmessage) | **POST** /v4/open-channel/message/broadcast | Broadcast to all open channels
*MessageManagementApi* | [**deleteChannelMessageHistory**](docs/MessageManagementApi.md#deletechannelmessagehistory) | **POST** /v4/channel/message/history/delete | Delete server-side channel message history
*MessageManagementApi* | [**deleteChannelTypeMessageMetadata**](docs/MessageManagementApi.md#deletechanneltypemessagemetadata) | **POST** /v4/channel-type/message/metadata/delete | Delete message metadata
*MessageManagementApi* | [**deleteCommunityChannelMessageMetadata**](docs/MessageManagementApi.md#deletecommunitychannelmessagemetadata) | **POST** /v4/community-channel/message/metadata/delete | Delete community-channel message metadata keys
*MessageManagementApi* | [**deleteMessage**](docs/MessageManagementApi.md#deletemessage) | **POST** /v4/message/delete | Delete a message (recall)
*MessageManagementApi* | [**listChannelTypeMessageMetadata**](docs/MessageManagementApi.md#listchanneltypemessagemetadata) | **POST** /v4/channel-type/message/metadata/list | Get message metadata
*MessageManagementApi* | [**listCommunityChannelMessageMetadata**](docs/MessageManagementApi.md#listcommunitychannelmessagemetadata) | **POST** /v4/community-channel/message/metadata/list | List community-channel message metadata
*MessageManagementApi* | [**sendCommunityChannelMessage**](docs/MessageManagementApi.md#sendcommunitychannelmessage) | **POST** /v4/community-channel/message/send | Send a community channel message
*MessageManagementApi* | [**sendDirectChannelMessage**](docs/MessageManagementApi.md#senddirectchannelmessage) | **POST** /v4/direct-channel/message/send | Send a direct message
*MessageManagementApi* | [**sendGroupChannelMessage**](docs/MessageManagementApi.md#sendgroupchannelmessage) | **POST** /v4/group-channel/message/send | Send a group message
*MessageManagementApi* | [**sendOpenChannelMessage**](docs/MessageManagementApi.md#sendopenchannelmessage) | **POST** /v4/open-channel/message/send | Send an open channel message
*MessageManagementApi* | [**setChannelTypeMessageMetadata**](docs/MessageManagementApi.md#setchanneltypemessagemetadata) | **POST** /v4/channel-type/message/metadata/set | Set message metadata
*MessageManagementApi* | [**setCommunityChannelMessageMetadata**](docs/MessageManagementApi.md#setcommunitychannelmessagemetadata) | **POST** /v4/community-channel/message/metadata/set | Set community-channel message metadata
*MessageManagementApi* | [**updateCommunityChannelMessage**](docs/MessageManagementApi.md#updatecommunitychannelmessage) | **POST** /v4/community-channel/message/update | Update community-channel message
*MessageManagementApi* | [**updateDirectChannelMessage**](docs/MessageManagementApi.md#updatedirectchannelmessage) | **POST** /v4/direct-channel/message/update | Update direct-channel message
*MessageManagementApi* | [**updateGroupChannelMessage**](docs/MessageManagementApi.md#updategroupchannelmessage) | **POST** /v4/group-channel/message/update | Update group-channel message
*ModerationApi* | [**batchAddProfanityWords**](docs/ModerationApi.md#batchaddprofanitywords) | **POST** /v4/profanity-word/batch/add | Batch add profanity words
*ModerationApi* | [**batchRemoveProfanityWords**](docs/ModerationApi.md#batchremoveprofanitywords) | **POST** /v4/profanity-word/batch/remove | Batch delete profanity words
*ModerationApi* | [**listProfanityWords**](docs/ModerationApi.md#listprofanitywords) | **POST** /v4/profanity-word/list | List profanity words
*ModerationApi* | [**removeProfanityWord**](docs/ModerationApi.md#removeprofanityword) | **POST** /v4/profanity-word/remove | Delete profanity word
*OpenChannelManagementApi* | [**createOpenChannel**](docs/OpenChannelManagementApi.md#createopenchannel) | **POST** /v4/open-channel/create | Create an open channel
*OpenChannelManagementApi* | [**destroyOpenChannels**](docs/OpenChannelManagementApi.md#destroyopenchannels) | **POST** /v4/open-channel/destroy | Destroy an open channel
*OpenChannelManagementApi* | [**getOpenChannel**](docs/OpenChannelManagementApi.md#getopenchannel) | **POST** /v4/open-channel/get | Get open channel info
*OpenChannelManagementApi* | [**setOpenChannelDestroyType**](docs/OpenChannelManagementApi.md#setopenchanneldestroytype) | **POST** /v4/open-channel/destroy-type/set | Set auto-destroy type
*OpenChannelMessagePriorityApi* | [**addOpenChannelLowPriorityMessageTypeList**](docs/OpenChannelMessagePriorityApi.md#addopenchannellowprioritymessagetypelist) | **POST** /v4/open-channel/low-priority-message-type-list/add | Add low-priority message types
*OpenChannelMessagePriorityApi* | [**getOpenChannelLowPriorityMessageTypeList**](docs/OpenChannelMessagePriorityApi.md#getopenchannellowprioritymessagetypelist) | **POST** /v4/open-channel/low-priority-message-type-list/get | Query low-priority message types
*OpenChannelMessagePriorityApi* | [**removeOpenChannelLowPriorityMessageTypeList**](docs/OpenChannelMessagePriorityApi.md#removeopenchannellowprioritymessagetypelist) | **POST** /v4/open-channel/low-priority-message-type-list/remove | Remove low-priority message types
*OpenChannelMetadataApi* | [**batchGetOpenChannelMetadata**](docs/OpenChannelMetadataApi.md#batchgetopenchannelmetadata) | **POST** /v4/open-channel/metadata/batch/get | Query metadata
*OpenChannelMetadataApi* | [**batchRemoveOpenChannelMetadata**](docs/OpenChannelMetadataApi.md#batchremoveopenchannelmetadata) | **POST** /v4/open-channel/metadata/batch/remove | Batch delete metadata
*OpenChannelMetadataApi* | [**batchSetOpenChannelMetadata**](docs/OpenChannelMetadataApi.md#batchsetopenchannelmetadata) | **POST** /v4/open-channel/metadata/batch/set | Batch set metadata
*OpenChannelParticipantsModerationApi* | [**addOpenChannelFreezeList**](docs/OpenChannelParticipantsModerationApi.md#addopenchannelfreezelist) | **POST** /v4/open-channel/freeze-list/add | Freeze an open channel
*OpenChannelParticipantsModerationApi* | [**addOpenChannelGlobalMuteList**](docs/OpenChannelParticipantsModerationApi.md#addopenchannelglobalmutelist) | **POST** /v4/open-channel/global-mute-list/add | Mute a user globally
*OpenChannelParticipantsModerationApi* | [**addOpenChannelParticipantAllowedSenderList**](docs/OpenChannelParticipantsModerationApi.md#addopenchannelparticipantallowedsenderlist) | **POST** /v4/open-channel/participant/allowed-sender-list/add | Add to allowed senders list
*OpenChannelParticipantsModerationApi* | [**addOpenChannelParticipantBanList**](docs/OpenChannelParticipantsModerationApi.md#addopenchannelparticipantbanlist) | **POST** /v4/open-channel/participant/ban-list/add | Ban a participant
*OpenChannelParticipantsModerationApi* | [**addOpenChannelParticipantMuteList**](docs/OpenChannelParticipantsModerationApi.md#addopenchannelparticipantmutelist) | **POST** /v4/open-channel/participant/mute-list/add | Mute a participant
*OpenChannelParticipantsModerationApi* | [**checkOpenChannelFreeze**](docs/OpenChannelParticipantsModerationApi.md#checkopenchannelfreeze) | **POST** /v4/open-channel/freeze/check | Check open channel freeze status
*OpenChannelParticipantsModerationApi* | [**checkOpenChannelParticipantsExist**](docs/OpenChannelParticipantsModerationApi.md#checkopenchannelparticipantsexist) | **POST** /v4/open-channel/participant/exist | Batch check participants
*OpenChannelParticipantsModerationApi* | [**getOpenChannelGlobalMuteList**](docs/OpenChannelParticipantsModerationApi.md#getopenchannelglobalmutelist) | **POST** /v4/open-channel/global-mute-list/get | List globally muted users
*OpenChannelParticipantsModerationApi* | [**getOpenChannelParticipantAllowedSenderList**](docs/OpenChannelParticipantsModerationApi.md#getopenchannelparticipantallowedsenderlist) | **POST** /v4/open-channel/participant/allowed-sender-list/get | Query allowed senders list
*OpenChannelParticipantsModerationApi* | [**getOpenChannelParticipantBanList**](docs/OpenChannelParticipantsModerationApi.md#getopenchannelparticipantbanlist) | **POST** /v4/open-channel/participant/ban-list/get | List banned participants
*OpenChannelParticipantsModerationApi* | [**getOpenChannelParticipantMuteList**](docs/OpenChannelParticipantsModerationApi.md#getopenchannelparticipantmutelist) | **POST** /v4/open-channel/participant/mute-list/get | List muted participants
*OpenChannelParticipantsModerationApi* | [**listFrozenOpenChannels**](docs/OpenChannelParticipantsModerationApi.md#listfrozenopenchannels) | **POST** /v4/open-channel/freeze-list/get | List frozen open channels
*OpenChannelParticipantsModerationApi* | [**listOpenChannelParticipants**](docs/OpenChannelParticipantsModerationApi.md#listopenchannelparticipants) | **POST** /v4/open-channel/participant/list | List participants
*OpenChannelParticipantsModerationApi* | [**removeOpenChannelFreezeList**](docs/OpenChannelParticipantsModerationApi.md#removeopenchannelfreezelist) | **POST** /v4/open-channel/freeze-list/remove | Unfreeze an open channel
*OpenChannelParticipantsModerationApi* | [**removeOpenChannelGlobalMuteList**](docs/OpenChannelParticipantsModerationApi.md#removeopenchannelglobalmutelist) | **POST** /v4/open-channel/global-mute-list/remove | Unmute a user globally
*OpenChannelParticipantsModerationApi* | [**removeOpenChannelParticipantAllowedSenderList**](docs/OpenChannelParticipantsModerationApi.md#removeopenchannelparticipantallowedsenderlist) | **POST** /v4/open-channel/participant/allowed-sender-list/remove | Remove from allowed senders list
*OpenChannelParticipantsModerationApi* | [**removeOpenChannelParticipantBanList**](docs/OpenChannelParticipantsModerationApi.md#removeopenchannelparticipantbanlist) | **POST** /v4/open-channel/participant/ban-list/remove | Unban a participant
*OpenChannelParticipantsModerationApi* | [**removeOpenChannelParticipantMuteList**](docs/OpenChannelParticipantsModerationApi.md#removeopenchannelparticipantmutelist) | **POST** /v4/open-channel/participant/mute-list/remove | Unmute a participant
*OpenChannelPriorityControlsApi* | [**addOpenChannelPriorityMessageTypeList**](docs/OpenChannelPriorityControlsApi.md#addopenchannelprioritymessagetypelist) | **POST** /v4/open-channel/priority-message-type-list/add | Add priority message types
*OpenChannelPriorityControlsApi* | [**addOpenChannelPrioritySenderList**](docs/OpenChannelPriorityControlsApi.md#addopenchannelprioritysenderlist) | **POST** /v4/open-channel/priority-sender-list/add | Add priority senders
*OpenChannelPriorityControlsApi* | [**getOpenChannelPriorityMessageTypeList**](docs/OpenChannelPriorityControlsApi.md#getopenchannelprioritymessagetypelist) | **POST** /v4/open-channel/priority-message-type-list/get | Query priority message types
*OpenChannelPriorityControlsApi* | [**getOpenChannelPrioritySenderList**](docs/OpenChannelPriorityControlsApi.md#getopenchannelprioritysenderlist) | **POST** /v4/open-channel/priority-sender-list/get | Query priority senders
*OpenChannelPriorityControlsApi* | [**removeOpenChannelPriorityMessageTypeList**](docs/OpenChannelPriorityControlsApi.md#removeopenchannelprioritymessagetypelist) | **POST** /v4/open-channel/priority-message-type-list/remove | Remove priority message types
*OpenChannelPriorityControlsApi* | [**removeOpenChannelPrioritySenderList**](docs/OpenChannelPriorityControlsApi.md#removeopenchannelprioritysenderlist) | **POST** /v4/open-channel/priority-sender-list/remove | Remove priority senders
*SystemMessagesApi* | [**broadcastMessageOnline**](docs/SystemMessagesApi.md#broadcastmessageonline) | **POST** /v4/system-channel/message/broadcast-online | Broadcast to online users
*SystemMessagesApi* | [**broadcastSystemChannelMessage**](docs/SystemMessagesApi.md#broadcastsystemchannelmessage) | **POST** /v4/system-channel/message/broadcast-all | Broadcast to all users (persistent)
*SystemMessagesApi* | [**deleteBroadcastMessage**](docs/SystemMessagesApi.md#deletebroadcastmessage) | **POST** /v4/system-channel/message/broadcast/delete | Recall broadcast to all users
*SystemMessagesApi* | [**sendSystemChannelMessage**](docs/SystemMessagesApi.md#sendsystemchannelmessage) | **POST** /v4/system-channel/message/send | Send a system message
*SystemMessagesApi* | [**sendSystemChannelPushByPackage**](docs/SystemMessagesApi.md#sendsystemchannelpushbypackage) | **POST** /v4/system-channel/app-package-users/send | Push by app package name
*SystemMessagesApi* | [**sendSystemChannelPushByTag**](docs/SystemMessagesApi.md#sendsystemchannelpushbytag) | **POST** /v4/system-channel/tagged-users/send | Push to tagged users
*UserBlocklistApi* | [**addUserBlocklist**](docs/UserBlocklistApi.md#adduserblocklist) | **POST** /v4/user/blocklist/add | Add to blocklist
*UserBlocklistApi* | [**getUserBlocklist**](docs/UserBlocklistApi.md#getuserblocklist) | **POST** /v4/user/blocklist/get | Get blocklist
*UserBlocklistApi* | [**removeUserBlocklist**](docs/UserBlocklistApi.md#removeuserblocklist) | **POST** /v4/user/blocklist/remove | Remove from blocklist
*UserManagementApi* | [**banUsers**](docs/UserManagementApi.md#banusers) | **POST** /v4/user/ban | Ban a user
*UserManagementApi* | [**batchGetUserTags**](docs/UserManagementApi.md#batchgetusertags) | **POST** /v4/user/tag/batch/get | Get user tags
*UserManagementApi* | [**batchSetUserTags**](docs/UserManagementApi.md#batchsetusertags) | **POST** /v4/user/tag/batch/set | Batch set user tags
*UserManagementApi* | [**expireAccessToken**](docs/UserManagementApi.md#expireaccesstoken) | **POST** /v4/auth/access-token/expire | Expire an access token
*UserManagementApi* | [**getUser**](docs/UserManagementApi.md#getuser) | **POST** /v4/user/get | Get user info
*UserManagementApi* | [**getUserConnectionStatus**](docs/UserManagementApi.md#getuserconnectionstatus) | **POST** /v4/user/connection-status/get | Check user online status
*UserManagementApi* | [**issueAccessToken**](docs/UserManagementApi.md#issueaccesstoken) | **POST** /v4/auth/access-token/issue | Register a user
*UserManagementApi* | [**listBannedUsers**](docs/UserManagementApi.md#listbannedusers) | **POST** /v4/user/ban/list | List banned users
*UserManagementApi* | [**listChannelTypeMute**](docs/UserManagementApi.md#listchanneltypemute) | **POST** /v4/channel-type/mute/list | List muted direct channel users
*UserManagementApi* | [**listSoftDeletedUsers**](docs/UserManagementApi.md#listsoftdeletedusers) | **POST** /v4/user/soft-deleted/list | Query soft-deleted users
*UserManagementApi* | [**restoreUsers**](docs/UserManagementApi.md#restoreusers) | **POST** /v4/user/restore | Restore a user
*UserManagementApi* | [**setChannelTypeMute**](docs/UserManagementApi.md#setchanneltypemute) | **POST** /v4/channel-type/mute/set | Mute a user in direct channels
*UserManagementApi* | [**softDeleteUsers**](docs/UserManagementApi.md#softdeleteusers) | **POST** /v4/user/soft-delete | Soft-delete a user
*UserManagementApi* | [**unbanUsers**](docs/UserManagementApi.md#unbanusers) | **POST** /v4/user/unban | Unban a user
*UserManagementApi* | [**updateUser**](docs/UserManagementApi.md#updateuser) | **POST** /v4/user/update | Update user info
*UserProfileHostingApi* | [**batchGetUserProfiles**](docs/UserProfileHostingApi.md#batchgetuserprofiles) | **POST** /v4/user/profile/batch/get | Batch get user profiles
*UserProfileHostingApi* | [**deleteUserProfiles**](docs/UserProfileHostingApi.md#deleteuserprofiles) | **POST** /v4/user/profile/delete | Clear user profiles
*UserProfileHostingApi* | [**listUserProfiles**](docs/UserProfileHostingApi.md#listuserprofiles) | **POST** /v4/user/profile/list | List user profiles
*UserProfileHostingApi* | [**setUserProfile**](docs/UserProfileHostingApi.md#setuserprofile) | **POST** /v4/user/profile/set | Set user profile


## Documentation for Models

- [AccessTokenExpireRequest](docs/AccessTokenExpireRequest.md)
- [AccessTokenIssueRequest](docs/AccessTokenIssueRequest.md)
- [AccessTokenIssueResponse](docs/AccessTokenIssueResponse.md)
- [AccessTokenIssueResult](docs/AccessTokenIssueResult.md)
- [BannedUser](docs/BannedUser.md)
- [ChannelAttributeGetRequest](docs/ChannelAttributeGetRequest.md)
- [ChannelAttributeGetResponse](docs/ChannelAttributeGetResponse.md)
- [ChannelAttributeGetResponseResult](docs/ChannelAttributeGetResponseResult.md)
- [ChannelAttributeTagItem](docs/ChannelAttributeTagItem.md)
- [ChannelMessageHistoryDeleteRequest](docs/ChannelMessageHistoryDeleteRequest.md)
- [ChannelMessageSendResponse](docs/ChannelMessageSendResponse.md)
- [ChannelMessageSendResponseResult](docs/ChannelMessageSendResponseResult.md)
- [ChannelNotificationState](docs/ChannelNotificationState.md)
- [ChannelPinSetRequest](docs/ChannelPinSetRequest.md)
- [ChannelPinState](docs/ChannelPinState.md)
- [ChannelPushGetRequest](docs/ChannelPushGetRequest.md)
- [ChannelPushGetResponse](docs/ChannelPushGetResponse.md)
- [ChannelPushGetResponseResult](docs/ChannelPushGetResponseResult.md)
- [ChannelPushSetRequest](docs/ChannelPushSetRequest.md)
- [ChannelTagAddRequest](docs/ChannelTagAddRequest.md)
- [ChannelTagListRequest](docs/ChannelTagListRequest.md)
- [ChannelTagListResponse](docs/ChannelTagListResponse.md)
- [ChannelTagListResponseResult](docs/ChannelTagListResponseResult.md)
- [ChannelTagRemoveRequest](docs/ChannelTagRemoveRequest.md)
- [ChannelTagTargetItem](docs/ChannelTagTargetItem.md)
- [ChannelTypeMessageMetadataDeleteRequest](docs/ChannelTypeMessageMetadataDeleteRequest.md)
- [ChannelTypeMessageMetadataListRequest](docs/ChannelTypeMessageMetadataListRequest.md)
- [ChannelTypeMessageMetadataListResponse](docs/ChannelTypeMessageMetadataListResponse.md)
- [ChannelTypeMessageMetadataListResponseResult](docs/ChannelTypeMessageMetadataListResponseResult.md)
- [ChannelTypeMuteListRequest](docs/ChannelTypeMuteListRequest.md)
- [ChannelTypeMuteListResponse](docs/ChannelTypeMuteListResponse.md)
- [ChannelTypeMuteListResponseResult](docs/ChannelTypeMuteListResponseResult.md)
- [ChannelTypeMuteSetRequest](docs/ChannelTypeMuteSetRequest.md)
- [ChannelTypeNotificationGetRequest](docs/ChannelTypeNotificationGetRequest.md)
- [ChannelTypeNotificationGetResponse](docs/ChannelTypeNotificationGetResponse.md)
- [ChannelTypeNotificationGetResponseResult](docs/ChannelTypeNotificationGetResponseResult.md)
- [ChannelTypeNotificationSetRequest](docs/ChannelTypeNotificationSetRequest.md)
- [CodeOnlyResponse](docs/CodeOnlyResponse.md)
- [CommunityChannelAllowedSenderItem](docs/CommunityChannelAllowedSenderItem.md)
- [CommunityChannelAllowedSenderListGetRequest](docs/CommunityChannelAllowedSenderListGetRequest.md)
- [CommunityChannelAllowedSenderListGetResponse](docs/CommunityChannelAllowedSenderListGetResponse.md)
- [CommunityChannelAllowedSenderListGetResponseResult](docs/CommunityChannelAllowedSenderListGetResponseResult.md)
- [CommunityChannelAllowedSenderListUpdateRequest](docs/CommunityChannelAllowedSenderListUpdateRequest.md)
- [CommunityChannelCreateRequest](docs/CommunityChannelCreateRequest.md)
- [CommunityChannelDismissRequest](docs/CommunityChannelDismissRequest.md)
- [CommunityChannelFreezeListGetRequest](docs/CommunityChannelFreezeListGetRequest.md)
- [CommunityChannelFreezeListGetResponse](docs/CommunityChannelFreezeListGetResponse.md)
- [CommunityChannelFreezeListGetResponseResult](docs/CommunityChannelFreezeListGetResponseResult.md)
- [CommunityChannelFreezeListSetRequest](docs/CommunityChannelFreezeListSetRequest.md)
- [CommunityChannelHistoryMessageListRequest](docs/CommunityChannelHistoryMessageListRequest.md)
- [CommunityChannelMemberExistResponse](docs/CommunityChannelMemberExistResponse.md)
- [CommunityChannelMemberExistResponseResult](docs/CommunityChannelMemberExistResponseResult.md)
- [CommunityChannelMemberRequest](docs/CommunityChannelMemberRequest.md)
- [CommunityChannelMessageMetadataDeleteRequest](docs/CommunityChannelMessageMetadataDeleteRequest.md)
- [CommunityChannelMessageMetadataListRequest](docs/CommunityChannelMessageMetadataListRequest.md)
- [CommunityChannelMessageMetadataListResponse](docs/CommunityChannelMessageMetadataListResponse.md)
- [CommunityChannelMessageMetadataListResponseResult](docs/CommunityChannelMessageMetadataListResponseResult.md)
- [CommunityChannelMessageMetadataSetRequest](docs/CommunityChannelMessageMetadataSetRequest.md)
- [CommunityChannelMessageSendRequest](docs/CommunityChannelMessageSendRequest.md)
- [CommunityChannelMessageUpdateRequest](docs/CommunityChannelMessageUpdateRequest.md)
- [CommunityChannelMuteListAddRequest](docs/CommunityChannelMuteListAddRequest.md)
- [CommunityChannelMuteListGetRequest](docs/CommunityChannelMuteListGetRequest.md)
- [CommunityChannelMuteListGetResponse](docs/CommunityChannelMuteListGetResponse.md)
- [CommunityChannelMuteListGetResponseResult](docs/CommunityChannelMuteListGetResponseResult.md)
- [CommunityChannelMuteListRemoveRequest](docs/CommunityChannelMuteListRemoveRequest.md)
- [CommunityChannelMutedMemberItem](docs/CommunityChannelMutedMemberItem.md)
- [CommunityChannelSubchannelUserGroupListRequest](docs/CommunityChannelSubchannelUserGroupListRequest.md)
- [CommunityChannelSubchannelUserGroupListResponse](docs/CommunityChannelSubchannelUserGroupListResponse.md)
- [CommunityChannelSubchannelUserGroupListResponseResult](docs/CommunityChannelSubchannelUserGroupListResponseResult.md)
- [CommunityChannelUpdateRequest](docs/CommunityChannelUpdateRequest.md)
- [CommunityChannelUserGroupAddRequest](docs/CommunityChannelUserGroupAddRequest.md)
- [CommunityChannelUserGroupBindingRequest](docs/CommunityChannelUserGroupBindingRequest.md)
- [CommunityChannelUserGroupDeleteRequest](docs/CommunityChannelUserGroupDeleteRequest.md)
- [CommunityChannelUserGroupItem](docs/CommunityChannelUserGroupItem.md)
- [CommunityChannelUserGroupListRequest](docs/CommunityChannelUserGroupListRequest.md)
- [CommunityChannelUserGroupListResponse](docs/CommunityChannelUserGroupListResponse.md)
- [CommunityChannelUserGroupListResponseResult](docs/CommunityChannelUserGroupListResponseResult.md)
- [CommunityChannelUserGroupSubchannelListRequest](docs/CommunityChannelUserGroupSubchannelListRequest.md)
- [CommunityChannelUserGroupSubchannelListResponse](docs/CommunityChannelUserGroupSubchannelListResponse.md)
- [CommunityChannelUserGroupSubchannelListResponseResult](docs/CommunityChannelUserGroupSubchannelListResponseResult.md)
- [CommunityChannelUserGroupUsersRequest](docs/CommunityChannelUserGroupUsersRequest.md)
- [CommunityChannelUserUserGroupListRequest](docs/CommunityChannelUserUserGroupListRequest.md)
- [CommunityChannelUserUserGroupListResponse](docs/CommunityChannelUserUserGroupListResponse.md)
- [CommunityChannelUserUserGroupListResponseResult](docs/CommunityChannelUserUserGroupListResponseResult.md)
- [CommunityPrivateSubchannelMemberListRequest](docs/CommunityPrivateSubchannelMemberListRequest.md)
- [CommunityPrivateSubchannelMemberListResponse](docs/CommunityPrivateSubchannelMemberListResponse.md)
- [CommunityPrivateSubchannelMemberListResponseResult](docs/CommunityPrivateSubchannelMemberListResponseResult.md)
- [CommunityPrivateSubchannelMembersRequest](docs/CommunityPrivateSubchannelMembersRequest.md)
- [CommunitySubchannelCreateRequest](docs/CommunitySubchannelCreateRequest.md)
- [CommunitySubchannelItem](docs/CommunitySubchannelItem.md)
- [CommunitySubchannelKeyRequest](docs/CommunitySubchannelKeyRequest.md)
- [CommunitySubchannelListRequest](docs/CommunitySubchannelListRequest.md)
- [CommunitySubchannelListResponse](docs/CommunitySubchannelListResponse.md)
- [CommunitySubchannelListResponseResult](docs/CommunitySubchannelListResponseResult.md)
- [CommunitySubchannelTypeUpdateRequest](docs/CommunitySubchannelTypeUpdateRequest.md)
- [CommunityUserSubchannelListRequest](docs/CommunityUserSubchannelListRequest.md)
- [CommunityUserSubchannelListResponse](docs/CommunityUserSubchannelListResponse.md)
- [CommunityUserSubchannelListResponseResult](docs/CommunityUserSubchannelListResponseResult.md)
- [DirectChannelMessageSendRequest](docs/DirectChannelMessageSendRequest.md)
- [DirectChannelMessageUpdateRequest](docs/DirectChannelMessageUpdateRequest.md)
- [FriendAddRequest](docs/FriendAddRequest.md)
- [FriendCleanRequest](docs/FriendCleanRequest.md)
- [FriendDeleteRequest](docs/FriendDeleteRequest.md)
- [FriendItem](docs/FriendItem.md)
- [FriendListRequest](docs/FriendListRequest.md)
- [FriendListResponse](docs/FriendListResponse.md)
- [FriendListResponseResult](docs/FriendListResponseResult.md)
- [FriendPermissionGetRequest](docs/FriendPermissionGetRequest.md)
- [FriendPermissionGetResponse](docs/FriendPermissionGetResponse.md)
- [FriendPermissionGetResponseResult](docs/FriendPermissionGetResponseResult.md)
- [FriendPermissionItem](docs/FriendPermissionItem.md)
- [FriendPermissionSetRequest](docs/FriendPermissionSetRequest.md)
- [FriendProfileSetRequest](docs/FriendProfileSetRequest.md)
- [FriendRelationshipGetRequest](docs/FriendRelationshipGetRequest.md)
- [FriendRelationshipGetResponse](docs/FriendRelationshipGetResponse.md)
- [FriendRelationshipGetResponseResult](docs/FriendRelationshipGetResponseResult.md)
- [FriendRelationshipItem](docs/FriendRelationshipItem.md)
- [GroupChannelAdminUsersRequest](docs/GroupChannelAdminUsersRequest.md)
- [GroupChannelAliasGetRequest](docs/GroupChannelAliasGetRequest.md)
- [GroupChannelAliasGetResponse](docs/GroupChannelAliasGetResponse.md)
- [GroupChannelAliasGetResponseResult](docs/GroupChannelAliasGetResponseResult.md)
- [GroupChannelAliasSetRequest](docs/GroupChannelAliasSetRequest.md)
- [GroupChannelAllowedSenderListGetRequest](docs/GroupChannelAllowedSenderListGetRequest.md)
- [GroupChannelAllowedSenderListGetResponse](docs/GroupChannelAllowedSenderListGetResponse.md)
- [GroupChannelAllowedSenderListGetResponseResult](docs/GroupChannelAllowedSenderListGetResponseResult.md)
- [GroupChannelAllowedSenderListUpdateRequest](docs/GroupChannelAllowedSenderListUpdateRequest.md)
- [GroupChannelCreateRequest](docs/GroupChannelCreateRequest.md)
- [GroupChannelDismissRequest](docs/GroupChannelDismissRequest.md)
- [GroupChannelFavoriteItem](docs/GroupChannelFavoriteItem.md)
- [GroupChannelFreezeListGetRequest](docs/GroupChannelFreezeListGetRequest.md)
- [GroupChannelFreezeListGetResponse](docs/GroupChannelFreezeListGetResponse.md)
- [GroupChannelFreezeListGetResponseResult](docs/GroupChannelFreezeListGetResponseResult.md)
- [GroupChannelFreezeListUpdateRequest](docs/GroupChannelFreezeListUpdateRequest.md)
- [GroupChannelFreezeStatusItem](docs/GroupChannelFreezeStatusItem.md)
- [GroupChannelJoinRequest](docs/GroupChannelJoinRequest.md)
- [GroupChannelJoinResponse](docs/GroupChannelJoinResponse.md)
- [GroupChannelJoinedItem](docs/GroupChannelJoinedItem.md)
- [GroupChannelJoinedListRequest](docs/GroupChannelJoinedListRequest.md)
- [GroupChannelJoinedListResponse](docs/GroupChannelJoinedListResponse.md)
- [GroupChannelJoinedListResponseResult](docs/GroupChannelJoinedListResponseResult.md)
- [GroupChannelKickUserFromAllRequest](docs/GroupChannelKickUserFromAllRequest.md)
- [GroupChannelListRequest](docs/GroupChannelListRequest.md)
- [GroupChannelListResponse](docs/GroupChannelListResponse.md)
- [GroupChannelListResponseResult](docs/GroupChannelListResponseResult.md)
- [GroupChannelMemberBatchGetRequest](docs/GroupChannelMemberBatchGetRequest.md)
- [GroupChannelMemberBatchGetResponse](docs/GroupChannelMemberBatchGetResponse.md)
- [GroupChannelMemberBatchGetResponseResult](docs/GroupChannelMemberBatchGetResponseResult.md)
- [GroupChannelMemberFavoritesListRequest](docs/GroupChannelMemberFavoritesListRequest.md)
- [GroupChannelMemberFavoritesListResponse](docs/GroupChannelMemberFavoritesListResponse.md)
- [GroupChannelMemberFavoritesListResponseResult](docs/GroupChannelMemberFavoritesListResponseResult.md)
- [GroupChannelMemberFavoritesUpdateRequest](docs/GroupChannelMemberFavoritesUpdateRequest.md)
- [GroupChannelMemberItem](docs/GroupChannelMemberItem.md)
- [GroupChannelMemberListRequest](docs/GroupChannelMemberListRequest.md)
- [GroupChannelMemberListResponse](docs/GroupChannelMemberListResponse.md)
- [GroupChannelMemberListResponseResult](docs/GroupChannelMemberListResponseResult.md)
- [GroupChannelMemberSetRequest](docs/GroupChannelMemberSetRequest.md)
- [GroupChannelMessageSendRequest](docs/GroupChannelMessageSendRequest.md)
- [GroupChannelMessageUpdateRequest](docs/GroupChannelMessageUpdateRequest.md)
- [GroupChannelMutedMemberItem](docs/GroupChannelMutedMemberItem.md)
- [GroupChannelProfileItem](docs/GroupChannelProfileItem.md)
- [GroupChannelProfileListRequest](docs/GroupChannelProfileListRequest.md)
- [GroupChannelProfileListResponse](docs/GroupChannelProfileListResponse.md)
- [GroupChannelProfileListResponseResult](docs/GroupChannelProfileListResponseResult.md)
- [GroupChannelProfileUpdateRequest](docs/GroupChannelProfileUpdateRequest.md)
- [GroupChannelQuitRequest](docs/GroupChannelQuitRequest.md)
- [GroupChannelSummaryItem](docs/GroupChannelSummaryItem.md)
- [GroupChannelTransferOwnerRequest](docs/GroupChannelTransferOwnerRequest.md)
- [GroupChannelUserMuteListAddRequest](docs/GroupChannelUserMuteListAddRequest.md)
- [GroupChannelUserMuteListGetRequest](docs/GroupChannelUserMuteListGetRequest.md)
- [GroupChannelUserMuteListGetResponse](docs/GroupChannelUserMuteListGetResponse.md)
- [GroupChannelUserMuteListGetResponseResult](docs/GroupChannelUserMuteListGetResponseResult.md)
- [GroupChannelUserMuteListRemoveRequest](docs/GroupChannelUserMuteListRemoveRequest.md)
- [MessageChannelDelivery](docs/MessageChannelDelivery.md)
- [MessageDeleteRequest](docs/MessageDeleteRequest.md)
- [MessageHistoryResponse](docs/MessageHistoryResponse.md)
- [MessageHistoryResponseResult](docs/MessageHistoryResponseResult.md)
- [MessageMetadataListItem](docs/MessageMetadataListItem.md)
- [MessageMetadataSetRequest](docs/MessageMetadataSetRequest.md)
- [MessageRecord](docs/MessageRecord.md)
- [MessageUserDelivery](docs/MessageUserDelivery.md)
- [OpenChannelAllowedSenderListGetResponse](docs/OpenChannelAllowedSenderListGetResponse.md)
- [OpenChannelAllowedSenderListGetResponseResult](docs/OpenChannelAllowedSenderListGetResponseResult.md)
- [OpenChannelAllowedSenderListUpdateRequest](docs/OpenChannelAllowedSenderListUpdateRequest.md)
- [OpenChannelBannedParticipantItem](docs/OpenChannelBannedParticipantItem.md)
- [OpenChannelBroadcastRequest](docs/OpenChannelBroadcastRequest.md)
- [OpenChannelCreateRequest](docs/OpenChannelCreateRequest.md)
- [OpenChannelDestroyRequest](docs/OpenChannelDestroyRequest.md)
- [OpenChannelDestroyTypeSetRequest](docs/OpenChannelDestroyTypeSetRequest.md)
- [OpenChannelFreezeCheckRequest](docs/OpenChannelFreezeCheckRequest.md)
- [OpenChannelFreezeCheckResponse](docs/OpenChannelFreezeCheckResponse.md)
- [OpenChannelFreezeCheckResponseResult](docs/OpenChannelFreezeCheckResponseResult.md)
- [OpenChannelFreezeListGetRequest](docs/OpenChannelFreezeListGetRequest.md)
- [OpenChannelFreezeListGetResponse](docs/OpenChannelFreezeListGetResponse.md)
- [OpenChannelFreezeListGetResponseResult](docs/OpenChannelFreezeListGetResponseResult.md)
- [OpenChannelFreezeListUpdateRequest](docs/OpenChannelFreezeListUpdateRequest.md)
- [OpenChannelGetRequest](docs/OpenChannelGetRequest.md)
- [OpenChannelGetResponse](docs/OpenChannelGetResponse.md)
- [OpenChannelGetResponseResult](docs/OpenChannelGetResponseResult.md)
- [OpenChannelGlobalMuteListAddRequest](docs/OpenChannelGlobalMuteListAddRequest.md)
- [OpenChannelGlobalMuteListRemoveRequest](docs/OpenChannelGlobalMuteListRemoveRequest.md)
- [OpenChannelLowPriorityMessageTypeListRequest](docs/OpenChannelLowPriorityMessageTypeListRequest.md)
- [OpenChannelMessageSendRequest](docs/OpenChannelMessageSendRequest.md)
- [OpenChannelMessageTypeListResponse](docs/OpenChannelMessageTypeListResponse.md)
- [OpenChannelMessageTypeListResponseResult](docs/OpenChannelMessageTypeListResponseResult.md)
- [OpenChannelMetadataBatchGetRequest](docs/OpenChannelMetadataBatchGetRequest.md)
- [OpenChannelMetadataBatchGetResponse](docs/OpenChannelMetadataBatchGetResponse.md)
- [OpenChannelMetadataBatchGetResponseResult](docs/OpenChannelMetadataBatchGetResponseResult.md)
- [OpenChannelMetadataBatchRemoveRequest](docs/OpenChannelMetadataBatchRemoveRequest.md)
- [OpenChannelMetadataBatchSetRequest](docs/OpenChannelMetadataBatchSetRequest.md)
- [OpenChannelMetadataEntry](docs/OpenChannelMetadataEntry.md)
- [OpenChannelMutedParticipantItem](docs/OpenChannelMutedParticipantItem.md)
- [OpenChannelParticipantBanListGetResponse](docs/OpenChannelParticipantBanListGetResponse.md)
- [OpenChannelParticipantBanListGetResponseResult](docs/OpenChannelParticipantBanListGetResponseResult.md)
- [OpenChannelParticipantExistItem](docs/OpenChannelParticipantExistItem.md)
- [OpenChannelParticipantExistRequest](docs/OpenChannelParticipantExistRequest.md)
- [OpenChannelParticipantExistResponse](docs/OpenChannelParticipantExistResponse.md)
- [OpenChannelParticipantExistResponseResult](docs/OpenChannelParticipantExistResponseResult.md)
- [OpenChannelParticipantIdsRequest](docs/OpenChannelParticipantIdsRequest.md)
- [OpenChannelParticipantIdsResponse](docs/OpenChannelParticipantIdsResponse.md)
- [OpenChannelParticipantIdsResponseResult](docs/OpenChannelParticipantIdsResponseResult.md)
- [OpenChannelParticipantItem](docs/OpenChannelParticipantItem.md)
- [OpenChannelParticipantListByChannelRequest](docs/OpenChannelParticipantListByChannelRequest.md)
- [OpenChannelParticipantListRequest](docs/OpenChannelParticipantListRequest.md)
- [OpenChannelParticipantListResponse](docs/OpenChannelParticipantListResponse.md)
- [OpenChannelParticipantListResponseResult](docs/OpenChannelParticipantListResponseResult.md)
- [OpenChannelParticipantMuteListAddRequest](docs/OpenChannelParticipantMuteListAddRequest.md)
- [OpenChannelParticipantMuteListGetResponse](docs/OpenChannelParticipantMuteListGetResponse.md)
- [OpenChannelParticipantMuteListGetResponseResult](docs/OpenChannelParticipantMuteListGetResponseResult.md)
- [OpenChannelParticipantMuteListRemoveRequest](docs/OpenChannelParticipantMuteListRemoveRequest.md)
- [OpenChannelPriorityMessageTypeListRequest](docs/OpenChannelPriorityMessageTypeListRequest.md)
- [ProfanityWordBatchAddRequest](docs/ProfanityWordBatchAddRequest.md)
- [ProfanityWordBatchAddResponse](docs/ProfanityWordBatchAddResponse.md)
- [ProfanityWordBatchAddResponseResult](docs/ProfanityWordBatchAddResponseResult.md)
- [ProfanityWordBatchDeleteRequest](docs/ProfanityWordBatchDeleteRequest.md)
- [ProfanityWordDeleteRequest](docs/ProfanityWordDeleteRequest.md)
- [ProfanityWordItem](docs/ProfanityWordItem.md)
- [ProfanityWordListRequest](docs/ProfanityWordListRequest.md)
- [ProfanityWordListResponse](docs/ProfanityWordListResponse.md)
- [ProfanityWordListResponseResult](docs/ProfanityWordListResponseResult.md)
- [ProfanityWordListedItem](docs/ProfanityWordListedItem.md)
- [SingleMessageIdResponse](docs/SingleMessageIdResponse.md)
- [SingleMessageIdResponseResult](docs/SingleMessageIdResponseResult.md)
- [SystemChannelBroadcastAllRequest](docs/SystemChannelBroadcastAllRequest.md)
- [SystemChannelBroadcastDeleteRequest](docs/SystemChannelBroadcastDeleteRequest.md)
- [SystemChannelBroadcastOnlineRequest](docs/SystemChannelBroadcastOnlineRequest.md)
- [SystemChannelMessageSendRequest](docs/SystemChannelMessageSendRequest.md)
- [SystemChannelPushAudience](docs/SystemChannelPushAudience.md)
- [SystemChannelPushMessage](docs/SystemChannelPushMessage.md)
- [SystemChannelPushNotification](docs/SystemChannelPushNotification.md)
- [SystemChannelPushRequest](docs/SystemChannelPushRequest.md)
- [SystemChannelPushResponse](docs/SystemChannelPushResponse.md)
- [SystemChannelPushResponseResult](docs/SystemChannelPushResponseResult.md)
- [UserBanListRequest](docs/UserBanListRequest.md)
- [UserBanListResponse](docs/UserBanListResponse.md)
- [UserBanListResponseResult](docs/UserBanListResponseResult.md)
- [UserBanRequest](docs/UserBanRequest.md)
- [UserBlocklistAddRequest](docs/UserBlocklistAddRequest.md)
- [UserBlocklistGetRequest](docs/UserBlocklistGetRequest.md)
- [UserBlocklistGetResponse](docs/UserBlocklistGetResponse.md)
- [UserBlocklistGetResponseResult](docs/UserBlocklistGetResponseResult.md)
- [UserBlocklistRemoveRequest](docs/UserBlocklistRemoveRequest.md)
- [UserChannelTagAddRequest](docs/UserChannelTagAddRequest.md)
- [UserChannelTagItem](docs/UserChannelTagItem.md)
- [UserChannelTagListItem](docs/UserChannelTagListItem.md)
- [UserChannelTagListRequest](docs/UserChannelTagListRequest.md)
- [UserChannelTagListResponse](docs/UserChannelTagListResponse.md)
- [UserChannelTagListResponseResult](docs/UserChannelTagListResponseResult.md)
- [UserChannelTagRemoveRequest](docs/UserChannelTagRemoveRequest.md)
- [UserConnectionStatusRequest](docs/UserConnectionStatusRequest.md)
- [UserConnectionStatusResponse](docs/UserConnectionStatusResponse.md)
- [UserConnectionStatusResponseResult](docs/UserConnectionStatusResponseResult.md)
- [UserGetRequest](docs/UserGetRequest.md)
- [UserGetResponse](docs/UserGetResponse.md)
- [UserGetResult](docs/UserGetResult.md)
- [UserIdsMax100Request](docs/UserIdsMax100Request.md)
- [UserIdsMax20Request](docs/UserIdsMax20Request.md)
- [UserIdsRequest](docs/UserIdsRequest.md)
- [UserMessageSendResponse](docs/UserMessageSendResponse.md)
- [UserMessageSendResponseResult](docs/UserMessageSendResponseResult.md)
- [UserOperationResponse](docs/UserOperationResponse.md)
- [UserOperationResponseResult](docs/UserOperationResponseResult.md)
- [UserProfileBatchGetResponse](docs/UserProfileBatchGetResponse.md)
- [UserProfileBatchGetResponseResult](docs/UserProfileBatchGetResponseResult.md)
- [UserProfileItem](docs/UserProfileItem.md)
- [UserProfileListItem](docs/UserProfileListItem.md)
- [UserProfileListRequest](docs/UserProfileListRequest.md)
- [UserProfileListResponse](docs/UserProfileListResponse.md)
- [UserProfileListResponseResult](docs/UserProfileListResponseResult.md)
- [UserProfileSetRequest](docs/UserProfileSetRequest.md)
- [UserProfileSetResponse](docs/UserProfileSetResponse.md)
- [UserSoftDeletedListRequest](docs/UserSoftDeletedListRequest.md)
- [UserSoftDeletedListResponse](docs/UserSoftDeletedListResponse.md)
- [UserSoftDeletedListResponseResult](docs/UserSoftDeletedListResponseResult.md)
- [UserTagBatchGetItem](docs/UserTagBatchGetItem.md)
- [UserTagBatchGetRequest](docs/UserTagBatchGetRequest.md)
- [UserTagBatchGetResponse](docs/UserTagBatchGetResponse.md)
- [UserTagBatchGetResponseResult](docs/UserTagBatchGetResponseResult.md)
- [UserTagBatchSetRequest](docs/UserTagBatchSetRequest.md)
- [UserUpdateRequest](docs/UserUpdateRequest.md)


## Documentation for Authorization


Authentication schemes defined for the API:

### NexconnSignature

- **Type**: API key
- **API key parameter name**: App-Key
- **Location**: HTTP header


## Package Info

- Repository: `https://gitlab2.rongcloud.net/public-server/nexconn-server-sdk-node`
- Package version: `0.1.0`

## License

This project is licensed under the [MIT License](LICENSE).
