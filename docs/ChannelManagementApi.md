# ChannelManagementApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addTagToChannels**](#addtagtochannels) | **POST** /v4/channel/tag/add | Add tag to channel|
|[**addUserChannelTags**](#adduserchanneltags) | **POST** /v4/user/channel/tag/add | Add user channel tag|
|[**getChannelAttribute**](#getchannelattribute) | **POST** /v4/channel/attribute/get | Get channel attributes|
|[**getChannelPushNotification**](#getchannelpushnotification) | **POST** /v4/channel/push/get | Get channel DND|
|[**getChannelTypeNotification**](#getchanneltypenotification) | **POST** /v4/channel-type/push/get | Get DND by channel type|
|[**listChannelsByTag**](#listchannelsbytag) | **POST** /v4/channel/tag/list | Get channels by tag|
|[**listUserChannelTags**](#listuserchanneltags) | **POST** /v4/user/channel/tag/list | List user channel tags|
|[**removeTagFromChannels**](#removetagfromchannels) | **POST** /v4/channel/tag/delete | Remove tag from channel|
|[**removeUserChannelTags**](#removeuserchanneltags) | **POST** /v4/user/channel/tag/remove | Remove user channel tag|
|[**setChannelPin**](#setchannelpin) | **POST** /v4/channel/pin/set | Pin a channel|
|[**setChannelPushNotification**](#setchannelpushnotification) | **POST** /v4/channel/push/set | Set channel DND|
|[**setChannelTypeNotification**](#setchanneltypenotification) | **POST** /v4/channel-type/push/set | Set DND by channel type|

# **addTagToChannels**
> CodeOnlyResponse addTagToChannels(channelTagAddRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    ChannelTagAddRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let channelTagAddRequest: ChannelTagAddRequest; //

const { status, data } = await apiInstance.addTagToChannels(
    channelTagAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelTagAddRequest** | **ChannelTagAddRequest**|  | |


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

# **addUserChannelTags**
> CodeOnlyResponse addUserChannelTags(userChannelTagAddRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    UserChannelTagAddRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let userChannelTagAddRequest: UserChannelTagAddRequest; //

const { status, data } = await apiInstance.addUserChannelTags(
    userChannelTagAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userChannelTagAddRequest** | **UserChannelTagAddRequest**|  | |


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

# **getChannelAttribute**
> ChannelAttributeGetResponse getChannelAttribute(channelAttributeGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    ChannelAttributeGetRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let channelAttributeGetRequest: ChannelAttributeGetRequest; //

const { status, data } = await apiInstance.getChannelAttribute(
    channelAttributeGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelAttributeGetRequest** | **ChannelAttributeGetRequest**|  | |


### Return type

**ChannelAttributeGetResponse**

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

# **getChannelPushNotification**
> ChannelPushGetResponse getChannelPushNotification(channelPushGetRequest)

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/channel/notification/get`.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    ChannelPushGetRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let channelPushGetRequest: ChannelPushGetRequest; //

const { status, data } = await apiInstance.getChannelPushNotification(
    channelPushGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelPushGetRequest** | **ChannelPushGetRequest**|  | |


### Return type

**ChannelPushGetResponse**

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

# **getChannelTypeNotification**
> ChannelTypeNotificationGetResponse getChannelTypeNotification(channelTypeNotificationGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    ChannelTypeNotificationGetRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let channelTypeNotificationGetRequest: ChannelTypeNotificationGetRequest; //

const { status, data } = await apiInstance.getChannelTypeNotification(
    channelTypeNotificationGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelTypeNotificationGetRequest** | **ChannelTypeNotificationGetRequest**|  | |


### Return type

**ChannelTypeNotificationGetResponse**

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

# **listChannelsByTag**
> ChannelTagListResponse listChannelsByTag(channelTagListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    ChannelTagListRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let channelTagListRequest: ChannelTagListRequest; //

const { status, data } = await apiInstance.listChannelsByTag(
    channelTagListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelTagListRequest** | **ChannelTagListRequest**|  | |


### Return type

**ChannelTagListResponse**

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

# **listUserChannelTags**
> UserChannelTagListResponse listUserChannelTags(userChannelTagListRequest)


### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    UserChannelTagListRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let userChannelTagListRequest: UserChannelTagListRequest; //

const { status, data } = await apiInstance.listUserChannelTags(
    userChannelTagListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userChannelTagListRequest** | **UserChannelTagListRequest**|  | |


### Return type

**UserChannelTagListResponse**

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

# **removeTagFromChannels**
> CodeOnlyResponse removeTagFromChannels(channelTagRemoveRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    ChannelTagRemoveRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let channelTagRemoveRequest: ChannelTagRemoveRequest; //

const { status, data } = await apiInstance.removeTagFromChannels(
    channelTagRemoveRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelTagRemoveRequest** | **ChannelTagRemoveRequest**|  | |


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

# **removeUserChannelTags**
> CodeOnlyResponse removeUserChannelTags(userChannelTagRemoveRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    UserChannelTagRemoveRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let userChannelTagRemoveRequest: UserChannelTagRemoveRequest; //

const { status, data } = await apiInstance.removeUserChannelTags(
    userChannelTagRemoveRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userChannelTagRemoveRequest** | **UserChannelTagRemoveRequest**|  | |


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

# **setChannelPin**
> CodeOnlyResponse setChannelPin(channelPinSetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    ChannelPinSetRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let channelPinSetRequest: ChannelPinSetRequest; //

const { status, data } = await apiInstance.setChannelPin(
    channelPinSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelPinSetRequest** | **ChannelPinSetRequest**|  | |


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

# **setChannelPushNotification**
> CodeOnlyResponse setChannelPushNotification(channelPushSetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    ChannelPushSetRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let channelPushSetRequest: ChannelPushSetRequest; //

const { status, data } = await apiInstance.setChannelPushNotification(
    channelPushSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelPushSetRequest** | **ChannelPushSetRequest**|  | |


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

# **setChannelTypeNotification**
> CodeOnlyResponse setChannelTypeNotification(channelTypeNotificationSetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    ChannelManagementApi,
    Configuration,
    ChannelTypeNotificationSetRequest
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
const apiInstance = new ChannelManagementApi(configuration);

let channelTypeNotificationSetRequest: ChannelTypeNotificationSetRequest; //

const { status, data } = await apiInstance.setChannelTypeNotification(
    channelTypeNotificationSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelTypeNotificationSetRequest** | **ChannelTypeNotificationSetRequest**|  | |


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

