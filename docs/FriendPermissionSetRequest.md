# FriendPermissionSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userIds** | **Array&lt;string&gt;** |  | [default to undefined]
**permissionType** | **number** | &#x60;1&#x60; allows everyone, &#x60;2&#x60; requires approval, and &#x60;3&#x60; rejects all requests. | [default to undefined]

## Example

```typescript
import { FriendPermissionSetRequest } from '@nexconn/server-sdk';

const instance: FriendPermissionSetRequest = {
    userIds,
    permissionType,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
