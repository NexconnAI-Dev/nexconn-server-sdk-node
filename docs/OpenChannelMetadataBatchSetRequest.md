# OpenChannelMetadataBatchSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [default to undefined]
**metadataOwnerId** | **string** | Legacy &#x60;entryOwnerId&#x60;. | [default to undefined]
**metadata** | **{ [key: string]: string; }** | Legacy &#x60;entryInfo&#x60;. Up to 20 metadata entries per request. | [default to undefined]
**shouldAutoDelete** | **number** | &#x60;0&#x60; keeps metadata after the owner leaves and &#x60;1&#x60; removes it automatically. | [optional] [default to undefined]

## Example

```typescript
import { OpenChannelMetadataBatchSetRequest } from '@nexconn/server-sdk';

const instance: OpenChannelMetadataBatchSetRequest = {
    channelId,
    metadataOwnerId,
    metadata,
    shouldAutoDelete,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
