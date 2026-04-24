# ChannelTypeMessageMetadataDeleteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | **string** |  | [default to undefined]
**userId** | **string** |  | [default to undefined]
**channelType** | **number** | Supports direct and group channels. Legacy field name is &#x60;conversationType&#x60;. | [default to undefined]
**channelId** | **string** | Legacy &#x60;targetId&#x60;. | [default to undefined]
**keys** | **Array&lt;string&gt;** |  | [default to undefined]
**syncToSender** | **number** | Legacy &#x60;syncToSender&#x60;. &#x60;0&#x60; by default. | [optional] [default to undefined]

## Example

```typescript
import { ChannelTypeMessageMetadataDeleteRequest } from 'nexconn-sdk-node';

const instance: ChannelTypeMessageMetadataDeleteRequest = {
    messageId,
    userId,
    channelType,
    channelId,
    keys,
    syncToSender,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
