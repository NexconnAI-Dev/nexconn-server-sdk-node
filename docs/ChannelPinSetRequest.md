# ChannelPinSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** |  | [default to undefined]
**channelType** | **number** | Legacy &#x60;conversationType&#x60;. Current docs use numeric channel types such as &#x60;1&#x60;, &#x60;3&#x60;, and &#x60;6&#x60;. | [default to undefined]
**channelId** | **string** | Legacy &#x60;targetId&#x60;. | [default to undefined]
**isPin** | **boolean** | JSON field name used by the server. &#x60;true&#x60; pins the conversation and &#x60;false&#x60; cancels the pin. | [default to undefined]

## Example

```typescript
import { ChannelPinSetRequest } from '@nexconn/server-sdk';

const instance: ChannelPinSetRequest = {
    userId,
    channelType,
    channelId,
    isPin,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
