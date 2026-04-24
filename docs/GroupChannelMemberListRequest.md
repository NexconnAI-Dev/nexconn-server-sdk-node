# GroupChannelMemberListRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | Group channel ID. | [default to undefined]
**memberRole** | **number** | Member role filter. &#x60;0&#x60; all members, &#x60;1&#x60; regular members, &#x60;2&#x60; admins, &#x60;3&#x60; owner. | [optional] [default to undefined]
**pageToken** | **string** | Pagination token returned by the previous request. Omit it for the first page. | [optional] [default to undefined]
**pageSize** | **number** | Number of members to return per page. The official default is 50 and the maximum is 100. | [optional] [default to undefined]
**order** | **number** | Sort order by join time. &#x60;0&#x60; ascending and &#x60;1&#x60; descending. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelMemberListRequest } from 'nexconn-sdk-node';

const instance: GroupChannelMemberListRequest = {
    channelId,
    memberRole,
    pageToken,
    pageSize,
    order,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
