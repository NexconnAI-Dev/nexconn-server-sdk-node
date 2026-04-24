# GroupChannelModerationApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addGroupChannelAllowedSenderList**](#addgroupchannelallowedsenderlist) | **POST** /v4/group-channel/allowed-sender-list/add | Add to allowed senders list|
|[**addGroupChannelFreezeList**](#addgroupchannelfreezelist) | **POST** /v4/group-channel/freeze-list/add | Freeze a group|
|[**addGroupChannelUserMuteList**](#addgroupchannelusermutelist) | **POST** /v4/group-channel/user/mute-list/add | Mute a group member|
|[**getGroupChannelAllowedSenderList**](#getgroupchannelallowedsenderlist) | **POST** /v4/group-channel/allowed-sender-list/get | Query allowed senders list|
|[**getGroupChannelFreezeList**](#getgroupchannelfreezelist) | **POST** /v4/group-channel/freeze-list/get | Query group freeze status|
|[**getGroupChannelUserMuteList**](#getgroupchannelusermutelist) | **POST** /v4/group-channel/user/mute-list/get | List muted group members|
|[**removeGroupChannelAllowedSenderList**](#removegroupchannelallowedsenderlist) | **POST** /v4/group-channel/allowed-sender-list/remove | Remove from allowed senders list|
|[**removeGroupChannelFreezeList**](#removegroupchannelfreezelist) | **POST** /v4/group-channel/freeze-list/remove | Unfreeze a group|
|[**removeGroupChannelUserMuteList**](#removegroupchannelusermutelist) | **POST** /v4/group-channel/user/mute-list/remove | Unmute a group member|

# **addGroupChannelAllowedSenderList**
> CodeOnlyResponse addGroupChannelAllowedSenderList(groupChannelAllowedSenderListUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelModerationApi,
    Configuration,
    GroupChannelAllowedSenderListUpdateRequest
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
const apiInstance = new GroupChannelModerationApi(configuration);

let groupChannelAllowedSenderListUpdateRequest: GroupChannelAllowedSenderListUpdateRequest; //

const { status, data } = await apiInstance.addGroupChannelAllowedSenderList(
    groupChannelAllowedSenderListUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelAllowedSenderListUpdateRequest** | **GroupChannelAllowedSenderListUpdateRequest**|  | |


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

# **addGroupChannelFreezeList**
> CodeOnlyResponse addGroupChannelFreezeList(groupChannelFreezeListUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelModerationApi,
    Configuration,
    GroupChannelFreezeListUpdateRequest
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
const apiInstance = new GroupChannelModerationApi(configuration);

let groupChannelFreezeListUpdateRequest: GroupChannelFreezeListUpdateRequest; //

const { status, data } = await apiInstance.addGroupChannelFreezeList(
    groupChannelFreezeListUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelFreezeListUpdateRequest** | **GroupChannelFreezeListUpdateRequest**|  | |


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

# **addGroupChannelUserMuteList**
> CodeOnlyResponse addGroupChannelUserMuteList(groupChannelUserMuteListAddRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelModerationApi,
    Configuration,
    GroupChannelUserMuteListAddRequest
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
const apiInstance = new GroupChannelModerationApi(configuration);

let groupChannelUserMuteListAddRequest: GroupChannelUserMuteListAddRequest; //

const { status, data } = await apiInstance.addGroupChannelUserMuteList(
    groupChannelUserMuteListAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelUserMuteListAddRequest** | **GroupChannelUserMuteListAddRequest**|  | |


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

# **getGroupChannelAllowedSenderList**
> GroupChannelAllowedSenderListGetResponse getGroupChannelAllowedSenderList(groupChannelAllowedSenderListGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelModerationApi,
    Configuration,
    GroupChannelAllowedSenderListGetRequest
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
const apiInstance = new GroupChannelModerationApi(configuration);

let groupChannelAllowedSenderListGetRequest: GroupChannelAllowedSenderListGetRequest; //

const { status, data } = await apiInstance.getGroupChannelAllowedSenderList(
    groupChannelAllowedSenderListGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelAllowedSenderListGetRequest** | **GroupChannelAllowedSenderListGetRequest**|  | |


### Return type

**GroupChannelAllowedSenderListGetResponse**

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

# **getGroupChannelFreezeList**
> GroupChannelFreezeListGetResponse getGroupChannelFreezeList(groupChannelFreezeListGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelModerationApi,
    Configuration,
    GroupChannelFreezeListGetRequest
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
const apiInstance = new GroupChannelModerationApi(configuration);

let groupChannelFreezeListGetRequest: GroupChannelFreezeListGetRequest; //

const { status, data } = await apiInstance.getGroupChannelFreezeList(
    groupChannelFreezeListGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelFreezeListGetRequest** | **GroupChannelFreezeListGetRequest**|  | |


### Return type

**GroupChannelFreezeListGetResponse**

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

# **getGroupChannelUserMuteList**
> GroupChannelUserMuteListGetResponse getGroupChannelUserMuteList(groupChannelUserMuteListGetRequest)

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/group-channel/user/mute-list-get`.

### Example

```typescript
import {
    GroupChannelModerationApi,
    Configuration,
    GroupChannelUserMuteListGetRequest
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
const apiInstance = new GroupChannelModerationApi(configuration);

let groupChannelUserMuteListGetRequest: GroupChannelUserMuteListGetRequest; //

const { status, data } = await apiInstance.getGroupChannelUserMuteList(
    groupChannelUserMuteListGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelUserMuteListGetRequest** | **GroupChannelUserMuteListGetRequest**|  | |


### Return type

**GroupChannelUserMuteListGetResponse**

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

# **removeGroupChannelAllowedSenderList**
> CodeOnlyResponse removeGroupChannelAllowedSenderList(groupChannelAllowedSenderListUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelModerationApi,
    Configuration,
    GroupChannelAllowedSenderListUpdateRequest
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
const apiInstance = new GroupChannelModerationApi(configuration);

let groupChannelAllowedSenderListUpdateRequest: GroupChannelAllowedSenderListUpdateRequest; //

const { status, data } = await apiInstance.removeGroupChannelAllowedSenderList(
    groupChannelAllowedSenderListUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelAllowedSenderListUpdateRequest** | **GroupChannelAllowedSenderListUpdateRequest**|  | |


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

# **removeGroupChannelFreezeList**
> CodeOnlyResponse removeGroupChannelFreezeList(groupChannelFreezeListUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelModerationApi,
    Configuration,
    GroupChannelFreezeListUpdateRequest
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
const apiInstance = new GroupChannelModerationApi(configuration);

let groupChannelFreezeListUpdateRequest: GroupChannelFreezeListUpdateRequest; //

const { status, data } = await apiInstance.removeGroupChannelFreezeList(
    groupChannelFreezeListUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelFreezeListUpdateRequest** | **GroupChannelFreezeListUpdateRequest**|  | |


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

# **removeGroupChannelUserMuteList**
> CodeOnlyResponse removeGroupChannelUserMuteList(groupChannelUserMuteListRemoveRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    GroupChannelModerationApi,
    Configuration,
    GroupChannelUserMuteListRemoveRequest
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
const apiInstance = new GroupChannelModerationApi(configuration);

let groupChannelUserMuteListRemoveRequest: GroupChannelUserMuteListRemoveRequest; //

const { status, data } = await apiInstance.removeGroupChannelUserMuteList(
    groupChannelUserMuteListRemoveRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelUserMuteListRemoveRequest** | **GroupChannelUserMuteListRemoveRequest**|  | |


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

