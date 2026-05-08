# GroupChannelQuitRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [default to undefined]
**userIds** | **Array&lt;string&gt;** |  | [default to undefined]
**shouldDeleteMute** | **number** | &#x60;0&#x60; means keep each leaving member\&#39;s mute state and &#x60;1&#x60; means remove it. | [optional] [default to undefined]
**shouldDeleteAllowedSendersList** | **number** | &#x60;0&#x60; means keep each leaving member\&#39;s allowed-senders-list state and &#x60;1&#x60; means remove it. | [optional] [default to undefined]
**shouldDeleteFavorites** | **number** | &#x60;0&#x60; means keep each leaving member\&#39;s favorites record and &#x60;1&#x60; means remove it. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelQuitRequest } from '@nexconn/server-sdk';

const instance: GroupChannelQuitRequest = {
    channelId,
    userIds,
    shouldDeleteMute,
    shouldDeleteAllowedSendersList,
    shouldDeleteFavorites,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
