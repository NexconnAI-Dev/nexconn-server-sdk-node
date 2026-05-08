# CommunityChannelFreezeListGetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [default to undefined]
**subchannelId** | **string** |  | [optional] [default to undefined]
**page** | **number** | Pagination field from &#x60;CommunityAllowedSenderListInput&#x60; / &#x60;AbstractCommunityPagingInput&#x60; (present in Java model; not all server code paths consume it). | [optional] [default to 1]
**pageSize** | **number** |  | [optional] [default to 50]

## Example

```typescript
import { CommunityChannelFreezeListGetRequest } from '@nexconn/server-sdk';

const instance: CommunityChannelFreezeListGetRequest = {
    channelId,
    subchannelId,
    page,
    pageSize,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
