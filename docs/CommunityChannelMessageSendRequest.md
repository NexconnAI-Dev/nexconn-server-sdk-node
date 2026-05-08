# CommunityChannelMessageSendRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromUserId** | **string** | Sender user ID. Non-members can send through the server API, but push display works best when the sender has an access token. | [default to undefined]
**toChannelIds** | **Array&lt;string&gt;** | Target community channel IDs. Up to 3 community channels are supported per request. | [default to undefined]
**toUserIds** | **Array&lt;string&gt;** | Recipient member user IDs for a targeted community message. Only effective when sending to a single community channel. | [optional] [default to undefined]
**messageType** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | [default to undefined]
**content** | **string** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. | [default to undefined]
**pushContent** | **string** | Push notification text for offline recipients. Optional for built-in user content messages and required for push-enabled custom or notification messages. | [optional] [default to undefined]
**pushData** | **string** | Custom push payload data. Exposed as &#x60;appData&#x60; on mobile push payloads. | [optional] [default to undefined]
**shouldPersist** | **number** | Whether to store the message in community message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] [default to undefined]
**isCounted** | **number** | Whether to count this message as unread for offline users. &#x60;1&#x60; counts as unread and &#x60;0&#x60; does not. | [optional] [default to undefined]
**hasMention** | **number** | Whether this is an @mention message. Set to &#x60;1&#x60; when &#x60;content&#x60; contains &#x60;mentionedInfo&#x60;. | [optional] [default to undefined]
**contentAvailable** | **number** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. | [optional] [default to undefined]
**pushExt** | **string** | Extended push configuration (JSON string as accepted by the server &#x60;CommunityChannelMsgSendInput&#x60;). | [optional] [default to undefined]
**subchannelId** | **string** | Target subchannel ID. If omitted, delivery follows the app\&#39;s default community-channel behavior. | [optional] [default to undefined]
**hasMetadata** | **boolean** | Whether to enable message metadata for this message. | [optional] [default to undefined]
**metadata** | **{ [key: string]: any; }** | Custom message metadata entries. Only effective when &#x60;hasMetadata&#x60; is &#x60;true&#x60;. | [optional] [default to undefined]

## Example

```typescript
import { CommunityChannelMessageSendRequest } from '@nexconn/server-sdk';

const instance: CommunityChannelMessageSendRequest = {
    fromUserId,
    toChannelIds,
    toUserIds,
    messageType,
    content,
    pushContent,
    pushData,
    shouldPersist,
    isCounted,
    hasMention,
    contentAvailable,
    pushExt,
    subchannelId,
    hasMetadata,
    metadata,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
