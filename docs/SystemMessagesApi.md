# SystemMessagesApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**broadcastMessageOnline**](#broadcastmessageonline) | **POST** /v4/system-channel/message/broadcast-online | Broadcast to online users|
|[**broadcastSystemChannelMessage**](#broadcastsystemchannelmessage) | **POST** /v4/system-channel/message/broadcast-all | Broadcast to all users (persistent)|
|[**deleteBroadcastMessage**](#deletebroadcastmessage) | **POST** /v4/system-channel/message/broadcast/delete | Recall broadcast to all users|
|[**sendSystemChannelMessage**](#sendsystemchannelmessage) | **POST** /v4/system-channel/message/send | Send a system message|
|[**sendSystemChannelPushByPackage**](#sendsystemchannelpushbypackage) | **POST** /v4/system-channel/app-package-users/send | Push by app package name|
|[**sendSystemChannelPushByTag**](#sendsystemchannelpushbytag) | **POST** /v4/system-channel/tagged-users/send | Push to tagged users|

# **broadcastMessageOnline**
> SingleMessageIdResponse broadcastMessageOnline(systemChannelBroadcastOnlineRequest)

Rate limit: 60/min.

### Example

```typescript
import {
    SystemMessagesApi,
    Configuration,
    SystemChannelBroadcastOnlineRequest
} from '@nexconn/server-sdk';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new SystemMessagesApi(configuration);

let systemChannelBroadcastOnlineRequest: SystemChannelBroadcastOnlineRequest; //

const { status, data } = await apiInstance.broadcastMessageOnline(
    systemChannelBroadcastOnlineRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **systemChannelBroadcastOnlineRequest** | **SystemChannelBroadcastOnlineRequest**|  | |


### Return type

**SingleMessageIdResponse**

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **broadcastSystemChannelMessage**
> SingleMessageIdResponse broadcastSystemChannelMessage(systemChannelBroadcastAllRequest)

Rate limit: 2/hour, 3/day.

### Example

```typescript
import {
    SystemMessagesApi,
    Configuration,
    SystemChannelBroadcastAllRequest
} from '@nexconn/server-sdk';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new SystemMessagesApi(configuration);

let systemChannelBroadcastAllRequest: SystemChannelBroadcastAllRequest; //

const { status, data } = await apiInstance.broadcastSystemChannelMessage(
    systemChannelBroadcastAllRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **systemChannelBroadcastAllRequest** | **SystemChannelBroadcastAllRequest**|  | |


### Return type

**SingleMessageIdResponse**

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteBroadcastMessage**
> CodeOnlyResponse deleteBroadcastMessage(systemChannelBroadcastDeleteRequest)

Rate limit: 2/hour, 3/day.

### Example

```typescript
import {
    SystemMessagesApi,
    Configuration,
    SystemChannelBroadcastDeleteRequest
} from '@nexconn/server-sdk';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new SystemMessagesApi(configuration);

let systemChannelBroadcastDeleteRequest: SystemChannelBroadcastDeleteRequest; //

const { status, data } = await apiInstance.deleteBroadcastMessage(
    systemChannelBroadcastDeleteRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **systemChannelBroadcastDeleteRequest** | **SystemChannelBroadcastDeleteRequest**|  | |


### Return type

**CodeOnlyResponse**

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sendSystemChannelMessage**
> UserMessageSendResponse sendSystemChannelMessage(systemChannelMessageSendRequest)

Rate limit: 100 msgs/sec (by recipient count).

### Example

```typescript
import {
    SystemMessagesApi,
    Configuration,
    SystemChannelMessageSendRequest
} from '@nexconn/server-sdk';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new SystemMessagesApi(configuration);

let systemChannelMessageSendRequest: SystemChannelMessageSendRequest; //

const { status, data } = await apiInstance.sendSystemChannelMessage(
    systemChannelMessageSendRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **systemChannelMessageSendRequest** | **SystemChannelMessageSendRequest**|  | |


### Return type

**UserMessageSendResponse**

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sendSystemChannelPushByPackage**
> SystemChannelPushResponse sendSystemChannelPushByPackage(systemChannelPushRequest)

Rate limit: 2/hour, 3/day (shared).

### Example

```typescript
import {
    SystemMessagesApi,
    Configuration,
    SystemChannelPushRequest
} from '@nexconn/server-sdk';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new SystemMessagesApi(configuration);

let systemChannelPushRequest: SystemChannelPushRequest; //

const { status, data } = await apiInstance.sendSystemChannelPushByPackage(
    systemChannelPushRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **systemChannelPushRequest** | **SystemChannelPushRequest**|  | |


### Return type

**SystemChannelPushResponse**

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sendSystemChannelPushByTag**
> SystemChannelPushResponse sendSystemChannelPushByTag(systemChannelPushRequest)

Rate limit: 2/hour, 3/day (shared).

### Example

```typescript
import {
    SystemMessagesApi,
    Configuration,
    SystemChannelPushRequest
} from '@nexconn/server-sdk';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new SystemMessagesApi(configuration);

let systemChannelPushRequest: SystemChannelPushRequest; //

const { status, data } = await apiInstance.sendSystemChannelPushByTag(
    systemChannelPushRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **systemChannelPushRequest** | **SystemChannelPushRequest**|  | |


### Return type

**SystemChannelPushResponse**

### Authorization

[NexconnSignature](../README.md#NexconnSignature)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

