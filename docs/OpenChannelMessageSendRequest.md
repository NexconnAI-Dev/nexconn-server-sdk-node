# OpenChannelMessageSendRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromUserId** | **string** | Sender user ID. | [default to undefined]
**toChannelIds** | **Array&lt;string&gt;** | Target open channel IDs. Multiple channels are allowed; the official documentation recommends up to 10 IDs per request. | [default to undefined]
**messageType** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | [default to undefined]
**content** | **string** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. | [default to undefined]
**shouldPersist** | **number** | Whether to store the message in open channel cloud history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] [default to undefined]
**isEchoToSender** | **number** | Whether to sync the sent message to the sender\&#39;s client while online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional] [default to undefined]
**priority** | **number** | Message priority. &#x60;0&#x60; standard, &#x60;1&#x60; allowlisted, &#x60;2&#x60; high priority, &#x60;3&#x60; low priority. | [optional] [default to undefined]

## Example

```typescript
import { OpenChannelMessageSendRequest } from '@nexconn/server-sdk';

const instance: OpenChannelMessageSendRequest = {
    fromUserId,
    toChannelIds,
    messageType,
    content,
    shouldPersist,
    isEchoToSender,
    priority,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
