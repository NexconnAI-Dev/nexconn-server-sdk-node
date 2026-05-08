# GroupChannelTransferOwnerRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** |  | [default to undefined]
**newOwner** | **string** |  | [default to undefined]
**shouldLeave** | **number** | &#x60;0&#x60; means keep the previous owner in the group and &#x60;1&#x60; means leave the group. | [optional] [default to undefined]
**shouldDeleteMute** | **number** | &#x60;0&#x60; means keep the previous owner\&#39;s mute state and &#x60;1&#x60; means remove it. | [optional] [default to undefined]
**shouldDeleteAllowedSendersList** | **number** | &#x60;0&#x60; means keep the previous owner\&#39;s allowed-senders-list state and &#x60;1&#x60; means remove it. | [optional] [default to undefined]
**shouldDeleteFavorites** | **number** | &#x60;0&#x60; means keep favorites and &#x60;1&#x60; means remove them. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelTransferOwnerRequest } from '@nexconn/server-sdk';

const instance: GroupChannelTransferOwnerRequest = {
    channelId,
    newOwner,
    shouldLeave,
    shouldDeleteMute,
    shouldDeleteAllowedSendersList,
    shouldDeleteFavorites,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
