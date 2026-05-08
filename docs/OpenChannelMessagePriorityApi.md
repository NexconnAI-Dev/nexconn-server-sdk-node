# OpenChannelMessagePriorityApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addOpenChannelLowPriorityMessageTypeList**](#addopenchannellowprioritymessagetypelist) | **POST** /v4/open-channel/low-priority-message-type-list/add | Add low-priority message types|
|[**getOpenChannelLowPriorityMessageTypeList**](#getopenchannellowprioritymessagetypelist) | **POST** /v4/open-channel/low-priority-message-type-list/get | Query low-priority message types|
|[**removeOpenChannelLowPriorityMessageTypeList**](#removeopenchannellowprioritymessagetypelist) | **POST** /v4/open-channel/low-priority-message-type-list/remove | Remove low-priority message types|

# **addOpenChannelLowPriorityMessageTypeList**
> CodeOnlyResponse addOpenChannelLowPriorityMessageTypeList(openChannelLowPriorityMessageTypeListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelMessagePriorityApi,
    Configuration,
    OpenChannelLowPriorityMessageTypeListRequest
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
const apiInstance = new OpenChannelMessagePriorityApi(configuration);

let openChannelLowPriorityMessageTypeListRequest: OpenChannelLowPriorityMessageTypeListRequest; //

const { status, data } = await apiInstance.addOpenChannelLowPriorityMessageTypeList(
    openChannelLowPriorityMessageTypeListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelLowPriorityMessageTypeListRequest** | **OpenChannelLowPriorityMessageTypeListRequest**|  | |


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

# **getOpenChannelLowPriorityMessageTypeList**
> OpenChannelMessageTypeListResponse getOpenChannelLowPriorityMessageTypeList()

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelMessagePriorityApi,
    Configuration
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
const apiInstance = new OpenChannelMessagePriorityApi(configuration);
const { status, data } = await apiInstance.getOpenChannelLowPriorityMessageTypeList();

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

# **removeOpenChannelLowPriorityMessageTypeList**
> CodeOnlyResponse removeOpenChannelLowPriorityMessageTypeList(openChannelLowPriorityMessageTypeListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelMessagePriorityApi,
    Configuration,
    OpenChannelLowPriorityMessageTypeListRequest
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
const apiInstance = new OpenChannelMessagePriorityApi(configuration);

let openChannelLowPriorityMessageTypeListRequest: OpenChannelLowPriorityMessageTypeListRequest; //

const { status, data } = await apiInstance.removeOpenChannelLowPriorityMessageTypeList(
    openChannelLowPriorityMessageTypeListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelLowPriorityMessageTypeListRequest** | **OpenChannelLowPriorityMessageTypeListRequest**|  | |


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

