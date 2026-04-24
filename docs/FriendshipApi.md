# FriendshipApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addFriend**](#addfriend) | **POST** /v4/friend/add | Add friend|
|[**getFriendPermission**](#getfriendpermission) | **POST** /v4/friend/permission/get | Get friend permission|
|[**getFriendRelationships**](#getfriendrelationships) | **POST** /v4/friend/relationship/get | Get friend relationships|
|[**listFriends**](#listfriends) | **POST** /v4/friend/list | List friends|
|[**removeAllFriends**](#removeallfriends) | **POST** /v4/friend/remove-all | Clean all friends|
|[**removeFriends**](#removefriends) | **POST** /v4/friend/remove | Delete friends|
|[**setFriendPermission**](#setfriendpermission) | **POST** /v4/friend/permission/set | Set friend permission|
|[**setFriendProfile**](#setfriendprofile) | **POST** /v4/friend/profile/set | Set friend profile|

# **addFriend**
> CodeOnlyResponse addFriend(friendAddRequest)


### Example

```typescript
import {
    FriendshipApi,
    Configuration,
    FriendAddRequest
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
const apiInstance = new FriendshipApi(configuration);

let friendAddRequest: FriendAddRequest; //

const { status, data } = await apiInstance.addFriend(
    friendAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **friendAddRequest** | **FriendAddRequest**|  | |


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

# **getFriendPermission**
> FriendPermissionGetResponse getFriendPermission(friendPermissionGetRequest)


### Example

```typescript
import {
    FriendshipApi,
    Configuration,
    FriendPermissionGetRequest
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
const apiInstance = new FriendshipApi(configuration);

let friendPermissionGetRequest: FriendPermissionGetRequest; //

const { status, data } = await apiInstance.getFriendPermission(
    friendPermissionGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **friendPermissionGetRequest** | **FriendPermissionGetRequest**|  | |


### Return type

**FriendPermissionGetResponse**

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

# **getFriendRelationships**
> FriendRelationshipGetResponse getFriendRelationships(friendRelationshipGetRequest)


### Example

```typescript
import {
    FriendshipApi,
    Configuration,
    FriendRelationshipGetRequest
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
const apiInstance = new FriendshipApi(configuration);

let friendRelationshipGetRequest: FriendRelationshipGetRequest; //

const { status, data } = await apiInstance.getFriendRelationships(
    friendRelationshipGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **friendRelationshipGetRequest** | **FriendRelationshipGetRequest**|  | |


### Return type

**FriendRelationshipGetResponse**

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

# **listFriends**
> FriendListResponse listFriends(friendListRequest)


### Example

```typescript
import {
    FriendshipApi,
    Configuration,
    FriendListRequest
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
const apiInstance = new FriendshipApi(configuration);

let friendListRequest: FriendListRequest; //

const { status, data } = await apiInstance.listFriends(
    friendListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **friendListRequest** | **FriendListRequest**|  | |


### Return type

**FriendListResponse**

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

# **removeAllFriends**
> CodeOnlyResponse removeAllFriends(friendCleanRequest)


### Example

```typescript
import {
    FriendshipApi,
    Configuration,
    FriendCleanRequest
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
const apiInstance = new FriendshipApi(configuration);

let friendCleanRequest: FriendCleanRequest; //

const { status, data } = await apiInstance.removeAllFriends(
    friendCleanRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **friendCleanRequest** | **FriendCleanRequest**|  | |


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

# **removeFriends**
> CodeOnlyResponse removeFriends(friendDeleteRequest)


### Example

```typescript
import {
    FriendshipApi,
    Configuration,
    FriendDeleteRequest
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
const apiInstance = new FriendshipApi(configuration);

let friendDeleteRequest: FriendDeleteRequest; //

const { status, data } = await apiInstance.removeFriends(
    friendDeleteRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **friendDeleteRequest** | **FriendDeleteRequest**|  | |


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

# **setFriendPermission**
> CodeOnlyResponse setFriendPermission(friendPermissionSetRequest)


### Example

```typescript
import {
    FriendshipApi,
    Configuration,
    FriendPermissionSetRequest
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
const apiInstance = new FriendshipApi(configuration);

let friendPermissionSetRequest: FriendPermissionSetRequest; //

const { status, data } = await apiInstance.setFriendPermission(
    friendPermissionSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **friendPermissionSetRequest** | **FriendPermissionSetRequest**|  | |


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

# **setFriendProfile**
> CodeOnlyResponse setFriendProfile(friendProfileSetRequest)


### Example

```typescript
import {
    FriendshipApi,
    Configuration,
    FriendProfileSetRequest
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
const apiInstance = new FriendshipApi(configuration);

let friendProfileSetRequest: FriendProfileSetRequest; //

const { status, data } = await apiInstance.setFriendProfile(
    friendProfileSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **friendProfileSetRequest** | **FriendProfileSetRequest**|  | |


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

