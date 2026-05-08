# OpenChannelMetadataBatchGetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [default to undefined]
**metadataKeys** | **Array&lt;string&gt;** | Metadata keys to fetch. When omitted, the service returns metadata according to its default rule. | [optional] [default to undefined]

## Example

```typescript
import { OpenChannelMetadataBatchGetRequest } from '@nexconn/server-sdk';

const instance: OpenChannelMetadataBatchGetRequest = {
    channelId,
    metadataKeys,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
