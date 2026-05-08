# CommunityChannelHistoryMessageListRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [default to undefined]
**subchannelId** | **string** |  | [default to undefined]
**startAt** | **number** |  | [default to undefined]
**endAt** | **number** |  | [default to undefined]
**fromUserId** | **string** |  | [optional] [default to undefined]
**pageSize** | **number** |  | [optional] [default to 20]

## Example

```typescript
import { CommunityChannelHistoryMessageListRequest } from '@nexconn/server-sdk';

const instance: CommunityChannelHistoryMessageListRequest = {
    channelId,
    subchannelId,
    startAt,
    endAt,
    fromUserId,
    pageSize,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
