# GroupChannelProfileUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | Legacy &#x60;groupId&#x60;. | [default to undefined]
**groupProfile** | **{ [key: string]: any; }** | Group basic profile object defined by the source API. | [optional] [default to undefined]
**permissions** | **{ [key: string]: any; }** | Group permission object defined by the source API. | [optional] [default to undefined]
**groupExtProfile** | **{ [key: string]: string; }** | Group extra profile object. Keys should use the &#x60;ext_&#x60; prefix and support up to 10 entries. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelProfileUpdateRequest } from 'nexconn-sdk-node';

const instance: GroupChannelProfileUpdateRequest = {
    channelId,
    groupProfile,
    permissions,
    groupExtProfile,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
