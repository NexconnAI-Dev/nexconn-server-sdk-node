# UserManagementApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**banUsers**](#banusers) | **POST** /v4/user/ban | Ban a user|
|[**batchGetUserTags**](#batchgetusertags) | **POST** /v4/user/tag/batch/get | Get user tags|
|[**batchSetUserTags**](#batchsetusertags) | **POST** /v4/user/tag/batch/set | Batch set user tags|
|[**expireAccessToken**](#expireaccesstoken) | **POST** /v4/auth/access-token/expire | Expire an access token|
|[**getUser**](#getuser) | **POST** /v4/user/get | Get user info|
|[**getUserConnectionStatus**](#getuserconnectionstatus) | **POST** /v4/user/connection-status/get | Check user online status|
|[**issueAccessToken**](#issueaccesstoken) | **POST** /v4/auth/access-token/issue | Register a user|
|[**listBannedUsers**](#listbannedusers) | **POST** /v4/user/ban/list | List banned users|
|[**listChannelTypeMute**](#listchanneltypemute) | **POST** /v4/channel-type/mute/list | List muted direct channel users|
|[**listSoftDeletedUsers**](#listsoftdeletedusers) | **POST** /v4/user/soft-deleted/list | Query soft-deleted users|
|[**restoreUsers**](#restoreusers) | **POST** /v4/user/restore | Restore a user|
|[**setChannelTypeMute**](#setchanneltypemute) | **POST** /v4/channel-type/mute/set | Mute a user in direct channels|
|[**softDeleteUsers**](#softdeleteusers) | **POST** /v4/user/soft-delete | Soft-delete a user|
|[**unbanUsers**](#unbanusers) | **POST** /v4/user/unban | Unban a user|
|[**updateUser**](#updateuser) | **POST** /v4/user/update | Update user info|

# **banUsers**
> CodeOnlyResponse banUsers(userBanRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    UserBanRequest
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
const apiInstance = new UserManagementApi(configuration);

let userBanRequest: UserBanRequest; //

const { status, data } = await apiInstance.banUsers(
    userBanRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userBanRequest** | **UserBanRequest**|  | |


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

# **batchGetUserTags**
> UserTagBatchGetResponse batchGetUserTags(userTagBatchGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    UserTagBatchGetRequest
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
const apiInstance = new UserManagementApi(configuration);

let userTagBatchGetRequest: UserTagBatchGetRequest; //

const { status, data } = await apiInstance.batchGetUserTags(
    userTagBatchGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userTagBatchGetRequest** | **UserTagBatchGetRequest**|  | |


### Return type

**UserTagBatchGetResponse**

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

# **batchSetUserTags**
> CodeOnlyResponse batchSetUserTags(userTagBatchSetRequest)

Rate limit: 10/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    UserTagBatchSetRequest
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
const apiInstance = new UserManagementApi(configuration);

let userTagBatchSetRequest: UserTagBatchSetRequest; //

const { status, data } = await apiInstance.batchSetUserTags(
    userTagBatchSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userTagBatchSetRequest** | **UserTagBatchSetRequest**|  | |


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

# **expireAccessToken**
> CodeOnlyResponse expireAccessToken(accessTokenExpireRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    AccessTokenExpireRequest
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
const apiInstance = new UserManagementApi(configuration);

let accessTokenExpireRequest: AccessTokenExpireRequest; //

const { status, data } = await apiInstance.expireAccessToken(
    accessTokenExpireRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **accessTokenExpireRequest** | **AccessTokenExpireRequest**|  | |


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

# **getUser**
> UserGetResponse getUser(userGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    UserGetRequest
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
const apiInstance = new UserManagementApi(configuration);

let userGetRequest: UserGetRequest; //

const { status, data } = await apiInstance.getUser(
    userGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userGetRequest** | **UserGetRequest**|  | |


### Return type

**UserGetResponse**

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

# **getUserConnectionStatus**
> UserConnectionStatusResponse getUserConnectionStatus(userConnectionStatusRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    UserConnectionStatusRequest
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
const apiInstance = new UserManagementApi(configuration);

let userConnectionStatusRequest: UserConnectionStatusRequest; //

const { status, data } = await apiInstance.getUserConnectionStatus(
    userConnectionStatusRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userConnectionStatusRequest** | **UserConnectionStatusRequest**|  | |


### Return type

**UserConnectionStatusResponse**

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

# **issueAccessToken**
> AccessTokenIssueResponse issueAccessToken(accessTokenIssueRequest)

Rate limit: 200/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    AccessTokenIssueRequest
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
const apiInstance = new UserManagementApi(configuration);

let accessTokenIssueRequest: AccessTokenIssueRequest; //

const { status, data } = await apiInstance.issueAccessToken(
    accessTokenIssueRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **accessTokenIssueRequest** | **AccessTokenIssueRequest**|  | |


### Return type

**AccessTokenIssueResponse**

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

# **listBannedUsers**
> UserBanListResponse listBannedUsers(userBanListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    UserBanListRequest
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
const apiInstance = new UserManagementApi(configuration);

let userBanListRequest: UserBanListRequest; //

const { status, data } = await apiInstance.listBannedUsers(
    userBanListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userBanListRequest** | **UserBanListRequest**|  | |


### Return type

**UserBanListResponse**

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

# **listChannelTypeMute**
> ChannelTypeMuteListResponse listChannelTypeMute(channelTypeMuteListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    ChannelTypeMuteListRequest
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
const apiInstance = new UserManagementApi(configuration);

let channelTypeMuteListRequest: ChannelTypeMuteListRequest; //

const { status, data } = await apiInstance.listChannelTypeMute(
    channelTypeMuteListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelTypeMuteListRequest** | **ChannelTypeMuteListRequest**|  | |


### Return type

**ChannelTypeMuteListResponse**

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

# **listSoftDeletedUsers**
> UserSoftDeletedListResponse listSoftDeletedUsers(userSoftDeletedListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    UserSoftDeletedListRequest
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
const apiInstance = new UserManagementApi(configuration);

let userSoftDeletedListRequest: UserSoftDeletedListRequest; //

const { status, data } = await apiInstance.listSoftDeletedUsers(
    userSoftDeletedListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userSoftDeletedListRequest** | **UserSoftDeletedListRequest**|  | |


### Return type

**UserSoftDeletedListResponse**

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

# **restoreUsers**
> UserOperationResponse restoreUsers(userIdsMax100Request)

Rate limit: 100 users/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    UserIdsMax100Request
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
const apiInstance = new UserManagementApi(configuration);

let userIdsMax100Request: UserIdsMax100Request; //

const { status, data } = await apiInstance.restoreUsers(
    userIdsMax100Request
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userIdsMax100Request** | **UserIdsMax100Request**|  | |


### Return type

**UserOperationResponse**

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

# **setChannelTypeMute**
> CodeOnlyResponse setChannelTypeMute(channelTypeMuteSetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    ChannelTypeMuteSetRequest
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
const apiInstance = new UserManagementApi(configuration);

let channelTypeMuteSetRequest: ChannelTypeMuteSetRequest; //

const { status, data } = await apiInstance.setChannelTypeMute(
    channelTypeMuteSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelTypeMuteSetRequest** | **ChannelTypeMuteSetRequest**|  | |


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

# **softDeleteUsers**
> UserOperationResponse softDeleteUsers(userIdsMax100Request)

Rate limit: 100 users/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    UserIdsMax100Request
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
const apiInstance = new UserManagementApi(configuration);

let userIdsMax100Request: UserIdsMax100Request; //

const { status, data } = await apiInstance.softDeleteUsers(
    userIdsMax100Request
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userIdsMax100Request** | **UserIdsMax100Request**|  | |


### Return type

**UserOperationResponse**

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

# **unbanUsers**
> CodeOnlyResponse unbanUsers(userIdsMax20Request)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
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
const apiInstance = new UserManagementApi(configuration);

let userIdsMax20Request: UserIdsMax20Request; //

const { status, data } = await apiInstance.unbanUsers(
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

# **updateUser**
> CodeOnlyResponse updateUser(userUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    UserManagementApi,
    Configuration,
    UserUpdateRequest
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
const apiInstance = new UserManagementApi(configuration);

let userUpdateRequest: UserUpdateRequest; //

const { status, data } = await apiInstance.updateUser(
    userUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **userUpdateRequest** | **UserUpdateRequest**|  | |


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

