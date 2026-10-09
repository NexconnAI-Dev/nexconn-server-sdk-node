# CommunityChannelHistoryMessageListRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | Community channel ID. | [default to undefined]
**subchannelId** | **string** | Optional community subchannel ID. When omitted, messages from the whole community channel are queried. | [optional] [default to undefined]
**userId** | **string** | User ID of the community-channel participant. | [default to undefined]
**startAt** | **number** | Query start timestamp in Unix milliseconds. Must be greater than or equal to &#x60;endAt&#x60;; the range cannot exceed 14 days. | [default to undefined]
**endAt** | **number** | Query end timestamp in Unix milliseconds. Messages are returned in descending timestamp order. | [default to undefined]
**pageSize** | **number** | Number of messages to return. Must be between 1 and 100. | [optional] [default to 10]
**includeStart** | **boolean** | Whether to include the message at &#x60;startAt&#x60; when it matches the query boundary. | [default to undefined]

## Example

```typescript
import { CommunityChannelHistoryMessageListRequest } from '@nexconn/server-sdk';

const instance: CommunityChannelHistoryMessageListRequest = {
    channelId,
    subchannelId,
    userId,
    startAt,
    endAt,
    pageSize,
    includeStart,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
