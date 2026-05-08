# FriendAddRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** |  | [default to undefined]
**targetId** | **string** |  | [default to undefined]
**action** | **number** | &#x60;1&#x60; means add with verification and &#x60;2&#x60; means add directly. | [optional] [default to undefined]
**extra** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { FriendAddRequest } from '@nexconn/server-sdk';

const instance: FriendAddRequest = {
    userId,
    targetId,
    action,
    extra,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
