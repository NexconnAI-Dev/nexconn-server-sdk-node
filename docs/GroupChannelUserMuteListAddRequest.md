# GroupChannelUserMuteListAddRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | Optional. When omitted, the operation applies to all group channels according to the PDF. | [optional] [default to undefined]
**userIds** | **Array&lt;string&gt;** |  | [default to undefined]
**durationMinutes** | **number** |  | [default to undefined]

## Example

```typescript
import { GroupChannelUserMuteListAddRequest } from '@nexconn/server-sdk';

const instance: GroupChannelUserMuteListAddRequest = {
    channelId,
    userIds,
    durationMinutes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
