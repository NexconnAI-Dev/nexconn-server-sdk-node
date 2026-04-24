# CommunitySubchannelCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [default to undefined]
**subchannelId** | **string** | Legacy &#x60;busChannel&#x60;. | [default to undefined]
**channelVisibility** | **number** | Legacy &#x60;type&#x60;. &#x60;0&#x60; for public and &#x60;1&#x60; for private. | [optional] [default to undefined]

## Example

```typescript
import { CommunitySubchannelCreateRequest } from 'nexconn-sdk-node';

const instance: CommunitySubchannelCreateRequest = {
    channelId,
    subchannelId,
    channelVisibility,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
