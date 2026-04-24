# ChannelPushGetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelType** | **string** | Session / channel type as a string (&#x60;1&#x60; to &#x60;10&#x60; as accepted by the server). | [default to undefined]
**requestId** | **string** | User ID whose channel notification setting is queried. | [default to undefined]
**channelId** | **string** | Legacy &#x60;targetId&#x60;. | [default to undefined]
**subchannelId** | **string** | Legacy &#x60;busChannel&#x60;. Used for community-channel subchannel level settings. | [optional] [default to undefined]

## Example

```typescript
import { ChannelPushGetRequest } from 'nexconn-sdk-node';

const instance: ChannelPushGetRequest = {
    channelType,
    requestId,
    channelId,
    subchannelId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
