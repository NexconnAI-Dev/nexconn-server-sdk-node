# GroupChannelMemberBatchGetResponseResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pageToken** | **string** | From &#x60;EGMemberListResult.pageToken&#x60;. | [optional] [default to undefined]
**totalCount** | **number** | From &#x60;EGMemberListResult.totalCount&#x60;. | [optional] [default to undefined]
**members** | [**Array&lt;GroupChannelMemberItem&gt;**](GroupChannelMemberItem.md) |  | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelMemberBatchGetResponseResult } from 'nexconn-sdk-node';

const instance: GroupChannelMemberBatchGetResponseResult = {
    pageToken,
    totalCount,
    members,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
