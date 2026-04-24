# OpenChannelCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | Legacy &#x60;chatroomId&#x60;. | [default to undefined]
**destroyType** | **number** | \&#39;0\&#39; for inactive-time destroy and \&#39;1\&#39; for fixed-time destroy. | [optional] [default to undefined]
**ttlMinutes** | **number** | Legacy &#x60;destroyTime&#x60;. Valid range is 60 to 10080 minutes according to the PDF. | [optional] [default to undefined]
**shouldFreeze** | **boolean** | Whether whole-channel freeze is enabled when the chatroom is created. | [optional] [default to undefined]
**allowedSendersList** | **Array&lt;string&gt;** | Allowed senders list applied when the chatroom is frozen. | [optional] [default to undefined]
**metadataOwnerId** | **string** | Legacy &#x60;entryOwnerId&#x60;. | [optional] [default to undefined]
**metadata** | **{ [key: string]: string; }** | Legacy &#x60;entryInfo&#x60;. Open-channel metadata key/value pairs. | [optional] [default to undefined]

## Example

```typescript
import { OpenChannelCreateRequest } from 'nexconn-sdk-node';

const instance: OpenChannelCreateRequest = {
    channelId,
    destroyType,
    ttlMinutes,
    shouldFreeze,
    allowedSendersList,
    metadataOwnerId,
    metadata,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
