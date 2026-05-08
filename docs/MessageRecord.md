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
**channelType** | **number** | Channel type of the stored message. | [optional] [default to undefined]
**content** | **string** | Raw message content payload as stored by the service. | [optional] [default to undefined]
**hasMetadata** | **boolean** | Whether the message has metadata entries attached. | [optional] [default to undefined]
**metadata** | [**Array&lt;MessageMetadataListItem&gt;**](MessageMetadataListItem.md) | List of metadata entries (&#x60;CommunityHistoryMessage&#x60; uses &#x60;List&lt;MetadataItem&gt;&#x60;, not a map). | [optional] [default to undefined]

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
    channelType,
    content,
    hasMetadata,
    metadata,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
