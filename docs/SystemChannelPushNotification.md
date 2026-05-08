# SystemChannelPushNotification


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** |  | [optional] [default to undefined]
**forceShowPushContent** | **number** |  | [optional] [default to undefined]
**alert** | **string** |  | [optional] [default to undefined]
**ios** | **{ [key: string]: any; }** |  | [optional] [default to undefined]
**android** | **{ [key: string]: any; }** |  | [optional] [default to undefined]
**harmonyOS** | **{ [key: string]: any; }** |  | [optional] [default to undefined]

## Example

```typescript
import { SystemChannelPushNotification } from '@nexconn/server-sdk';

const instance: SystemChannelPushNotification = {
    title,
    forceShowPushContent,
    alert,
    ios,
    android,
    harmonyOS,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
