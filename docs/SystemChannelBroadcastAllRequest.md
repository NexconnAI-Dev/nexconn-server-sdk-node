# SystemChannelBroadcastAllRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fromUserId** | **string** |  | [default to undefined]
**messageType** | **string** |  | [default to undefined]
**content** | **string** |  | [default to undefined]
**pushContent** | **string** |  | [optional] [default to undefined]
**pushData** | **string** |  | [optional] [default to undefined]
**contentAvailable** | **number** |  | [optional] [default to undefined]
**pushExt** | **string** | Extended push configuration (JSON string as accepted by &#x60;MessageBroadcastInput&#x60;). | [optional] [default to undefined]
**disableUpdateLastMsg** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { SystemChannelBroadcastAllRequest } from '@nexconn/server-sdk';

const instance: SystemChannelBroadcastAllRequest = {
    fromUserId,
    messageType,
    content,
    pushContent,
    pushData,
    contentAvailable,
    pushExt,
    disableUpdateLastMsg,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
