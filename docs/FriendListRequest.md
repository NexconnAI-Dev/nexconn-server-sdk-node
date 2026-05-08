# FriendListRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** |  | [default to undefined]
**pageToken** | **string** |  | [optional] [default to undefined]
**pageSize** | **number** |  | [optional] [default to 50]
**order** | **number** | &#x60;0&#x60; for ascending order and &#x60;1&#x60; for descending order. | [optional] [default to undefined]

## Example

```typescript
import { FriendListRequest } from '@nexconn/server-sdk';

const instance: FriendListRequest = {
    userId,
    pageToken,
    pageSize,
    order,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
