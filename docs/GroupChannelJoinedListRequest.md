# GroupChannelJoinedListRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** | User ID whose joined groups should be listed. | [default to undefined]
**role** | **number** | Role filter. &#x60;0&#x60; all roles, &#x60;1&#x60; regular member, &#x60;2&#x60; admin, &#x60;3&#x60; owner. | [optional] [default to undefined]
**pageToken** | **string** | Pagination token returned by the previous request. Omit it for the first page. | [optional] [default to undefined]
**pageSize** | **number** | Number of groups to return per page. The official default is 50 and the maximum is 100. | [optional] [default to undefined]
**order** | **number** | Sort order by join time. &#x60;0&#x60; ascending and &#x60;1&#x60; descending. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelJoinedListRequest } from '@nexconn/server-sdk';

const instance: GroupChannelJoinedListRequest = {
    userId,
    role,
    pageToken,
    pageSize,
    order,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
