# GroupChannelProfileItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | Group channel ID. | [optional] [default to undefined]
**name** | **string** | Group name. | [optional] [default to undefined]
**groupProfile** | **{ [key: string]: any; }** | Group basic profile JSON object, such as introduction, announcement, and portrait URL. | [optional] [default to undefined]
**groupExtProfile** | **{ [key: string]: any; }** | Extended group profile JSON object. Keys are typically custom fields prefixed with &#x60;ext_&#x60;. | [optional] [default to undefined]
**permissions** | **{ [key: string]: any; }** | Group permission settings JSON object, including join, invite, and profile-management permissions. | [optional] [default to undefined]
**owner** | **string** | User ID of the current group owner. | [optional] [default to undefined]
**createdAt** | **number** | Timestamp when the group was created. | [optional] [default to undefined]
**memberCount** | **number** | Current number of group members. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelProfileItem } from '@nexconn/server-sdk';

const instance: GroupChannelProfileItem = {
    channelId,
    name,
    groupProfile,
    groupExtProfile,
    permissions,
    owner,
    createdAt,
    memberCount,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
