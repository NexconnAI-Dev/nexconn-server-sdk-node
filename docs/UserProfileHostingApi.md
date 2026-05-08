# UserProfileHostingApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**batchGetUserProfiles**](#batchgetuserprofiles) | **POST** /v4/user/profile/batch/get | Batch get user profiles|
|[**deleteUserProfiles**](#deleteuserprofiles) | **POST** /v4/user/profile/delete | Clear user profiles|
|[**listUserProfiles**](#listuserprofiles) | **POST** /v4/user/profile/list | List user profiles|
|[**setUserProfile**](#setuserprofile) | **POST** /v4/user/profile/set | Set user profile|

# **batchGetUserProfiles**
> UserProfileBatchGetResponse batchGetUserProfiles(userIdsMax20Request)


### Example

```typescript
import {
    UserProfileHostingApi,
    Configuration,
    UserIdsMax20Request
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
const apiInstance = new UserProfileHostingApi(configuration);

let userIdsMax20Request: UserIdsMax20Request; //

const { status, data } = await apiInstance.batchGetUserProfiles(
    userIdsMax20Request
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userIdsMax20Request** | **UserIdsMax20Request**|  | |


### Return type

**UserProfileBatchGetResponse**

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

# **deleteUserProfiles**
> CodeOnlyResponse deleteUserProfiles(userIdsMax20Request)


### Example

```typescript
import {
    UserProfileHostingApi,
    Configuration,
    UserIdsMax20Request
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
const apiInstance = new UserProfileHostingApi(configuration);

let userIdsMax20Request: UserIdsMax20Request; //

const { status, data } = await apiInstance.deleteUserProfiles(
    userIdsMax20Request
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userIdsMax20Request** | **UserIdsMax20Request**|  | |


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

# **listUserProfiles**
> UserProfileListResponse listUserProfiles(userProfileListRequest)


### Example

```typescript
import {
    UserProfileHostingApi,
    Configuration,
    UserProfileListRequest
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
const apiInstance = new UserProfileHostingApi(configuration);

let userProfileListRequest: UserProfileListRequest; //

const { status, data } = await apiInstance.listUserProfiles(
    userProfileListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userProfileListRequest** | **UserProfileListRequest**|  | |


### Return type

**UserProfileListResponse**

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

# **setUserProfile**
> UserProfileSetResponse setUserProfile(userProfileSetRequest)


### Example

```typescript
import {
    UserProfileHostingApi,
    Configuration,
    UserProfileSetRequest
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
const apiInstance = new UserProfileHostingApi(configuration);

let userProfileSetRequest: UserProfileSetRequest; //

const { status, data } = await apiInstance.setUserProfile(
    userProfileSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userProfileSetRequest** | **UserProfileSetRequest**|  | |


### Return type

**UserProfileSetResponse**

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

