# OpenChannelMetadataEntry


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **string** |  | [optional] [default to undefined]
**value** | **string** |  | [optional] [default to undefined]
**metadataOwnerId** | **string** | KV entry owner; serializes as &#x60;metadataOwnerId&#x60; from the source map key &#x60;userId&#x60; (&#x60;OpenChannelMetadataListResult.MetadataItem&#x60;). | [optional] [default to undefined]
**shouldAutoDelete** | **number** | Parsed from source &#x60;autoDelete&#x60; string. &#x60;1&#x60; enables auto-delete and &#x60;0&#x60; disables it. | [optional] [default to undefined]
**updatedAt** | **number** | Parsed from source &#x60;lastSetTime&#x60; (milliseconds). | [optional] [default to undefined]

## Example

```typescript
import { OpenChannelMetadataEntry } from '@nexconn/server-sdk';

const instance: OpenChannelMetadataEntry = {
    key,
    value,
    metadataOwnerId,
    shouldAutoDelete,
    updatedAt,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
