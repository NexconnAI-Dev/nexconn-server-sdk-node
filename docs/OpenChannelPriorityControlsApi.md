# OpenChannelPriorityControlsApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addOpenChannelPriorityMessageTypeList**](#addopenchannelprioritymessagetypelist) | **POST** /v4/open-channel/priority-message-type-list/add | Add priority message types|
|[**addOpenChannelPrioritySenderList**](#addopenchannelprioritysenderlist) | **POST** /v4/open-channel/priority-sender-list/add | Add priority senders|
|[**getOpenChannelPriorityMessageTypeList**](#getopenchannelprioritymessagetypelist) | **POST** /v4/open-channel/priority-message-type-list/get | Query priority message types|
|[**getOpenChannelPrioritySenderList**](#getopenchannelprioritysenderlist) | **POST** /v4/open-channel/priority-sender-list/get | Query priority senders|
|[**removeOpenChannelPriorityMessageTypeList**](#removeopenchannelprioritymessagetypelist) | **POST** /v4/open-channel/priority-message-type-list/remove | Remove priority message types|
|[**removeOpenChannelPrioritySenderList**](#removeopenchannelprioritysenderlist) | **POST** /v4/open-channel/priority-sender-list/remove | Remove priority senders|

# **addOpenChannelPriorityMessageTypeList**
> CodeOnlyResponse addOpenChannelPriorityMessageTypeList(openChannelPriorityMessageTypeListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelPriorityControlsApi,
    Configuration,
    OpenChannelPriorityMessageTypeListRequest
} from 'nexconn-sdk-node';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new OpenChannelPriorityControlsApi(configuration);

let openChannelPriorityMessageTypeListRequest: OpenChannelPriorityMessageTypeListRequest; //

const { status, data } = await apiInstance.addOpenChannelPriorityMessageTypeList(
    openChannelPriorityMessageTypeListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelPriorityMessageTypeListRequest** | **OpenChannelPriorityMessageTypeListRequest**|  | |


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

# **addOpenChannelPrioritySenderList**
> CodeOnlyResponse addOpenChannelPrioritySenderList(openChannelParticipantIdsRequest)

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/priority-sender-list/add`.

### Example

```typescript
import {
    OpenChannelPriorityControlsApi,
    Configuration,
    OpenChannelParticipantIdsRequest
} from 'nexconn-sdk-node';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new OpenChannelPriorityControlsApi(configuration);

let openChannelParticipantIdsRequest: OpenChannelParticipantIdsRequest; //

const { status, data } = await apiInstance.addOpenChannelPrioritySenderList(
    openChannelParticipantIdsRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantIdsRequest** | **OpenChannelParticipantIdsRequest**|  | |


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

# **getOpenChannelPriorityMessageTypeList**
> OpenChannelMessageTypeListResponse getOpenChannelPriorityMessageTypeList()

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelPriorityControlsApi,
    Configuration
} from 'nexconn-sdk-node';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new OpenChannelPriorityControlsApi(configuration);
const { status, data } = await apiInstance.getOpenChannelPriorityMessageTypeList();

```

### Parameters
This endpoint does not require a request body.

### Return type

**OpenChannelMessageTypeListResponse**

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

# **getOpenChannelPrioritySenderList**
> OpenChannelParticipantIdsResponse getOpenChannelPrioritySenderList(openChannelParticipantListByChannelRequest)

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/priority-sender-list/get`.

### Example

```typescript
import {
    OpenChannelPriorityControlsApi,
    Configuration,
    OpenChannelParticipantListByChannelRequest
} from 'nexconn-sdk-node';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new OpenChannelPriorityControlsApi(configuration);

let openChannelParticipantListByChannelRequest: OpenChannelParticipantListByChannelRequest; //

const { status, data } = await apiInstance.getOpenChannelPrioritySenderList(
    openChannelParticipantListByChannelRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantListByChannelRequest** | **OpenChannelParticipantListByChannelRequest**|  | |


### Return type

**OpenChannelParticipantIdsResponse**

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

# **removeOpenChannelPriorityMessageTypeList**
> CodeOnlyResponse removeOpenChannelPriorityMessageTypeList(openChannelPriorityMessageTypeListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelPriorityControlsApi,
    Configuration,
    OpenChannelPriorityMessageTypeListRequest
} from 'nexconn-sdk-node';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new OpenChannelPriorityControlsApi(configuration);

let openChannelPriorityMessageTypeListRequest: OpenChannelPriorityMessageTypeListRequest; //

const { status, data } = await apiInstance.removeOpenChannelPriorityMessageTypeList(
    openChannelPriorityMessageTypeListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelPriorityMessageTypeListRequest** | **OpenChannelPriorityMessageTypeListRequest**|  | |


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

# **removeOpenChannelPrioritySenderList**
> CodeOnlyResponse removeOpenChannelPrioritySenderList(openChannelParticipantIdsRequest)

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/priority-sender-list/remove`.

### Example

```typescript
import {
    OpenChannelPriorityControlsApi,
    Configuration,
    OpenChannelParticipantIdsRequest
} from 'nexconn-sdk-node';

const configuration = new Configuration();
configuration.setRongCloudCredentials(
    process.env.RONGCLOUD_APP_KEY!,
    process.env.RONGCLOUD_APP_SECRET!,
);
configuration.setPrimaryBackupDomains(
    process.env.RONGCLOUD_PRIMARY_API_DOMAIN!,
    process.env.RONGCLOUD_SECONDARY_API_DOMAIN!,
);
const apiInstance = new OpenChannelPriorityControlsApi(configuration);

let openChannelParticipantIdsRequest: OpenChannelParticipantIdsRequest; //

const { status, data } = await apiInstance.removeOpenChannelPrioritySenderList(
    openChannelParticipantIdsRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantIdsRequest** | **OpenChannelParticipantIdsRequest**|  | |


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

