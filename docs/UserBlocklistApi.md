# UserBlocklistApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addUserBlocklist**](#adduserblocklist) | **POST** /v4/user/blocklist/add | Add to blocklist|
|[**getUserBlocklist**](#getuserblocklist) | **POST** /v4/user/blocklist/get | Get blocklist|
|[**removeUserBlocklist**](#removeuserblocklist) | **POST** /v4/user/blocklist/remove | Remove from blocklist|

# **addUserBlocklist**
> CodeOnlyResponse addUserBlocklist(userBlocklistAddRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserBlocklistApi,
    Configuration,
    UserBlocklistAddRequest
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
const apiInstance = new UserBlocklistApi(configuration);

let userBlocklistAddRequest: UserBlocklistAddRequest; //

const { status, data } = await apiInstance.addUserBlocklist(
    userBlocklistAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userBlocklistAddRequest** | **UserBlocklistAddRequest**|  | |


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

# **getUserBlocklist**
> UserBlocklistGetResponse getUserBlocklist(userBlocklistGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserBlocklistApi,
    Configuration,
    UserBlocklistGetRequest
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
const apiInstance = new UserBlocklistApi(configuration);

let userBlocklistGetRequest: UserBlocklistGetRequest; //

const { status, data } = await apiInstance.getUserBlocklist(
    userBlocklistGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userBlocklistGetRequest** | **UserBlocklistGetRequest**|  | |


### Return type

**UserBlocklistGetResponse**

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

# **removeUserBlocklist**
> CodeOnlyResponse removeUserBlocklist(userBlocklistRemoveRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserBlocklistApi,
    Configuration,
    UserBlocklistRemoveRequest
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
const apiInstance = new UserBlocklistApi(configuration);

let userBlocklistRemoveRequest: UserBlocklistRemoveRequest; //

const { status, data } = await apiInstance.removeUserBlocklist(
    userBlocklistRemoveRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userBlocklistRemoveRequest** | **UserBlocklistRemoveRequest**|  | |


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

