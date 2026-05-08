# OpenChannelManagementApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createOpenChannel**](#createopenchannel) | **POST** /v4/open-channel/create | Create an open channel|
|[**destroyOpenChannels**](#destroyopenchannels) | **POST** /v4/open-channel/destroy | Destroy an open channel|
|[**getOpenChannel**](#getopenchannel) | **POST** /v4/open-channel/get | Get open channel info|
|[**setOpenChannelDestroyType**](#setopenchanneldestroytype) | **POST** /v4/open-channel/destroy-type/set | Set auto-destroy type|

# **createOpenChannel**
> CodeOnlyResponse createOpenChannel(openChannelCreateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelManagementApi,
    Configuration,
    OpenChannelCreateRequest
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
const apiInstance = new OpenChannelManagementApi(configuration);

let openChannelCreateRequest: OpenChannelCreateRequest; //

const { status, data } = await apiInstance.createOpenChannel(
    openChannelCreateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelCreateRequest** | **OpenChannelCreateRequest**|  | |


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

# **destroyOpenChannels**
> CodeOnlyResponse destroyOpenChannels(openChannelDestroyRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelManagementApi,
    Configuration,
    OpenChannelDestroyRequest
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
const apiInstance = new OpenChannelManagementApi(configuration);

let openChannelDestroyRequest: OpenChannelDestroyRequest; //

const { status, data } = await apiInstance.destroyOpenChannels(
    openChannelDestroyRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelDestroyRequest** | **OpenChannelDestroyRequest**|  | |


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

# **getOpenChannel**
> OpenChannelGetResponse getOpenChannel(openChannelGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelManagementApi,
    Configuration,
    OpenChannelGetRequest
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
const apiInstance = new OpenChannelManagementApi(configuration);

let openChannelGetRequest: OpenChannelGetRequest; //

const { status, data } = await apiInstance.getOpenChannel(
    openChannelGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelGetRequest** | **OpenChannelGetRequest**|  | |


### Return type

**OpenChannelGetResponse**

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

# **setOpenChannelDestroyType**
> CodeOnlyResponse setOpenChannelDestroyType(openChannelDestroyTypeSetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelManagementApi,
    Configuration,
    OpenChannelDestroyTypeSetRequest
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
const apiInstance = new OpenChannelManagementApi(configuration);

let openChannelDestroyTypeSetRequest: OpenChannelDestroyTypeSetRequest; //

const { status, data } = await apiInstance.setOpenChannelDestroyType(
    openChannelDestroyTypeSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelDestroyTypeSetRequest** | **OpenChannelDestroyTypeSetRequest**|  | |


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

