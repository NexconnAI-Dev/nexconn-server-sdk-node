# CommunityChannelMessageMetadataSetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messageId** | **string** |  | [default to undefined]
**userId** | **string** |  | [default to undefined]
**channelId** | **string** |  | [default to undefined]
**subchannelId** | **string** |  | [optional] [default to undefined]
**metadata** | **{ [key: string]: string; }** | Community-channel message metadata to set. Keys support letters, digits, and &#x60;+ &#x3D; - _&#x60;, with a maximum key length of 32 characters. Each request can set up to 20 entries.  | [default to undefined]

## Example

```typescript
import { CommunityChannelMessageMetadataSetRequest } from '@nexconn/server-sdk';

const instance: CommunityChannelMessageMetadataSetRequest = {
    messageId,
    userId,
    channelId,
    subchannelId,
    metadata,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
