# ModerationApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**batchAddProfanityWords**](#batchaddprofanitywords) | **POST** /v4/profanity-word/batch/add | Batch add profanity words|
|[**batchRemoveProfanityWords**](#batchremoveprofanitywords) | **POST** /v4/profanity-word/batch/remove | Batch delete profanity words|
|[**listProfanityWords**](#listprofanitywords) | **POST** /v4/profanity-word/list | List profanity words|
|[**removeProfanityWord**](#removeprofanityword) | **POST** /v4/profanity-word/remove | Delete profanity word|

# **batchAddProfanityWords**
> ProfanityWordBatchAddResponse batchAddProfanityWords(profanityWordBatchAddRequest)


### Example

```typescript
import {
    ModerationApi,
    Configuration,
    ProfanityWordBatchAddRequest
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
const apiInstance = new ModerationApi(configuration);

let profanityWordBatchAddRequest: ProfanityWordBatchAddRequest; //

const { status, data } = await apiInstance.batchAddProfanityWords(
    profanityWordBatchAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profanityWordBatchAddRequest** | **ProfanityWordBatchAddRequest**|  | |


### Return type

**ProfanityWordBatchAddResponse**

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

# **batchRemoveProfanityWords**
> CodeOnlyResponse batchRemoveProfanityWords(profanityWordBatchDeleteRequest)


### Example

```typescript
import {
    ModerationApi,
    Configuration,
    ProfanityWordBatchDeleteRequest
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
const apiInstance = new ModerationApi(configuration);

let profanityWordBatchDeleteRequest: ProfanityWordBatchDeleteRequest; //

const { status, data } = await apiInstance.batchRemoveProfanityWords(
    profanityWordBatchDeleteRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profanityWordBatchDeleteRequest** | **ProfanityWordBatchDeleteRequest**|  | |


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

# **listProfanityWords**
> ProfanityWordListResponse listProfanityWords(profanityWordListRequest)


### Example

```typescript
import {
    ModerationApi,
    Configuration,
    ProfanityWordListRequest
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
const apiInstance = new ModerationApi(configuration);

let profanityWordListRequest: ProfanityWordListRequest; //

const { status, data } = await apiInstance.listProfanityWords(
    profanityWordListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profanityWordListRequest** | **ProfanityWordListRequest**|  | |


### Return type

**ProfanityWordListResponse**

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

# **removeProfanityWord**
> CodeOnlyResponse removeProfanityWord(profanityWordDeleteRequest)


### Example

```typescript
import {
    ModerationApi,
    Configuration,
    ProfanityWordDeleteRequest
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
const apiInstance = new ModerationApi(configuration);

let profanityWordDeleteRequest: ProfanityWordDeleteRequest; //

const { status, data } = await apiInstance.removeProfanityWord(
    profanityWordDeleteRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profanityWordDeleteRequest** | **ProfanityWordDeleteRequest**|  | |


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

