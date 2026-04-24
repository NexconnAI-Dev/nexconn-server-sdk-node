# GroupChannelManagementApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addGroupChannelAdmins**](#addgroupchanneladmins) | **POST** /v4/group-channel/admin/add | Add group admins|
|[**addGroupChannelMemberFavorites**](#addgroupchannelmemberfavorites) | **POST** /v4/group-channel/member/favorites/add | Add favorite group members|
|[**batchGetGroupChannelMembers**](#batchgetgroupchannelmembers) | **POST** /v4/group-channel/member/batch/get | Get specific group members|
|[**batchGetGroupChannelProfiles**](#batchgetgroupchannelprofiles) | **POST** /v4/group-channel/profile/list | List group profiles|
|[**createGroupChannel**](#creategroupchannel) | **POST** /v4/group-channel/create | Create a group|
|[**deleteGroupChannelAlias**](#deletegroupchannelalias) | **POST** /v4/group-channel/alias/delete | Delete group alias|
|[**dismissGroupChannel**](#dismissgroupchannel) | **POST** /v4/group-channel/dismiss | Dismiss a group|
|[**getGroupChannelAlias**](#getgroupchannelalias) | **POST** /v4/group-channel/alias/get | Get group alias|
|[**joinGroupChannel**](#joingroupchannel) | **POST** /v4/group-channel/join | Join a group|
|[**kickUserFromAllGroupChannels**](#kickuserfromallgroupchannels) | **POST** /v4/group-channel/member/kickout-all | Remove a user from all groups|
|[**listGroupChannelMemberFavorites**](#listgroupchannelmemberfavorites) | **POST** /v4/group-channel/member/favorites/list | List favorite group members|
|[**listGroupChannelMembers**](#listgroupchannelmembers) | **POST** /v4/group-channel/member/list | Query group members|
|[**listGroupChannels**](#listgroupchannels) | **POST** /v4/group-channel/list | List group channels|
|[**listUserJoinedGroupChannels**](#listuserjoinedgroupchannels) | **POST** /v4/group-channel/joined/list | Query user\&#39;s groups|
|[**quitGroupChannel**](#quitgroupchannel) | **POST** /v4/group-channel/leave | Leave a group|
|[**removeGroupChannelAdmins**](#removegroupchanneladmins) | **POST** /v4/group-channel/admin/remove | Remove group admins|
|[**removeGroupChannelMemberFavorites**](#removegroupchannelmemberfavorites) | **POST** /v4/group-channel/member/favorites/remove | Remove favorite group members|
|[**setGroupChannelAlias**](#setgroupchannelalias) | **POST** /v4/group-channel/alias/set | Set group alias|
|[**setGroupChannelMember**](#setgroupchannelmember) | **POST** /v4/group-channel/member/set | Set group member profile|
|[**transferGroupChannelOwner**](#transfergroupchannelowner) | **POST** /v4/group-channel/transfer/owner | Transfer group ownership|
|[**updateGroupChannelProfile**](#updategroupchannelprofile) | **POST** /v4/group-channel/profile/update | Update group info|

# **addGroupChannelAdmins**
> CodeOnlyResponse addGroupChannelAdmins(groupChannelAdminUsersRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelAdminUsersRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelAdminUsersRequest: GroupChannelAdminUsersRequest; //

const { status, data } = await apiInstance.addGroupChannelAdmins(
    groupChannelAdminUsersRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelAdminUsersRequest** | **GroupChannelAdminUsersRequest**|  | |


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

# **addGroupChannelMemberFavorites**
> CodeOnlyResponse addGroupChannelMemberFavorites(groupChannelMemberFavoritesUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelMemberFavoritesUpdateRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelMemberFavoritesUpdateRequest: GroupChannelMemberFavoritesUpdateRequest; //

const { status, data } = await apiInstance.addGroupChannelMemberFavorites(
    groupChannelMemberFavoritesUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelMemberFavoritesUpdateRequest** | **GroupChannelMemberFavoritesUpdateRequest**|  | |


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

# **batchGetGroupChannelMembers**
> GroupChannelMemberBatchGetResponse batchGetGroupChannelMembers(groupChannelMemberBatchGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelMemberBatchGetRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelMemberBatchGetRequest: GroupChannelMemberBatchGetRequest; //

const { status, data } = await apiInstance.batchGetGroupChannelMembers(
    groupChannelMemberBatchGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelMemberBatchGetRequest** | **GroupChannelMemberBatchGetRequest**|  | |


### Return type

**GroupChannelMemberBatchGetResponse**

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

# **batchGetGroupChannelProfiles**
> GroupChannelProfileListResponse batchGetGroupChannelProfiles(groupChannelProfileListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelProfileListRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelProfileListRequest: GroupChannelProfileListRequest; //

const { status, data } = await apiInstance.batchGetGroupChannelProfiles(
    groupChannelProfileListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelProfileListRequest** | **GroupChannelProfileListRequest**|  | |


### Return type

**GroupChannelProfileListResponse**

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

# **createGroupChannel**
> CodeOnlyResponse createGroupChannel(groupChannelCreateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelCreateRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelCreateRequest: GroupChannelCreateRequest; //

const { status, data } = await apiInstance.createGroupChannel(
    groupChannelCreateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelCreateRequest** | **GroupChannelCreateRequest**|  | |


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

# **deleteGroupChannelAlias**
> CodeOnlyResponse deleteGroupChannelAlias(groupChannelAliasGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelAliasGetRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelAliasGetRequest: GroupChannelAliasGetRequest; //

const { status, data } = await apiInstance.deleteGroupChannelAlias(
    groupChannelAliasGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelAliasGetRequest** | **GroupChannelAliasGetRequest**|  | |


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

# **dismissGroupChannel**
> CodeOnlyResponse dismissGroupChannel(groupChannelDismissRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelDismissRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelDismissRequest: GroupChannelDismissRequest; //

const { status, data } = await apiInstance.dismissGroupChannel(
    groupChannelDismissRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelDismissRequest** | **GroupChannelDismissRequest**|  | |


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

# **getGroupChannelAlias**
> GroupChannelAliasGetResponse getGroupChannelAlias(groupChannelAliasGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelAliasGetRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelAliasGetRequest: GroupChannelAliasGetRequest; //

const { status, data } = await apiInstance.getGroupChannelAlias(
    groupChannelAliasGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelAliasGetRequest** | **GroupChannelAliasGetRequest**|  | |


### Return type

**GroupChannelAliasGetResponse**

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

# **joinGroupChannel**
> GroupChannelJoinResponse joinGroupChannel(groupChannelJoinRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelJoinRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelJoinRequest: GroupChannelJoinRequest; //

const { status, data } = await apiInstance.joinGroupChannel(
    groupChannelJoinRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelJoinRequest** | **GroupChannelJoinRequest**|  | |


### Return type

**GroupChannelJoinResponse**

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

# **kickUserFromAllGroupChannels**
> CodeOnlyResponse kickUserFromAllGroupChannels(groupChannelKickUserFromAllRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelKickUserFromAllRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelKickUserFromAllRequest: GroupChannelKickUserFromAllRequest; //

const { status, data } = await apiInstance.kickUserFromAllGroupChannels(
    groupChannelKickUserFromAllRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelKickUserFromAllRequest** | **GroupChannelKickUserFromAllRequest**|  | |


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

# **listGroupChannelMemberFavorites**
> GroupChannelMemberFavoritesListResponse listGroupChannelMemberFavorites(groupChannelMemberFavoritesListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelMemberFavoritesListRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelMemberFavoritesListRequest: GroupChannelMemberFavoritesListRequest; //

const { status, data } = await apiInstance.listGroupChannelMemberFavorites(
    groupChannelMemberFavoritesListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelMemberFavoritesListRequest** | **GroupChannelMemberFavoritesListRequest**|  | |


### Return type

**GroupChannelMemberFavoritesListResponse**

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

# **listGroupChannelMembers**
> GroupChannelMemberListResponse listGroupChannelMembers(groupChannelMemberListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelMemberListRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelMemberListRequest: GroupChannelMemberListRequest; //

const { status, data } = await apiInstance.listGroupChannelMembers(
    groupChannelMemberListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelMemberListRequest** | **GroupChannelMemberListRequest**|  | |


### Return type

**GroupChannelMemberListResponse**

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

# **listGroupChannels**
> GroupChannelListResponse listGroupChannels(groupChannelListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelListRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelListRequest: GroupChannelListRequest; //

const { status, data } = await apiInstance.listGroupChannels(
    groupChannelListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelListRequest** | **GroupChannelListRequest**|  | |


### Return type

**GroupChannelListResponse**

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

# **listUserJoinedGroupChannels**
> GroupChannelJoinedListResponse listUserJoinedGroupChannels(groupChannelJoinedListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelJoinedListRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelJoinedListRequest: GroupChannelJoinedListRequest; //

const { status, data } = await apiInstance.listUserJoinedGroupChannels(
    groupChannelJoinedListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelJoinedListRequest** | **GroupChannelJoinedListRequest**|  | |


### Return type

**GroupChannelJoinedListResponse**

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

# **quitGroupChannel**
> CodeOnlyResponse quitGroupChannel(groupChannelQuitRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelQuitRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelQuitRequest: GroupChannelQuitRequest; //

const { status, data } = await apiInstance.quitGroupChannel(
    groupChannelQuitRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelQuitRequest** | **GroupChannelQuitRequest**|  | |


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

# **removeGroupChannelAdmins**
> CodeOnlyResponse removeGroupChannelAdmins(groupChannelAdminUsersRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelAdminUsersRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelAdminUsersRequest: GroupChannelAdminUsersRequest; //

const { status, data } = await apiInstance.removeGroupChannelAdmins(
    groupChannelAdminUsersRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelAdminUsersRequest** | **GroupChannelAdminUsersRequest**|  | |


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

# **removeGroupChannelMemberFavorites**
> CodeOnlyResponse removeGroupChannelMemberFavorites(groupChannelMemberFavoritesUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelMemberFavoritesUpdateRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelMemberFavoritesUpdateRequest: GroupChannelMemberFavoritesUpdateRequest; //

const { status, data } = await apiInstance.removeGroupChannelMemberFavorites(
    groupChannelMemberFavoritesUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelMemberFavoritesUpdateRequest** | **GroupChannelMemberFavoritesUpdateRequest**|  | |


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

# **setGroupChannelAlias**
> CodeOnlyResponse setGroupChannelAlias(groupChannelAliasSetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelAliasSetRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelAliasSetRequest: GroupChannelAliasSetRequest; //

const { status, data } = await apiInstance.setGroupChannelAlias(
    groupChannelAliasSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelAliasSetRequest** | **GroupChannelAliasSetRequest**|  | |


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

# **setGroupChannelMember**
> CodeOnlyResponse setGroupChannelMember(groupChannelMemberSetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelMemberSetRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelMemberSetRequest: GroupChannelMemberSetRequest; //

const { status, data } = await apiInstance.setGroupChannelMember(
    groupChannelMemberSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelMemberSetRequest** | **GroupChannelMemberSetRequest**|  | |


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

# **transferGroupChannelOwner**
> CodeOnlyResponse transferGroupChannelOwner(groupChannelTransferOwnerRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelTransferOwnerRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelTransferOwnerRequest: GroupChannelTransferOwnerRequest; //

const { status, data } = await apiInstance.transferGroupChannelOwner(
    groupChannelTransferOwnerRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelTransferOwnerRequest** | **GroupChannelTransferOwnerRequest**|  | |


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

# **updateGroupChannelProfile**
> CodeOnlyResponse updateGroupChannelProfile(groupChannelProfileUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelManagementApi,
    Configuration,
    GroupChannelProfileUpdateRequest
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
const apiInstance = new GroupChannelManagementApi(configuration);

let groupChannelProfileUpdateRequest: GroupChannelProfileUpdateRequest; //

const { status, data } = await apiInstance.updateGroupChannelProfile(
    groupChannelProfileUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelProfileUpdateRequest** | **GroupChannelProfileUpdateRequest**|  | |


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

