# SystemChannelPushRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Array&lt;string&gt;** |  | [default to undefined]
**fromUserId** | **string** |  | [default to undefined]
**audience** | [**SystemChannelPushAudience**](SystemChannelPushAudience.md) |  | [default to undefined]
**message** | [**SystemChannelPushMessage**](SystemChannelPushMessage.md) |  | [default to undefined]
**notification** | [**SystemChannelPushNotification**](SystemChannelPushNotification.md) |  | [default to undefined]

## Example

```typescript
import { SystemChannelPushRequest } from '@nexconn/server-sdk';

const instance: SystemChannelPushRequest = {
    platform,
    fromUserId,
    audience,
    message,
    notification,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
