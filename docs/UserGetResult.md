# UserGetResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | User display name. | [optional] [default to undefined]
**avatarUrl** | **string** | User avatar URL. | [optional] [default to undefined]
**createdAt** | **string** | User creation time as returned by the server (&#x60;GetUserInfoResult&#x60; serializes this as a string, e.g. formatted date-time). | [optional] [default to undefined]

## Example

```typescript
import { UserGetResult } from 'nexconn-sdk-node';

const instance: UserGetResult = {
    name,
    avatarUrl,
    createdAt,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
