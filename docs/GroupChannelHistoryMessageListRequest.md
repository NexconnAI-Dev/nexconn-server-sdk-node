# GroupChannelHistoryMessageListRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** | User ID of the group-channel participant. | [default to undefined]
**channelId** | **string** | Group channel ID. | [default to undefined]
**startAt** | **number** | Query start timestamp in Unix milliseconds. Must be greater than or equal to &#x60;endAt&#x60;; the range cannot exceed 14 days. | [default to undefined]
**endAt** | **number** | Query end timestamp in Unix milliseconds. Messages are returned in descending timestamp order. | [default to undefined]
**pageSize** | **number** | Number of messages to return. Must be between 1 and 100. | [optional] [default to 10]
**includeStart** | **boolean** | Whether to include the message at &#x60;startAt&#x60; when it matches the query boundary. | [default to undefined]

## Example

```typescript
import { GroupChannelHistoryMessageListRequest } from '@nexconn/server-sdk';

const instance: GroupChannelHistoryMessageListRequest = {
    userId,
    channelId,
    startAt,
    endAt,
    pageSize,
    includeStart,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
