# ChannelTypeMuteSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userIds** | **Array&lt;string&gt;** |  | [default to undefined]
**muteState** | **number** | &#x60;0&#x60; removes mute and &#x60;1&#x60; enables mute. | [default to undefined]
**channelTypes** | **Array&lt;string&gt;** | Channel types to apply (e.g. &#x60;PERSON&#x60;, &#x60;GROUP&#x60;, &#x60;CHATROOM&#x60;). Server validates against supported enums. | [default to undefined]

## Example

```typescript
import { ChannelTypeMuteSetRequest } from '@nexconn/server-sdk';

const instance: ChannelTypeMuteSetRequest = {
    userIds,
    muteState,
    channelTypes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
