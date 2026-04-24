# MessageMetadataSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | **string** |  | [default to undefined]
**userId** | **string** |  | [default to undefined]
**channelType** | **number** | Supports &#x60;1&#x60; and &#x60;3&#x60;. | [default to undefined]
**channelId** | **string** |  | [default to undefined]
**metadata** | **{ [key: string]: string; }** | Message metadata to set. Keys support letters, digits, and &#x60;+ &#x3D; - _&#x60;, with a maximum key length of 32 characters. Each request can set up to 100 entries.  | [default to undefined]
**isEchoToSender** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { MessageMetadataSetRequest } from 'nexconn-sdk-node';

const instance: MessageMetadataSetRequest = {
    messageId,
    userId,
    channelType,
    channelId,
    metadata,
    isEchoToSender,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
