# StreamMessageContent

Stream message content payload.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | **string** | Stream data chunk. Total message size must not exceed 128 KB across all chunks. | [default to undefined]
**seq** | **number** | Sequence number. Must be greater than 0, starting from 1, strictly incrementing and continuous. | [default to undefined]
**complete** | **boolean** | Whether this is the final chunk in the stream. &#x60;true&#x60; marks the end of the stream. | [default to undefined]
**completeReason** | **number** | Custom completion reason code. Only effective when &#x60;complete&#x60; is &#x60;true&#x60;. | [optional] [default to undefined]
**type** | **string** | Stream content type. Supported on the first chunk only. Default: text. Supported values: text, markdown, html. | [optional] [default to undefined]
**messageId** | **string** | Stream message unique ID. Not required for the first chunk. Required for subsequent chunks (use the value returned in the first chunk response). | [optional] [default to undefined]
**user** | **{ [key: string]: any; }** | Sender user information object. Supported on the first chunk only. | [optional] [default to undefined]
**mentionedInfo** | **{ [key: string]: any; }** | @mention information. Supported on the first chunk only. | [optional] [default to undefined]
**extra** | **{ [key: string]: any; }** | Extension information. Supported on the first chunk only. | [optional] [default to undefined]

## Example

```typescript
import { StreamMessageContent } from '@nexconn/server-sdk';

const instance: StreamMessageContent = {
    content,
    seq,
    complete,
    completeReason,
    type,
    messageId,
    user,
    mentionedInfo,
    extra,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
