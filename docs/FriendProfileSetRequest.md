# FriendProfileSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** |  | [default to undefined]
**targetId** | **string** |  | [default to undefined]
**alias** | **string** | Omit this field to clear the existing alias. | [optional] [default to undefined]
**friendExtProfile** | **{ [key: string]: string; }** | Custom friend extension attributes. Keys should match &#x60;ext_xxxxx&#x60;, may contain letters, digits, and underscores, and support up to 10 entries.  | [optional] [default to undefined]

## Example

```typescript
import { FriendProfileSetRequest } from '@nexconn/server-sdk';

const instance: FriendProfileSetRequest = {
    userId,
    targetId,
    alias,
    friendExtProfile,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
