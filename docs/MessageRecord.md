# MessageRecord


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | Channel identifier of the stored message. | [optional] [default to undefined]
**subchannelId** | **string** | Community subchannel ID associated with the stored message, when applicable. | [optional] [default to undefined]
**fromUserId** | **string** | Sender user ID of the stored message. | [optional] [default to undefined]
**messageId** | **string** | Unique message ID. | [optional] [default to undefined]
**sentAt** | **number** | Message send timestamp in milliseconds. | [optional] [default to undefined]
**messageType** | **string** | Message type of the stored message. | [optional] [default to undefined]
**content** | **string** | Raw message content payload as stored by the service. | [optional] [default to undefined]
**hasMetadata** | **boolean** | Whether the message has metadata entries attached. | [optional] [default to undefined]
**metadata** | [**Array&lt;MessageMetadataListItem&gt;**](MessageMetadataListItem.md) | Structured message metadata entries. Omitted when the original metadata is empty or cannot be parsed. | [optional] [default to undefined]
**quote** | **string** | Quoted message details as a JSON string containing msgUID, objectName and fromUserId. Omitted for messages without a quote. | [optional] [default to undefined]

## Example

```typescript
import { MessageRecord } from '@nexconn/server-sdk';

const instance: MessageRecord = {
    channelId,
    subchannelId,
    fromUserId,
    messageId,
    sentAt,
    messageType,
    content,
    hasMetadata,
    metadata,
    quote,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
