# CommunityChannelMessageMetadataDeleteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | **string** |  | [default to undefined]
**userId** | **string** |  | [default to undefined]
**channelId** | **string** |  | [default to undefined]
**subchannelId** | **string** | Should match the subchannel used when the message was sent. | [optional] [default to undefined]
**keys** | **Array&lt;string&gt;** |  | [default to undefined]

## Example

```typescript
import { CommunityChannelMessageMetadataDeleteRequest } from 'nexconn-sdk-node';

const instance: CommunityChannelMessageMetadataDeleteRequest = {
    messageId,
    userId,
    channelId,
    subchannelId,
    keys,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
