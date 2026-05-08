# OpenChannelParticipantsModerationApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addOpenChannelFreezeList**](#addopenchannelfreezelist) | **POST** /v4/open-channel/freeze-list/add | Freeze an open channel|
|[**addOpenChannelGlobalMuteList**](#addopenchannelglobalmutelist) | **POST** /v4/open-channel/global-mute-list/add | Mute a user globally|
|[**addOpenChannelParticipantAllowedSenderList**](#addopenchannelparticipantallowedsenderlist) | **POST** /v4/open-channel/participant/allowed-sender-list/add | Add to allowed senders list|
|[**addOpenChannelParticipantBanList**](#addopenchannelparticipantbanlist) | **POST** /v4/open-channel/participant/ban-list/add | Ban a participant|
|[**addOpenChannelParticipantMuteList**](#addopenchannelparticipantmutelist) | **POST** /v4/open-channel/participant/mute-list/add | Mute a participant|
|[**checkOpenChannelFreeze**](#checkopenchannelfreeze) | **POST** /v4/open-channel/freeze/check | Check open channel freeze status|
|[**checkOpenChannelParticipantsExist**](#checkopenchannelparticipantsexist) | **POST** /v4/open-channel/participant/exist | Batch check participants|
|[**getOpenChannelGlobalMuteList**](#getopenchannelglobalmutelist) | **POST** /v4/open-channel/global-mute-list/get | List globally muted users|
|[**getOpenChannelParticipantAllowedSenderList**](#getopenchannelparticipantallowedsenderlist) | **POST** /v4/open-channel/participant/allowed-sender-list/get | Query allowed senders list|
|[**getOpenChannelParticipantBanList**](#getopenchannelparticipantbanlist) | **POST** /v4/open-channel/participant/ban-list/get | List banned participants|
|[**getOpenChannelParticipantMuteList**](#getopenchannelparticipantmutelist) | **POST** /v4/open-channel/participant/mute-list/get | List muted participants|
|[**listFrozenOpenChannels**](#listfrozenopenchannels) | **POST** /v4/open-channel/freeze-list/get | List frozen open channels|
|[**listOpenChannelParticipants**](#listopenchannelparticipants) | **POST** /v4/open-channel/participant/list | List participants|
|[**removeOpenChannelFreezeList**](#removeopenchannelfreezelist) | **POST** /v4/open-channel/freeze-list/remove | Unfreeze an open channel|
|[**removeOpenChannelGlobalMuteList**](#removeopenchannelglobalmutelist) | **POST** /v4/open-channel/global-mute-list/remove | Unmute a user globally|
|[**removeOpenChannelParticipantAllowedSenderList**](#removeopenchannelparticipantallowedsenderlist) | **POST** /v4/open-channel/participant/allowed-sender-list/remove | Remove from allowed senders list|
|[**removeOpenChannelParticipantBanList**](#removeopenchannelparticipantbanlist) | **POST** /v4/open-channel/participant/ban-list/remove | Unban a participant|
|[**removeOpenChannelParticipantMuteList**](#removeopenchannelparticipantmutelist) | **POST** /v4/open-channel/participant/mute-list/remove | Unmute a participant|

# **addOpenChannelFreezeList**
> CodeOnlyResponse addOpenChannelFreezeList(openChannelFreezeListUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelFreezeListUpdateRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelFreezeListUpdateRequest: OpenChannelFreezeListUpdateRequest; //

const { status, data } = await apiInstance.addOpenChannelFreezeList(
    openChannelFreezeListUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelFreezeListUpdateRequest** | **OpenChannelFreezeListUpdateRequest**|  | |


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

# **addOpenChannelGlobalMuteList**
> CodeOnlyResponse addOpenChannelGlobalMuteList(openChannelGlobalMuteListAddRequest)

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/global-mute-list/add`.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelGlobalMuteListAddRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelGlobalMuteListAddRequest: OpenChannelGlobalMuteListAddRequest; //

const { status, data } = await apiInstance.addOpenChannelGlobalMuteList(
    openChannelGlobalMuteListAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelGlobalMuteListAddRequest** | **OpenChannelGlobalMuteListAddRequest**|  | |


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

# **addOpenChannelParticipantAllowedSenderList**
> CodeOnlyResponse addOpenChannelParticipantAllowedSenderList(openChannelAllowedSenderListUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelAllowedSenderListUpdateRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelAllowedSenderListUpdateRequest: OpenChannelAllowedSenderListUpdateRequest; //

const { status, data } = await apiInstance.addOpenChannelParticipantAllowedSenderList(
    openChannelAllowedSenderListUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelAllowedSenderListUpdateRequest** | **OpenChannelAllowedSenderListUpdateRequest**|  | |


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

# **addOpenChannelParticipantBanList**
> CodeOnlyResponse addOpenChannelParticipantBanList(openChannelParticipantMuteListAddRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelParticipantMuteListAddRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelParticipantMuteListAddRequest: OpenChannelParticipantMuteListAddRequest; //

const { status, data } = await apiInstance.addOpenChannelParticipantBanList(
    openChannelParticipantMuteListAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantMuteListAddRequest** | **OpenChannelParticipantMuteListAddRequest**|  | |


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

# **addOpenChannelParticipantMuteList**
> CodeOnlyResponse addOpenChannelParticipantMuteList(openChannelParticipantMuteListAddRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelParticipantMuteListAddRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelParticipantMuteListAddRequest: OpenChannelParticipantMuteListAddRequest; //

const { status, data } = await apiInstance.addOpenChannelParticipantMuteList(
    openChannelParticipantMuteListAddRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantMuteListAddRequest** | **OpenChannelParticipantMuteListAddRequest**|  | |


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

# **checkOpenChannelFreeze**
> OpenChannelFreezeCheckResponse checkOpenChannelFreeze(openChannelFreezeCheckRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelFreezeCheckRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelFreezeCheckRequest: OpenChannelFreezeCheckRequest; //

const { status, data } = await apiInstance.checkOpenChannelFreeze(
    openChannelFreezeCheckRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelFreezeCheckRequest** | **OpenChannelFreezeCheckRequest**|  | |


### Return type

**OpenChannelFreezeCheckResponse**

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

# **checkOpenChannelParticipantsExist**
> OpenChannelParticipantExistResponse checkOpenChannelParticipantsExist(openChannelParticipantExistRequest)

Rate limit: 100/sec. The same endpoint is also documented for single-user participant checks.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelParticipantExistRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelParticipantExistRequest: OpenChannelParticipantExistRequest; //

const { status, data } = await apiInstance.checkOpenChannelParticipantsExist(
    openChannelParticipantExistRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantExistRequest** | **OpenChannelParticipantExistRequest**|  | |


### Return type

**OpenChannelParticipantExistResponse**

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

# **getOpenChannelGlobalMuteList**
> OpenChannelParticipantMuteListGetResponse getOpenChannelGlobalMuteList()

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/global-mute-list/get`.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);
const { status, data } = await apiInstance.getOpenChannelGlobalMuteList();

```

### Parameters
This endpoint does not require a request body.

### Return type

**OpenChannelParticipantMuteListGetResponse**

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

# **getOpenChannelParticipantAllowedSenderList**
> OpenChannelAllowedSenderListGetResponse getOpenChannelParticipantAllowedSenderList(openChannelParticipantListByChannelRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelParticipantListByChannelRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelParticipantListByChannelRequest: OpenChannelParticipantListByChannelRequest; //

const { status, data } = await apiInstance.getOpenChannelParticipantAllowedSenderList(
    openChannelParticipantListByChannelRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantListByChannelRequest** | **OpenChannelParticipantListByChannelRequest**|  | |


### Return type

**OpenChannelAllowedSenderListGetResponse**

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

# **getOpenChannelParticipantBanList**
> OpenChannelParticipantBanListGetResponse getOpenChannelParticipantBanList(openChannelParticipantListByChannelRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelParticipantListByChannelRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelParticipantListByChannelRequest: OpenChannelParticipantListByChannelRequest; //

const { status, data } = await apiInstance.getOpenChannelParticipantBanList(
    openChannelParticipantListByChannelRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantListByChannelRequest** | **OpenChannelParticipantListByChannelRequest**|  | |


### Return type

**OpenChannelParticipantBanListGetResponse**

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

# **getOpenChannelParticipantMuteList**
> OpenChannelParticipantMuteListGetResponse getOpenChannelParticipantMuteList(openChannelParticipantListByChannelRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelParticipantListByChannelRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelParticipantListByChannelRequest: OpenChannelParticipantListByChannelRequest; //

const { status, data } = await apiInstance.getOpenChannelParticipantMuteList(
    openChannelParticipantListByChannelRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantListByChannelRequest** | **OpenChannelParticipantListByChannelRequest**|  | |


### Return type

**OpenChannelParticipantMuteListGetResponse**

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

# **listFrozenOpenChannels**
> OpenChannelFreezeListGetResponse listFrozenOpenChannels(openChannelFreezeListGetRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelFreezeListGetRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelFreezeListGetRequest: OpenChannelFreezeListGetRequest; //

const { status, data } = await apiInstance.listFrozenOpenChannels(
    openChannelFreezeListGetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelFreezeListGetRequest** | **OpenChannelFreezeListGetRequest**|  | |


### Return type

**OpenChannelFreezeListGetResponse**

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

# **listOpenChannelParticipants**
> OpenChannelParticipantListResponse listOpenChannelParticipants(openChannelParticipantListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelParticipantListRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelParticipantListRequest: OpenChannelParticipantListRequest; //

const { status, data } = await apiInstance.listOpenChannelParticipants(
    openChannelParticipantListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantListRequest** | **OpenChannelParticipantListRequest**|  | |


### Return type

**OpenChannelParticipantListResponse**

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

# **removeOpenChannelFreezeList**
> CodeOnlyResponse removeOpenChannelFreezeList(openChannelFreezeListUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelFreezeListUpdateRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelFreezeListUpdateRequest: OpenChannelFreezeListUpdateRequest; //

const { status, data } = await apiInstance.removeOpenChannelFreezeList(
    openChannelFreezeListUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelFreezeListUpdateRequest** | **OpenChannelFreezeListUpdateRequest**|  | |


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

# **removeOpenChannelGlobalMuteList**
> CodeOnlyResponse removeOpenChannelGlobalMuteList(openChannelGlobalMuteListRemoveRequest)

Rate limit: 100/sec. The public endpoint list currently publishes this capability as `/v4/open-channel/participant/global-mute-list/remove`.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelGlobalMuteListRemoveRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelGlobalMuteListRemoveRequest: OpenChannelGlobalMuteListRemoveRequest; //

const { status, data } = await apiInstance.removeOpenChannelGlobalMuteList(
    openChannelGlobalMuteListRemoveRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelGlobalMuteListRemoveRequest** | **OpenChannelGlobalMuteListRemoveRequest**|  | |


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

# **removeOpenChannelParticipantAllowedSenderList**
> CodeOnlyResponse removeOpenChannelParticipantAllowedSenderList(openChannelAllowedSenderListUpdateRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelAllowedSenderListUpdateRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelAllowedSenderListUpdateRequest: OpenChannelAllowedSenderListUpdateRequest; //

const { status, data } = await apiInstance.removeOpenChannelParticipantAllowedSenderList(
    openChannelAllowedSenderListUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelAllowedSenderListUpdateRequest** | **OpenChannelAllowedSenderListUpdateRequest**|  | |


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

# **removeOpenChannelParticipantBanList**
> CodeOnlyResponse removeOpenChannelParticipantBanList(openChannelParticipantMuteListRemoveRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelParticipantMuteListRemoveRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelParticipantMuteListRemoveRequest: OpenChannelParticipantMuteListRemoveRequest; //

const { status, data } = await apiInstance.removeOpenChannelParticipantBanList(
    openChannelParticipantMuteListRemoveRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantMuteListRemoveRequest** | **OpenChannelParticipantMuteListRemoveRequest**|  | |


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

# **removeOpenChannelParticipantMuteList**
> CodeOnlyResponse removeOpenChannelParticipantMuteList(openChannelParticipantMuteListRemoveRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    OpenChannelParticipantsModerationApi,
    Configuration,
    OpenChannelParticipantMuteListRemoveRequest
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
const apiInstance = new OpenChannelParticipantsModerationApi(configuration);

let openChannelParticipantMuteListRemoveRequest: OpenChannelParticipantMuteListRemoveRequest; //

const { status, data } = await apiInstance.removeOpenChannelParticipantMuteList(
    openChannelParticipantMuteListRemoveRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelParticipantMuteListRemoveRequest** | **OpenChannelParticipantMuteListRemoveRequest**|  | |


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

