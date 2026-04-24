# ChannelTypeNotificationSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelType** | **string** | Session / channel type as a string (&#x60;1&#x60; to &#x60;10&#x60; as accepted by the server). | [default to undefined]
**requestId** | **string** | User ID whose channel-type notification setting is updated. | [default to undefined]
**noDisturbLevel** | **number** | Do-not-disturb level for the specified channel type. | [default to undefined]

## Example

```typescript
import { ChannelTypeNotificationSetRequest } from 'nexconn-sdk-node';

const instance: ChannelTypeNotificationSetRequest = {
    channelType,
    requestId,
    noDisturbLevel,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
