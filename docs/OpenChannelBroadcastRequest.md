# OpenChannelBroadcastRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromUserId** | **string** | Sender user ID. | [default to undefined]
**messageType** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | [default to undefined]
**content** | **string** | Broadcast message payload serialized as a string. Maximum size is 128 KB. | [default to undefined]
**isEchoToSender** | **number** | Whether to sync the broadcast message to the sender\&#39;s client while the sender is online. | [optional] [default to undefined]

## Example

```typescript
import { OpenChannelBroadcastRequest } from '@nexconn/server-sdk';

const instance: OpenChannelBroadcastRequest = {
    fromUserId,
    messageType,
    content,
    isEchoToSender,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
