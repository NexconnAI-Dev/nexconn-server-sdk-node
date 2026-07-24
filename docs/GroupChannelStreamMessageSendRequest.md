# GroupChannelStreamMessageSendRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromUserId** | **string** | Sender user ID. | [default to undefined]
**toChannelId** | **string** | Target group channel ID. | [default to undefined]
**messageType** | **string** | Message type. Fixed value &#x60;RC:StreamMsg&#x60; for stream messages. | [default to undefined]
**content** | [**StreamMessageContent**](StreamMessageContent.md) |  | [default to undefined]
**toUserIds** | **Array&lt;string&gt;** | Recipient member user IDs for a targeted group message. Up to 10 users. | [optional] [default to undefined]
**isEchoToSender** | **number** | Whether to sync the message to the sender\&#39;s client while the sender is online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional] [default to undefined]
**shouldPersist** | **number** | Whether to store the message in cloud message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] [default to undefined]
**hasMention** | **number** | Whether this is an @mention message. Set to &#x60;1&#x60; when &#x60;content&#x60; contains &#x60;mentionedInfo&#x60;. | [optional] [default to undefined]
**metadata** | **{ [key: string]: string; }** | Custom message metadata entries. Keys are limited to 32 characters and values to 4096 characters. Up to 100 key-value pairs. | [optional] [default to undefined]
**disableUpdateLastMsg** | **boolean** | Whether to keep this message from updating the channel\&#39;s last-message preview. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelStreamMessageSendRequest } from '@nexconn/server-sdk';

const instance: GroupChannelStreamMessageSendRequest = {
    fromUserId,
    toChannelId,
    messageType,
    content,
    toUserIds,
    isEchoToSender,
    shouldPersist,
    hasMention,
    metadata,
    disableUpdateLastMsg,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
