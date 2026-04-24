# SystemChannelMessageSendRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromUserId** | **string** | Sender user ID. The sender should have an access token. | [default to undefined]
**toUserIds** | **Array&lt;string&gt;** | Recipient user IDs. Up to 100 users are supported in a single request. | [default to undefined]
**messageType** | **string** | Message type. Supports built-in types and custom types. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | [default to undefined]
**content** | **string** | Message content payload serialized as a string. Built-in message types should use a JSON object string. Maximum size is 128 KB. | [default to undefined]
**pushContent** | **string** | Push notification text for offline recipients. Required for custom or notification messages that need push delivery. | [optional] [default to undefined]
**pushData** | **string** | Custom push payload data. Exposed as &#x60;appData&#x60; on iOS and Android. | [optional] [default to undefined]
**shouldPersist** | **number** | Whether to store the message in cloud message history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] [default to undefined]
**contentAvailable** | **number** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. | [optional] [default to undefined]
**disablePush** | **boolean** | Whether to suppress push notifications for offline recipients. | [optional] [default to undefined]
**pushExt** | **string** | Extended push configuration (JSON string as accepted by &#x60;SystemChannelMsgSendInput&#x60;). | [optional] [default to undefined]
**disableUpdateLastMsg** | **boolean** | Whether to keep this message from updating the system channel\&#39;s last-message preview. | [optional] [default to undefined]

## Example

```typescript
import { SystemChannelMessageSendRequest } from 'nexconn-sdk-node';

const instance: SystemChannelMessageSendRequest = {
    fromUserId,
    toUserIds,
    messageType,
    content,
    pushContent,
    pushData,
    shouldPersist,
    contentAvailable,
    disablePush,
    pushExt,
    disableUpdateLastMsg,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
