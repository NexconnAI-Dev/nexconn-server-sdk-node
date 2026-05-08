# GroupChannelSummaryItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**groupProfile** | **{ [key: string]: any; }** | Group basic profile object as in &#x60;EGGroupListResult.GroupItem.groupProfile&#x60;. | [optional] [default to undefined]
**creator** | **string** | Group creator user ID. | [optional] [default to undefined]
**owner** | **string** |  | [optional] [default to undefined]
**createdAt** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelSummaryItem } from '@nexconn/server-sdk';

const instance: GroupChannelSummaryItem = {
    channelId,
    name,
    groupProfile,
    creator,
    owner,
    createdAt,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
