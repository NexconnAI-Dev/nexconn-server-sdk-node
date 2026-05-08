# OpenChannelParticipantExistRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | The open channel ID. | [default to undefined]
**participantIds** | **Array&lt;string&gt;** | User IDs to check. Up to 1,000 users per request. Pass a single-element array to check one user. | [default to undefined]

## Example

```typescript
import { OpenChannelParticipantExistRequest } from '@nexconn/server-sdk';

const instance: OpenChannelParticipantExistRequest = {
    channelId,
    participantIds,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
