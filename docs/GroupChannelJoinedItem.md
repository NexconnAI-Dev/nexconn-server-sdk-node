# GroupChannelJoinedItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | Group channel ID. | [optional] [default to undefined]
**name** | **string** | Group name. | [optional] [default to undefined]
**groupProfile** | **{ [key: string]: any; }** | Group basic profile JSON object. | [optional] [default to undefined]
**groupExtProfile** | **{ [key: string]: any; }** | Group extended profile JSON object. | [optional] [default to undefined]
**permissions** | **{ [key: string]: any; }** | Group permission settings JSON object. | [optional] [default to undefined]
**alias** | **string** | Group alias or remark name set by the querying user. | [optional] [default to undefined]
**owner** | **string** | User ID of the current group owner. | [optional] [default to undefined]
**memberCount** | **number** | Number of members in the group. | [optional] [default to undefined]
**joinedAt** | **number** | Timestamp when the querying user joined the group. | [optional] [default to undefined]
**role** | **number** | The querying user\&#39;s role in the group. &#x60;1&#x60; regular member, &#x60;2&#x60; admin, &#x60;3&#x60; owner. | [optional] [default to undefined]
**createdAt** | **number** | Timestamp when the group was created. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelJoinedItem } from 'nexconn-sdk-node';

const instance: GroupChannelJoinedItem = {
    channelId,
    name,
    groupProfile,
    groupExtProfile,
    permissions,
    alias,
    owner,
    memberCount,
    joinedAt,
    role,
    createdAt,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
