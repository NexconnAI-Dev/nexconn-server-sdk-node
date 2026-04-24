# GroupChannelMemberSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [default to undefined]
**userId** | **string** |  | [default to undefined]
**nickname** | **string** |  | [optional] [default to undefined]
**extra** | **string** | Member extra profile string defined by the source API. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelMemberSetRequest } from 'nexconn-sdk-node';

const instance: GroupChannelMemberSetRequest = {
    channelId,
    userId,
    nickname,
    extra,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
