# CommunityChannelMessageMetadataListRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | **string** |  | [default to undefined]
**channelId** | **string** |  | [default to undefined]
**subchannelId** | **string** | Should match the subchannel used when the message was sent. | [optional] [default to undefined]
**page** | **number** |  | [optional] [default to undefined]

## Example

```typescript
import { CommunityChannelMessageMetadataListRequest } from '@nexconn/server-sdk';

const instance: CommunityChannelMessageMetadataListRequest = {
    messageId,
    channelId,
    subchannelId,
    page,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
