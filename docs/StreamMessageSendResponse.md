# StreamMessageSendResponse

Response for stream message send. The `result` field is only present in the response to the first chunk.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **number** |  | [default to undefined]
**result** | [**StreamMessageSendResponseResult**](StreamMessageSendResponseResult.md) |  | [optional] [default to undefined]

## Example

```typescript
import { StreamMessageSendResponse } from '@nexconn/server-sdk';

const instance: StreamMessageSendResponse = {
    code,
    result,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
