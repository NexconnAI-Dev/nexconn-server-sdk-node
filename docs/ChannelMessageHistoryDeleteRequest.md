# ChannelMessageHistoryDeleteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelType** | **number** | Channel type. Supports &#x60;1&#x60; direct, &#x60;3&#x60; group, &#x60;4&#x60; open channel, and &#x60;6&#x60; system (&#x60;HistoryCleanInput&#x60;). | [default to undefined]
**fromUserId** | **string** | User whose server-side history is operated on. For open channels, this is the operator ID. | [default to undefined]
**channelId** | **string** | Target channel ID (&#x60;targetId&#x60; / conversation target). | [default to undefined]
**sentAt** | **string** | Optional cutoff (&#x60;msgTimestamp&#x60;). Serialized as string in &#x60;HistoryCleanInput&#x60;. | [optional] [default to undefined]

## Example

```typescript
import { ChannelMessageHistoryDeleteRequest } from 'nexconn-sdk-node';

const instance: ChannelMessageHistoryDeleteRequest = {
    channelType,
    fromUserId,
    channelId,
    sentAt,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
