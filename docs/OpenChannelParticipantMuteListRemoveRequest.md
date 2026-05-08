# OpenChannelParticipantMuteListRemoveRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [default to undefined]
**participantIds** | **Array&lt;string&gt;** |  | [default to undefined]
**extra** | **string** | Notification extra payload in JSON string format. | [optional] [default to undefined]
**needNotify** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { OpenChannelParticipantMuteListRemoveRequest } from '@nexconn/server-sdk';

const instance: OpenChannelParticipantMuteListRemoveRequest = {
    channelId,
    participantIds,
    extra,
    needNotify,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
