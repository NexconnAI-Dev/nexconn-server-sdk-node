# MessageDeleteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromUserId** | **string** | Sender user ID of the original message that is being deleted. | [default to undefined]
**channelType** | **number** | Channel type of the original message. Supports &#x60;1&#x60; direct, &#x60;3&#x60; group, &#x60;4&#x60; open channel, &#x60;6&#x60; system, and &#x60;10&#x60; community. | [default to undefined]
**channelId** | **string** | Target identifier of the original message. Depending on &#x60;channelType&#x60;, this can be a user ID, group ID, open channel ID, community channel ID, or system target ID. | [default to undefined]
**subchannelId** | **string** | Community subchannel ID. Required only when deleting a community-channel message that was sent to a specific subchannel. | [optional] [default to undefined]
**messageId** | **string** | Unique message ID to delete. This corresponds to the message UID returned by send or routing services. | [default to undefined]
**sentAt** | **number** | Send timestamp of the original message in milliseconds. Providing it helps the service locate the original message precisely. | [optional] [default to undefined]
**isAdmin** | **number** | Whether the deletion is performed as an admin operation. &#x60;1&#x60; shows an admin recall indicator and &#x60;0&#x60; performs a normal sender recall. | [optional] [default to undefined]
**disablePush** | **boolean** | Whether to suppress push notifications for the recall event. Not supported for open channels or community channels. | [optional] [default to undefined]
**extra** | **string** | Custom extension data carried with the recall operation. Not supported for community channels. | [optional] [default to undefined]
**disableUpdateLastMsg** | **boolean** | Whether to keep the recall operation from updating the channel\&#39;s last-message preview. | [optional] [default to undefined]

## Example

```typescript
import { MessageDeleteRequest } from 'nexconn-sdk-node';

const instance: MessageDeleteRequest = {
    fromUserId,
    channelType,
    channelId,
    subchannelId,
    messageId,
    sentAt,
    isAdmin,
    disablePush,
    extra,
    disableUpdateLastMsg,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
