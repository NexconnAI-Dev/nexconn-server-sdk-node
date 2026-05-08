# DirectChannelMessageSendRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromUserId** | **string** | Sender user ID. The sender should have an access token so push notifications can display sender information correctly. | [default to undefined]
**toUserIds** | **Array&lt;string&gt;** | Recipient user IDs. Up to 1000 users are supported in a single request. | [default to undefined]
**messageType** | **string** | Message type. Supports built-in types and custom types registered in the client SDK. Custom types must not start with &#x60;RC:&#x60; and must not exceed 32 characters. | [default to undefined]
**content** | **string** | Message content payload. Built-in message types should pass a JSON object serialized as a string. Maximum size is 128 KB. | [default to undefined]
**pushContent** | **string** | Push notification text shown to offline recipients. Required for custom message types or notification/signal messages that need push delivery. | [optional] [default to undefined]
**pushData** | **string** | Custom payload included in the push notification. Exposed as &#x60;appData&#x60; on iOS and Android. | [optional] [default to undefined]
**isEchoToSender** | **number** | Whether to sync the message to the sender\&#39;s client while the sender is online. &#x60;1&#x60; enables sync and &#x60;0&#x60; disables it. | [optional] [default to undefined]
**count** | **number** | Aligns with Java &#x60;DirectChannelMsgSendInput.count&#x60; (push/badge-related counter field name in server model). | [optional] [default to undefined]
**verifyBlocklist** | **number** | Whether to filter recipients against the sender\&#39;s blocklist. &#x60;0&#x60; means no filtering and &#x60;1&#x60; means filter blocked users out. | [optional] [default to undefined]
**shouldPersist** | **number** | Whether to store the message in recipient cloud history. &#x60;0&#x60; means do not store and &#x60;1&#x60; means store. | [optional] [default to undefined]
**contentAvailable** | **number** | iOS silent-push flag. &#x60;1&#x60; enables background delivery and &#x60;0&#x60; disables it. | [optional] [default to undefined]
**hasMetadata** | **boolean** | Whether to enable message metadata (message expansion) for this message. | [optional] [default to undefined]
**metadata** | **{ [key: string]: any; }** | Custom message metadata entries. Keys are limited to 32 characters and values to 4096 characters. | [optional] [default to undefined]
**disablePush** | **boolean** | Whether to suppress push notifications for offline recipients. | [optional] [default to undefined]
**pushExt** | **string** | Extended push configuration (JSON string as accepted by &#x60;DirectChannelMsgSendInput&#x60;). | [optional] [default to undefined]
**disableUpdateLastMsg** | **boolean** | Whether to keep this message from updating the channel\&#39;s last-message preview. | [optional] [default to undefined]
**needReadReceipt** | **number** | Whether to request read receipts for this persisted message. &#x60;1&#x60; requests read receipts and &#x60;0&#x60; disables them. | [optional] [default to undefined]

## Example

```typescript
import { DirectChannelMessageSendRequest } from '@nexconn/server-sdk';

const instance: DirectChannelMessageSendRequest = {
    fromUserId,
    toUserIds,
    messageType,
    content,
    pushContent,
    pushData,
    isEchoToSender,
    count,
    verifyBlocklist,
    shouldPersist,
    contentAvailable,
    hasMetadata,
    metadata,
    disablePush,
    pushExt,
    disableUpdateLastMsg,
    needReadReceipt,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
