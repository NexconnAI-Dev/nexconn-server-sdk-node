# OpenChannelHistoryMessageRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | Channel identifier of the stored message. | [optional] [default to undefined]
**fromUserId** | **string** | Sender user ID of the stored message. | [optional] [default to undefined]
**messageId** | **string** | Unique message ID. | [optional] [default to undefined]
**sentAt** | **number** | Message send timestamp in milliseconds. | [optional] [default to undefined]
**messageType** | **string** | Message type of the stored message. | [optional] [default to undefined]
**content** | **string** | Raw message content payload as stored by the service. | [optional] [default to undefined]
**quote** | **string** | Quoted message details as a JSON string containing msgUID, objectName and fromUserId. Omitted for messages without a quote. | [optional] [default to undefined]

## Example

```typescript
import { OpenChannelHistoryMessageRecord } from '@nexconn/server-sdk';

const instance: OpenChannelHistoryMessageRecord = {
    channelId,
    fromUserId,
    messageId,
    sentAt,
    messageType,
    content,
    quote,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
