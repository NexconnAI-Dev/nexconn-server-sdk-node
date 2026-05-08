# CommunityChannelManagementApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addCommunityChannelUserGroupUsers**](#addcommunitychannelusergroupusers) | **POST** /v4/community-channel/user-group/user/add | Add community channel user group users|
|[**addCommunityChannelUserGroups**](#addcommunitychannelusergroups) | **POST** /v4/community-channel/user-group/add | Add community channel user groups|
|[**addPrivateSubchannelMembers**](#addprivatesubchannelmembers) | **POST** /v4/community-channel/private-subchannel/member/add | Add private subchannel members|
|[**bindCommunityChannelUserGroup**](#bindcommunitychannelusergroup) | **POST** /v4/community-channel/channel/user-group/bind | Bind community channel user group|
|[**checkCommunityChannelMemberExist**](#checkcommunitychannelmemberexist) | **POST** /v4/community-channel/member/exist | Check community channel member exist|
|[**createCommunityChannel**](#createcommunitychannel) | **POST** /v4/community-channel/create | Create community channel|
|[**createCommunitySubchannel**](#createcommunitysubchannel) | **POST** /v4/community-channel/subchannel/create | Create community subchannel|
|[**deleteCommunitySubchannel**](#deletecommunitysubchannel) | **POST** /v4/community-channel/subchannel/delete | Delete community subchannel|
|[**dismissCommunityChannel**](#dismisscommunitychannel) | **POST** /v4/community-channel/dismiss | Dismiss community channel|
|[**joinCommunityChannel**](#joincommunitychannel) | **POST** /v4/community-channel/join | Join community channel|
|[**listCommunityChannelHistoryMessages**](#listcommunitychannelhistorymessages) | **POST** /v4/community-channel/history-message/list | List community-channel history messages|
|[**listCommunityChannelSubchannelUserGroups**](#listcommunitychannelsubchannelusergroups) | **POST** /v4/community-channel/channel/user-group/list | List community channel subchannel user groups|
|[**listCommunityChannelUserGroupSubchannels**](#listcommunitychannelusergroupsubchannels) | **POST** /v4/community-channel/user-group/subchannel/list | List community channel user group subchannels|
|[**listCommunityChannelUserGroups**](#listcommunitychannelusergroups) | **POST** /v4/community-channel/user-group/list | List community channel user groups|
|[**listCommunityChannelUserUserGroups**](#listcommunitychanneluserusergroups) | **POST** /v4/community-channel/user/user-group/list | List community channel user user groups|
|[**listCommunitySubchannels**](#listcommunitysubchannels) | **POST** /v4/community-channel/subchannel/list | List community subchannels|
|[**listCommunityUserSubchannels**](#listcommunityusersubchannels) | **POST** /v4/community-channel/user/subchannel/list | List community user subchannels|
|[**listPrivateSubchannelMembers**](#listprivatesubchannelmembers) | **POST** /v4/community-channel/private-subchannel/member/list | List private subchannel members|
|[**quitCommunityChannel**](#quitcommunitychannel) | **POST** /v4/community-channel/leave | Leave community channel|
|[**removeCommunityChannelUserGroupUsers**](#removecommunitychannelusergroupusers) | **POST** /v4/community-channel/user-group/user/remove | Remove community channel user group users|
|[**removeCommunityChannelUserGroups**](#removecommunitychannelusergroups) | **POST** /v4/community-channel/user-group/remove | Delete community channel user groups|
|[**removePrivateSubchannelMembers**](#removeprivatesubchannelmembers) | **POST** /v4/community-channel/private-subchannel/member/remove | Remove private subchannel members|
|[**unbindCommunityChannelUserGroup**](#unbindcommunitychannelusergroup) | **POST** /v4/community-channel/channel/user-group/unbind | Unbind community channel user group|
|[**updateCommunityChannelInfo**](#updatecommunitychannelinfo) | **POST** /v4/community-channel/update | Update community channel info|
|[**updateCommunitySubchannelType**](#updatecommunitysubchanneltype) | **POST** /v4/community-channel/subchannel-type/update | Update community subchannel type|

# **addCommunityChannelUserGroupUsers**
> CodeOnlyResponse addCommunityChannelUserGroupUsers(communityChannelUserGroupUsersRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelUserGroupUsersRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelUserGroupUsersRequest: CommunityChannelUserGroupUsersRequest; //

const { status, data } = await apiInstance.addCommunityChannelUserGroupUsers(
    communityChannelUserGroupUsersRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelUserGroupUsersRequest** | **CommunityChannelUserGroupUsersRequest**|  | |


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

# **addCommunityChannelUserGroups**
> CodeOnlyResponse addCommunityChannelUserGroups(communityChannelUserGroupAddRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelUserGroupAddRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelUserGroupAddRequest: CommunityChannelUserGroupAddRequest; //

const { status, data } = await apiInstance.addCommunityChannelUserGroups(
    communityChannelUserGroupAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelUserGroupAddRequest** | **CommunityChannelUserGroupAddRequest**|  | |


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

# **addPrivateSubchannelMembers**
> CodeOnlyResponse addPrivateSubchannelMembers(communityPrivateSubchannelMembersRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityPrivateSubchannelMembersRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityPrivateSubchannelMembersRequest: CommunityPrivateSubchannelMembersRequest; //

const { status, data } = await apiInstance.addPrivateSubchannelMembers(
    communityPrivateSubchannelMembersRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityPrivateSubchannelMembersRequest** | **CommunityPrivateSubchannelMembersRequest**|  | |


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

# **bindCommunityChannelUserGroup**
> CodeOnlyResponse bindCommunityChannelUserGroup(communityChannelUserGroupBindingRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelUserGroupBindingRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelUserGroupBindingRequest: CommunityChannelUserGroupBindingRequest; //

const { status, data } = await apiInstance.bindCommunityChannelUserGroup(
    communityChannelUserGroupBindingRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelUserGroupBindingRequest** | **CommunityChannelUserGroupBindingRequest**|  | |


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

# **checkCommunityChannelMemberExist**
> CommunityChannelMemberExistResponse checkCommunityChannelMemberExist(communityChannelMemberRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelMemberRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelMemberRequest: CommunityChannelMemberRequest; //

const { status, data } = await apiInstance.checkCommunityChannelMemberExist(
    communityChannelMemberRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMemberRequest** | **CommunityChannelMemberRequest**|  | |


### Return type

**CommunityChannelMemberExistResponse**

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

# **createCommunityChannel**
> CodeOnlyResponse createCommunityChannel(communityChannelCreateRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelCreateRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelCreateRequest: CommunityChannelCreateRequest; //

const { status, data } = await apiInstance.createCommunityChannel(
    communityChannelCreateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelCreateRequest** | **CommunityChannelCreateRequest**|  | |


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

# **createCommunitySubchannel**
> CodeOnlyResponse createCommunitySubchannel(communitySubchannelCreateRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunitySubchannelCreateRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communitySubchannelCreateRequest: CommunitySubchannelCreateRequest; //

const { status, data } = await apiInstance.createCommunitySubchannel(
    communitySubchannelCreateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communitySubchannelCreateRequest** | **CommunitySubchannelCreateRequest**|  | |


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

# **deleteCommunitySubchannel**
> CodeOnlyResponse deleteCommunitySubchannel(communitySubchannelKeyRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunitySubchannelKeyRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communitySubchannelKeyRequest: CommunitySubchannelKeyRequest; //

const { status, data } = await apiInstance.deleteCommunitySubchannel(
    communitySubchannelKeyRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communitySubchannelKeyRequest** | **CommunitySubchannelKeyRequest**|  | |


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

# **dismissCommunityChannel**
> CodeOnlyResponse dismissCommunityChannel(communityChannelDismissRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelDismissRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelDismissRequest: CommunityChannelDismissRequest; //

const { status, data } = await apiInstance.dismissCommunityChannel(
    communityChannelDismissRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelDismissRequest** | **CommunityChannelDismissRequest**|  | |


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

# **joinCommunityChannel**
> CodeOnlyResponse joinCommunityChannel(communityChannelMemberRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelMemberRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelMemberRequest: CommunityChannelMemberRequest; //

const { status, data } = await apiInstance.joinCommunityChannel(
    communityChannelMemberRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMemberRequest** | **CommunityChannelMemberRequest**|  | |


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

# **listCommunityChannelHistoryMessages**
> MessageHistoryResponse listCommunityChannelHistoryMessages(communityChannelHistoryMessageListRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelHistoryMessageListRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelHistoryMessageListRequest: CommunityChannelHistoryMessageListRequest; //

const { status, data } = await apiInstance.listCommunityChannelHistoryMessages(
    communityChannelHistoryMessageListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelHistoryMessageListRequest** | **CommunityChannelHistoryMessageListRequest**|  | |


### Return type

**MessageHistoryResponse**

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

# **listCommunityChannelSubchannelUserGroups**
> CommunityChannelSubchannelUserGroupListResponse listCommunityChannelSubchannelUserGroups(communityChannelSubchannelUserGroupListRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelSubchannelUserGroupListRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelSubchannelUserGroupListRequest: CommunityChannelSubchannelUserGroupListRequest; //

const { status, data } = await apiInstance.listCommunityChannelSubchannelUserGroups(
    communityChannelSubchannelUserGroupListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelSubchannelUserGroupListRequest** | **CommunityChannelSubchannelUserGroupListRequest**|  | |


### Return type

**CommunityChannelSubchannelUserGroupListResponse**

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

# **listCommunityChannelUserGroupSubchannels**
> CommunityChannelUserGroupSubchannelListResponse listCommunityChannelUserGroupSubchannels(communityChannelUserGroupSubchannelListRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelUserGroupSubchannelListRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelUserGroupSubchannelListRequest: CommunityChannelUserGroupSubchannelListRequest; //

const { status, data } = await apiInstance.listCommunityChannelUserGroupSubchannels(
    communityChannelUserGroupSubchannelListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelUserGroupSubchannelListRequest** | **CommunityChannelUserGroupSubchannelListRequest**|  | |


### Return type

**CommunityChannelUserGroupSubchannelListResponse**

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

# **listCommunityChannelUserGroups**
> CommunityChannelUserGroupListResponse listCommunityChannelUserGroups(communityChannelUserGroupListRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelUserGroupListRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelUserGroupListRequest: CommunityChannelUserGroupListRequest; //

const { status, data } = await apiInstance.listCommunityChannelUserGroups(
    communityChannelUserGroupListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelUserGroupListRequest** | **CommunityChannelUserGroupListRequest**|  | |


### Return type

**CommunityChannelUserGroupListResponse**

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

# **listCommunityChannelUserUserGroups**
> CommunityChannelUserUserGroupListResponse listCommunityChannelUserUserGroups(communityChannelUserUserGroupListRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelUserUserGroupListRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelUserUserGroupListRequest: CommunityChannelUserUserGroupListRequest; //

const { status, data } = await apiInstance.listCommunityChannelUserUserGroups(
    communityChannelUserUserGroupListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelUserUserGroupListRequest** | **CommunityChannelUserUserGroupListRequest**|  | |


### Return type

**CommunityChannelUserUserGroupListResponse**

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

# **listCommunitySubchannels**
> CommunitySubchannelListResponse listCommunitySubchannels(communitySubchannelListRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunitySubchannelListRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communitySubchannelListRequest: CommunitySubchannelListRequest; //

const { status, data } = await apiInstance.listCommunitySubchannels(
    communitySubchannelListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communitySubchannelListRequest** | **CommunitySubchannelListRequest**|  | |


### Return type

**CommunitySubchannelListResponse**

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

# **listCommunityUserSubchannels**
> CommunityUserSubchannelListResponse listCommunityUserSubchannels(communityUserSubchannelListRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityUserSubchannelListRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityUserSubchannelListRequest: CommunityUserSubchannelListRequest; //

const { status, data } = await apiInstance.listCommunityUserSubchannels(
    communityUserSubchannelListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityUserSubchannelListRequest** | **CommunityUserSubchannelListRequest**|  | |


### Return type

**CommunityUserSubchannelListResponse**

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

# **listPrivateSubchannelMembers**
> CommunityPrivateSubchannelMemberListResponse listPrivateSubchannelMembers(communityPrivateSubchannelMemberListRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityPrivateSubchannelMemberListRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityPrivateSubchannelMemberListRequest: CommunityPrivateSubchannelMemberListRequest; //

const { status, data } = await apiInstance.listPrivateSubchannelMembers(
    communityPrivateSubchannelMemberListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityPrivateSubchannelMemberListRequest** | **CommunityPrivateSubchannelMemberListRequest**|  | |


### Return type

**CommunityPrivateSubchannelMemberListResponse**

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

# **quitCommunityChannel**
> CodeOnlyResponse quitCommunityChannel(communityChannelMemberRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelMemberRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelMemberRequest: CommunityChannelMemberRequest; //

const { status, data } = await apiInstance.quitCommunityChannel(
    communityChannelMemberRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMemberRequest** | **CommunityChannelMemberRequest**|  | |


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

# **removeCommunityChannelUserGroupUsers**
> CodeOnlyResponse removeCommunityChannelUserGroupUsers(communityChannelUserGroupUsersRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelUserGroupUsersRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelUserGroupUsersRequest: CommunityChannelUserGroupUsersRequest; //

const { status, data } = await apiInstance.removeCommunityChannelUserGroupUsers(
    communityChannelUserGroupUsersRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelUserGroupUsersRequest** | **CommunityChannelUserGroupUsersRequest**|  | |


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

# **removeCommunityChannelUserGroups**
> CodeOnlyResponse removeCommunityChannelUserGroups(communityChannelUserGroupDeleteRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelUserGroupDeleteRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelUserGroupDeleteRequest: CommunityChannelUserGroupDeleteRequest; //

const { status, data } = await apiInstance.removeCommunityChannelUserGroups(
    communityChannelUserGroupDeleteRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelUserGroupDeleteRequest** | **CommunityChannelUserGroupDeleteRequest**|  | |


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

# **removePrivateSubchannelMembers**
> CodeOnlyResponse removePrivateSubchannelMembers(communityPrivateSubchannelMembersRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityPrivateSubchannelMembersRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityPrivateSubchannelMembersRequest: CommunityPrivateSubchannelMembersRequest; //

const { status, data } = await apiInstance.removePrivateSubchannelMembers(
    communityPrivateSubchannelMembersRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityPrivateSubchannelMembersRequest** | **CommunityPrivateSubchannelMembersRequest**|  | |


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

# **unbindCommunityChannelUserGroup**
> CodeOnlyResponse unbindCommunityChannelUserGroup(communityChannelUserGroupBindingRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelUserGroupBindingRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelUserGroupBindingRequest: CommunityChannelUserGroupBindingRequest; //

const { status, data } = await apiInstance.unbindCommunityChannelUserGroup(
    communityChannelUserGroupBindingRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelUserGroupBindingRequest** | **CommunityChannelUserGroupBindingRequest**|  | |


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

# **updateCommunityChannelInfo**
> CodeOnlyResponse updateCommunityChannelInfo(communityChannelUpdateRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunityChannelUpdateRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communityChannelUpdateRequest: CommunityChannelUpdateRequest; //

const { status, data } = await apiInstance.updateCommunityChannelInfo(
    communityChannelUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelUpdateRequest** | **CommunityChannelUpdateRequest**|  | |


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

# **updateCommunitySubchannelType**
> CodeOnlyResponse updateCommunitySubchannelType(communitySubchannelTypeUpdateRequest)


### Example

```typescript
import {
    CommunityChannelManagementApi,
    Configuration,
    CommunitySubchannelTypeUpdateRequest
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
const apiInstance = new CommunityChannelManagementApi(configuration);

let communitySubchannelTypeUpdateRequest: CommunitySubchannelTypeUpdateRequest; //

const { status, data } = await apiInstance.updateCommunitySubchannelType(
    communitySubchannelTypeUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communitySubchannelTypeUpdateRequest** | **CommunitySubchannelTypeUpdateRequest**|  | |


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

