# CommunityChannelModerationApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addCommunityChannelAllowedSenderList**](#addcommunitychannelallowedsenderlist) | **POST** /v4/community-channel/allowed-sender-list/add | Add community channel allowed sender list|
|[**addCommunityChannelMutedUsers**](#addcommunitychannelmutedusers) | **POST** /v4/community-channel/mute-list/add | Add community-channel muted users|
|[**getCommunityChannelFreezeList**](#getcommunitychannelfreezelist) | **POST** /v4/community-channel/freeze-list/get | Get community channel freeze status|
|[**listCommunityChannelAllowedSenderList**](#listcommunitychannelallowedsenderlist) | **POST** /v4/community-channel/allowed-sender-list/get | List community channel allowed sender list|
|[**listCommunityChannelMutedUsers**](#listcommunitychannelmutedusers) | **POST** /v4/community-channel/mute-list/get | List community-channel muted users|
|[**removeCommunityChannelAllowedSenderList**](#removecommunitychannelallowedsenderlist) | **POST** /v4/community-channel/allowed-sender-list/remove | Remove community channel allowed sender list|
|[**removeCommunityChannelMutedUsers**](#removecommunitychannelmutedusers) | **POST** /v4/community-channel/mute-list/remove | Remove community-channel muted users|
|[**setCommunityChannelFreezeList**](#setcommunitychannelfreezelist) | **POST** /v4/community-channel/freeze-list/set | Set community channel freeze list|

# **addCommunityChannelAllowedSenderList**
> CodeOnlyResponse addCommunityChannelAllowedSenderList(communityChannelAllowedSenderListUpdateRequest)


### Example

```typescript
import {
    CommunityChannelModerationApi,
    Configuration,
    CommunityChannelAllowedSenderListUpdateRequest
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
const apiInstance = new CommunityChannelModerationApi(configuration);

let communityChannelAllowedSenderListUpdateRequest: CommunityChannelAllowedSenderListUpdateRequest; //

const { status, data } = await apiInstance.addCommunityChannelAllowedSenderList(
    communityChannelAllowedSenderListUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelAllowedSenderListUpdateRequest** | **CommunityChannelAllowedSenderListUpdateRequest**|  | |


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

# **addCommunityChannelMutedUsers**
> CodeOnlyResponse addCommunityChannelMutedUsers(communityChannelMuteListAddRequest)


### Example

```typescript
import {
    CommunityChannelModerationApi,
    Configuration,
    CommunityChannelMuteListAddRequest
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
const apiInstance = new CommunityChannelModerationApi(configuration);

let communityChannelMuteListAddRequest: CommunityChannelMuteListAddRequest; //

const { status, data } = await apiInstance.addCommunityChannelMutedUsers(
    communityChannelMuteListAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMuteListAddRequest** | **CommunityChannelMuteListAddRequest**|  | |


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

# **getCommunityChannelFreezeList**
> CommunityChannelFreezeListGetResponse getCommunityChannelFreezeList(communityChannelFreezeListGetRequest)


### Example

```typescript
import {
    CommunityChannelModerationApi,
    Configuration,
    CommunityChannelFreezeListGetRequest
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
const apiInstance = new CommunityChannelModerationApi(configuration);

let communityChannelFreezeListGetRequest: CommunityChannelFreezeListGetRequest; //

const { status, data } = await apiInstance.getCommunityChannelFreezeList(
    communityChannelFreezeListGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelFreezeListGetRequest** | **CommunityChannelFreezeListGetRequest**|  | |


### Return type

**CommunityChannelFreezeListGetResponse**

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

# **listCommunityChannelAllowedSenderList**
> CommunityChannelAllowedSenderListGetResponse listCommunityChannelAllowedSenderList(communityChannelAllowedSenderListGetRequest)


### Example

```typescript
import {
    CommunityChannelModerationApi,
    Configuration,
    CommunityChannelAllowedSenderListGetRequest
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
const apiInstance = new CommunityChannelModerationApi(configuration);

let communityChannelAllowedSenderListGetRequest: CommunityChannelAllowedSenderListGetRequest; //

const { status, data } = await apiInstance.listCommunityChannelAllowedSenderList(
    communityChannelAllowedSenderListGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelAllowedSenderListGetRequest** | **CommunityChannelAllowedSenderListGetRequest**|  | |


### Return type

**CommunityChannelAllowedSenderListGetResponse**

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

# **listCommunityChannelMutedUsers**
> CommunityChannelMuteListGetResponse listCommunityChannelMutedUsers(communityChannelMuteListGetRequest)


### Example

```typescript
import {
    CommunityChannelModerationApi,
    Configuration,
    CommunityChannelMuteListGetRequest
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
const apiInstance = new CommunityChannelModerationApi(configuration);

let communityChannelMuteListGetRequest: CommunityChannelMuteListGetRequest; //

const { status, data } = await apiInstance.listCommunityChannelMutedUsers(
    communityChannelMuteListGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMuteListGetRequest** | **CommunityChannelMuteListGetRequest**|  | |


### Return type

**CommunityChannelMuteListGetResponse**

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

# **removeCommunityChannelAllowedSenderList**
> CodeOnlyResponse removeCommunityChannelAllowedSenderList(communityChannelAllowedSenderListUpdateRequest)


### Example

```typescript
import {
    CommunityChannelModerationApi,
    Configuration,
    CommunityChannelAllowedSenderListUpdateRequest
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
const apiInstance = new CommunityChannelModerationApi(configuration);

let communityChannelAllowedSenderListUpdateRequest: CommunityChannelAllowedSenderListUpdateRequest; //

const { status, data } = await apiInstance.removeCommunityChannelAllowedSenderList(
    communityChannelAllowedSenderListUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelAllowedSenderListUpdateRequest** | **CommunityChannelAllowedSenderListUpdateRequest**|  | |


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

# **removeCommunityChannelMutedUsers**
> CodeOnlyResponse removeCommunityChannelMutedUsers(communityChannelMuteListRemoveRequest)


### Example

```typescript
import {
    CommunityChannelModerationApi,
    Configuration,
    CommunityChannelMuteListRemoveRequest
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
const apiInstance = new CommunityChannelModerationApi(configuration);

let communityChannelMuteListRemoveRequest: CommunityChannelMuteListRemoveRequest; //

const { status, data } = await apiInstance.removeCommunityChannelMutedUsers(
    communityChannelMuteListRemoveRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMuteListRemoveRequest** | **CommunityChannelMuteListRemoveRequest**|  | |


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

# **setCommunityChannelFreezeList**
> CodeOnlyResponse setCommunityChannelFreezeList(communityChannelFreezeListSetRequest)


### Example

```typescript
import {
    CommunityChannelModerationApi,
    Configuration,
    CommunityChannelFreezeListSetRequest
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
const apiInstance = new CommunityChannelModerationApi(configuration);

let communityChannelFreezeListSetRequest: CommunityChannelFreezeListSetRequest; //

const { status, data } = await apiInstance.setCommunityChannelFreezeList(
    communityChannelFreezeListSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelFreezeListSetRequest** | **CommunityChannelFreezeListSetRequest**|  | |


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

