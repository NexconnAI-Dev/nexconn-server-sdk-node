# OpenChannelMetadataApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**batchGetOpenChannelMetadata**](#batchgetopenchannelmetadata) | **POST** /v4/open-channel/metadata/batch/get | Query metadata|
|[**batchRemoveOpenChannelMetadata**](#batchremoveopenchannelmetadata) | **POST** /v4/open-channel/metadata/batch/remove | Batch delete metadata|
|[**batchSetOpenChannelMetadata**](#batchsetopenchannelmetadata) | **POST** /v4/open-channel/metadata/batch/set | Batch set metadata|

# **batchGetOpenChannelMetadata**
> OpenChannelMetadataBatchGetResponse batchGetOpenChannelMetadata(openChannelMetadataBatchGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelMetadataApi,
    Configuration,
    OpenChannelMetadataBatchGetRequest
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
const apiInstance = new OpenChannelMetadataApi(configuration);

let openChannelMetadataBatchGetRequest: OpenChannelMetadataBatchGetRequest; //

const { status, data } = await apiInstance.batchGetOpenChannelMetadata(
    openChannelMetadataBatchGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelMetadataBatchGetRequest** | **OpenChannelMetadataBatchGetRequest**|  | |


### Return type

**OpenChannelMetadataBatchGetResponse**

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

# **batchRemoveOpenChannelMetadata**
> CodeOnlyResponse batchRemoveOpenChannelMetadata(openChannelMetadataBatchRemoveRequest)

Rate limit: 100 attrs/sec (shared).

### Example

```typescript
import {
    OpenChannelMetadataApi,
    Configuration,
    OpenChannelMetadataBatchRemoveRequest
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
const apiInstance = new OpenChannelMetadataApi(configuration);

let openChannelMetadataBatchRemoveRequest: OpenChannelMetadataBatchRemoveRequest; //

const { status, data } = await apiInstance.batchRemoveOpenChannelMetadata(
    openChannelMetadataBatchRemoveRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelMetadataBatchRemoveRequest** | **OpenChannelMetadataBatchRemoveRequest**|  | |


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

# **batchSetOpenChannelMetadata**
> CodeOnlyResponse batchSetOpenChannelMetadata(openChannelMetadataBatchSetRequest)

Rate limit: 100 attrs/sec (shared).

### Example

```typescript
import {
    OpenChannelMetadataApi,
    Configuration,
    OpenChannelMetadataBatchSetRequest
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
const apiInstance = new OpenChannelMetadataApi(configuration);

let openChannelMetadataBatchSetRequest: OpenChannelMetadataBatchSetRequest; //

const { status, data } = await apiInstance.batchSetOpenChannelMetadata(
    openChannelMetadataBatchSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelMetadataBatchSetRequest** | **OpenChannelMetadataBatchSetRequest**|  | |


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

