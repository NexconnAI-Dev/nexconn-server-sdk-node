# DirectChannelStreamMessageSendRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromUserId** | **string** | Sender user ID. The sender should have an access token so push notifications can display sender information correctly. | [default to undefined]
**toUserId** | **string** | Recipient user ID. Only a single recipient is supported per stream message. | [default to undefined]
**messageType** | **string** | Message type. Fixed value &#x60;RC:StreamMsg&#x60; for stream messages. | [default to undefined]
**content** | [**StreamMessageContent**](StreamMessageContent.md) |  | [default to undefined]
**isEchoToSender** | **number** | Whether to sync the message to the sender\&#39;s client while the sender is online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional] [default to undefined]
**shouldPersist** | **number** | Whether to store the message in recipient cloud history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] [default to undefined]
**metadata** | **{ [key: string]: string; }** | Custom message metadata entries. Keys are limited to 32 characters and values to 4096 characters. Up to 100 key-value pairs. | [optional] [default to undefined]
**disableUpdateLastMsg** | **boolean** | Whether to keep this message from updating the channel\&#39;s last-message preview. | [optional] [default to undefined]

## Example

```typescript
import { DirectChannelStreamMessageSendRequest } from '@nexconn/server-sdk';

const instance: DirectChannelStreamMessageSendRequest = {
    fromUserId,
    toUserId,
    messageType,
    content,
    isEchoToSender,
    shouldPersist,
    metadata,
    disableUpdateLastMsg,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
