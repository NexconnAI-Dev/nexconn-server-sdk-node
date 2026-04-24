# ChannelAttributeGetResponseResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [optional] [default to undefined]
**channelType** | **number** |  | [optional] [default to undefined]
**pin** | [**ChannelPinState**](ChannelPinState.md) |  | [optional] [default to undefined]
**notification** | [**ChannelNotificationState**](ChannelNotificationState.md) |  | [optional] [default to undefined]
**tags** | [**Array&lt;ChannelAttributeTagItem&gt;**](ChannelAttributeTagItem.md) | Same shape as &#x60;ChannelAttributeResult.TagInfo&#x60; (no &#x60;createdAt&#x60;; distinct from user tag list items). | [optional] [default to undefined]

## Example

```typescript
import { ChannelAttributeGetResponseResult } from 'nexconn-sdk-node';

const instance: ChannelAttributeGetResponseResult = {
    channelId,
    channelType,
    pin,
    notification,
    tags,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
