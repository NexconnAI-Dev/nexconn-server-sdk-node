# ChannelPushSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelType** | **string** | Session / channel type as a string (&#x60;1&#x60; to &#x60;10&#x60; as accepted by the server). Matches &#x60;ChannelTypeRequestInput&#x60; in the service. | [default to undefined]
**requestId** | **string** | User ID whose channel notification setting is updated. | [default to undefined]
**channelId** | **string** | Legacy &#x60;targetId&#x60;. | [default to undefined]
**subchannelId** | **string** | Legacy &#x60;busChannel&#x60;. Used for community-channel subchannel level settings. | [optional] [default to undefined]
**noDisturbLevel** | **number** | Do-not-disturb level (required by service validation; range &#x60;-1&#x60; to &#x60;5&#x60;). | [default to undefined]

## Example

```typescript
import { ChannelPushSetRequest } from 'nexconn-sdk-node';

const instance: ChannelPushSetRequest = {
    channelType,
    requestId,
    channelId,
    subchannelId,
    noDisturbLevel,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
