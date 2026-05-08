# AccessTokenIssueResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** | User ID that the issued access token belongs to. | [optional] [default to undefined]
**accessToken** | **string** | Issued access token for subsequent user-authenticated requests. | [optional] [default to undefined]

## Example

```typescript
import { AccessTokenIssueResult } from '@nexconn/server-sdk';

const instance: AccessTokenIssueResult = {
    userId,
    accessToken,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
