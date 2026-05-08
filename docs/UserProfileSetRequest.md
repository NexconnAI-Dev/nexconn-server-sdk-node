# UserProfileSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** |  | [default to undefined]
**userProfile** | **{ [key: string]: any; }** | Basic profile payload. Either &#x60;userProfile&#x60; or &#x60;userExtProfile&#x60; must be provided. | [optional] [default to undefined]
**userExtProfile** | **{ [key: string]: string; }** | Extended profile payload. Keys are case-sensitive, should use the &#x60;ext_&#x60; prefix, and values must be strings. Either &#x60;userProfile&#x60; or &#x60;userExtProfile&#x60; must be provided.  | [optional] [default to undefined]

## Example

```typescript
import { UserProfileSetRequest } from '@nexconn/server-sdk';

const instance: UserProfileSetRequest = {
    userId,
    userProfile,
    userExtProfile,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
