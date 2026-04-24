# MessageManagementApi

All requests use the primary/backup domains configured by the caller.

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**broadcastOpenChannelMessage**](#broadcastopenchannelmessage) | **POST** /v4/open-channel/message/broadcast | Broadcast to all open channels|
|[**deleteChannelMessageHistory**](#deletechannelmessagehistory) | **POST** /v4/channel/message/history/delete | Delete server-side channel message history|
|[**deleteChannelTypeMessageMetadata**](#deletechanneltypemessagemetadata) | **POST** /v4/channel-type/message/metadata/delete | Delete message metadata|
|[**deleteCommunityChannelMessageMetadata**](#deletecommunitychannelmessagemetadata) | **POST** /v4/community-channel/message/metadata/delete | Delete community-channel message metadata keys|
|[**deleteMessage**](#deletemessage) | **POST** /v4/message/delete | Delete a message (recall)|
|[**listChannelTypeMessageMetadata**](#listchanneltypemessagemetadata) | **POST** /v4/channel-type/message/metadata/list | Get message metadata|
|[**listCommunityChannelMessageMetadata**](#listcommunitychannelmessagemetadata) | **POST** /v4/community-channel/message/metadata/list | List community-channel message metadata|
|[**sendCommunityChannelMessage**](#sendcommunitychannelmessage) | **POST** /v4/community-channel/message/send | Send a community channel message|
|[**sendDirectChannelMessage**](#senddirectchannelmessage) | **POST** /v4/direct-channel/message/send | Send a direct message|
|[**sendGroupChannelMessage**](#sendgroupchannelmessage) | **POST** /v4/group-channel/message/send | Send a group message|
|[**sendOpenChannelMessage**](#sendopenchannelmessage) | **POST** /v4/open-channel/message/send | Send an open channel message|
|[**setChannelTypeMessageMetadata**](#setchanneltypemessagemetadata) | **POST** /v4/channel-type/message/metadata/set | Set message metadata|
|[**setCommunityChannelMessageMetadata**](#setcommunitychannelmessagemetadata) | **POST** /v4/community-channel/message/metadata/set | Set community-channel message metadata|
|[**updateCommunityChannelMessage**](#updatecommunitychannelmessage) | **POST** /v4/community-channel/message/update | Update community-channel message|
|[**updateDirectChannelMessage**](#updatedirectchannelmessage) | **POST** /v4/direct-channel/message/update | Update direct-channel message|
|[**updateGroupChannelMessage**](#updategroupchannelmessage) | **POST** /v4/group-channel/message/update | Update group-channel message|

# **broadcastOpenChannelMessage**
> CodeOnlyResponse broadcastOpenChannelMessage(openChannelBroadcastRequest)

Rate limit: 1/sec.

### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    OpenChannelBroadcastRequest
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
const apiInstance = new MessageManagementApi(configuration);

let openChannelBroadcastRequest: OpenChannelBroadcastRequest; //

const { status, data } = await apiInstance.broadcastOpenChannelMessage(
    openChannelBroadcastRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelBroadcastRequest** | **OpenChannelBroadcastRequest**|  | |


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

# **deleteChannelMessageHistory**
> CodeOnlyResponse deleteChannelMessageHistory(channelMessageHistoryDeleteRequest)

Rate limit: 100/sec. Server path `/v4/channel/message/history/delete` (`HistoryCleanInput`).

### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    ChannelMessageHistoryDeleteRequest
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
const apiInstance = new MessageManagementApi(configuration);

let channelMessageHistoryDeleteRequest: ChannelMessageHistoryDeleteRequest; //

const { status, data } = await apiInstance.deleteChannelMessageHistory(
    channelMessageHistoryDeleteRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelMessageHistoryDeleteRequest** | **ChannelMessageHistoryDeleteRequest**|  | |


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

# **deleteChannelTypeMessageMetadata**
> CodeOnlyResponse deleteChannelTypeMessageMetadata(channelTypeMessageMetadataDeleteRequest)

Rate limit: 100/sec (max 20 for group messages).

### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    ChannelTypeMessageMetadataDeleteRequest
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
const apiInstance = new MessageManagementApi(configuration);

let channelTypeMessageMetadataDeleteRequest: ChannelTypeMessageMetadataDeleteRequest; //

const { status, data } = await apiInstance.deleteChannelTypeMessageMetadata(
    channelTypeMessageMetadataDeleteRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelTypeMessageMetadataDeleteRequest** | **ChannelTypeMessageMetadataDeleteRequest**|  | |


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

# **deleteCommunityChannelMessageMetadata**
> CodeOnlyResponse deleteCommunityChannelMessageMetadata(communityChannelMessageMetadataDeleteRequest)


### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    CommunityChannelMessageMetadataDeleteRequest
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
const apiInstance = new MessageManagementApi(configuration);

let communityChannelMessageMetadataDeleteRequest: CommunityChannelMessageMetadataDeleteRequest; //

const { status, data } = await apiInstance.deleteCommunityChannelMessageMetadata(
    communityChannelMessageMetadataDeleteRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMessageMetadataDeleteRequest** | **CommunityChannelMessageMetadataDeleteRequest**|  | |


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

# **deleteMessage**
> CodeOnlyResponse deleteMessage(messageDeleteRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    MessageDeleteRequest
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
const apiInstance = new MessageManagementApi(configuration);

let messageDeleteRequest: MessageDeleteRequest; //

const { status, data } = await apiInstance.deleteMessage(
    messageDeleteRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **messageDeleteRequest** | **MessageDeleteRequest**|  | |


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

# **listChannelTypeMessageMetadata**
> ChannelTypeMessageMetadataListResponse listChannelTypeMessageMetadata(channelTypeMessageMetadataListRequest)

Rate limit: 100/sec.

### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    ChannelTypeMessageMetadataListRequest
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
const apiInstance = new MessageManagementApi(configuration);

let channelTypeMessageMetadataListRequest: ChannelTypeMessageMetadataListRequest; //

const { status, data } = await apiInstance.listChannelTypeMessageMetadata(
    channelTypeMessageMetadataListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **channelTypeMessageMetadataListRequest** | **ChannelTypeMessageMetadataListRequest**|  | |


### Return type

**ChannelTypeMessageMetadataListResponse**

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

# **listCommunityChannelMessageMetadata**
> CommunityChannelMessageMetadataListResponse listCommunityChannelMessageMetadata(communityChannelMessageMetadataListRequest)


### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    CommunityChannelMessageMetadataListRequest
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
const apiInstance = new MessageManagementApi(configuration);

let communityChannelMessageMetadataListRequest: CommunityChannelMessageMetadataListRequest; //

const { status, data } = await apiInstance.listCommunityChannelMessageMetadata(
    communityChannelMessageMetadataListRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMessageMetadataListRequest** | **CommunityChannelMessageMetadataListRequest**|  | |


### Return type

**CommunityChannelMessageMetadataListResponse**

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

# **sendCommunityChannelMessage**
> ChannelMessageSendResponse sendCommunityChannelMessage(communityChannelMessageSendRequest)

Rate limit: 100/sec (by target group count); 20/sec per channel.

### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    CommunityChannelMessageSendRequest
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
const apiInstance = new MessageManagementApi(configuration);

let communityChannelMessageSendRequest: CommunityChannelMessageSendRequest; //

const { status, data } = await apiInstance.sendCommunityChannelMessage(
    communityChannelMessageSendRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMessageSendRequest** | **CommunityChannelMessageSendRequest**|  | |


### Return type

**ChannelMessageSendResponse**

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

# **sendDirectChannelMessage**
> UserMessageSendResponse sendDirectChannelMessage(directChannelMessageSendRequest)

Rate limit: 6,000 msgs/min (by recipient count).

### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    DirectChannelMessageSendRequest
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
const apiInstance = new MessageManagementApi(configuration);

let directChannelMessageSendRequest: DirectChannelMessageSendRequest; //

const { status, data } = await apiInstance.sendDirectChannelMessage(
    directChannelMessageSendRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **directChannelMessageSendRequest** | **DirectChannelMessageSendRequest**|  | |


### Return type

**UserMessageSendResponse**

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

# **sendGroupChannelMessage**
> ChannelMessageSendResponse sendGroupChannelMessage(groupChannelMessageSendRequest)

Rate limit: 20/sec (by target group count).

### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    GroupChannelMessageSendRequest
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
const apiInstance = new MessageManagementApi(configuration);

let groupChannelMessageSendRequest: GroupChannelMessageSendRequest; //

const { status, data } = await apiInstance.sendGroupChannelMessage(
    groupChannelMessageSendRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelMessageSendRequest** | **GroupChannelMessageSendRequest**|  | |


### Return type

**ChannelMessageSendResponse**

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

# **sendOpenChannelMessage**
> ChannelMessageSendResponse sendOpenChannelMessage(openChannelMessageSendRequest)

Rate limit: 100/sec (by target open channel count).

### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    OpenChannelMessageSendRequest
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
const apiInstance = new MessageManagementApi(configuration);

let openChannelMessageSendRequest: OpenChannelMessageSendRequest; //

const { status, data } = await apiInstance.sendOpenChannelMessage(
    openChannelMessageSendRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **openChannelMessageSendRequest** | **OpenChannelMessageSendRequest**|  | |


### Return type

**ChannelMessageSendResponse**

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

# **setChannelTypeMessageMetadata**
> CodeOnlyResponse setChannelTypeMessageMetadata(messageMetadataSetRequest)

Rate limit: 100/sec (max 20 for group messages).

### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    MessageMetadataSetRequest
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
const apiInstance = new MessageManagementApi(configuration);

let messageMetadataSetRequest: MessageMetadataSetRequest; //

const { status, data } = await apiInstance.setChannelTypeMessageMetadata(
    messageMetadataSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **messageMetadataSetRequest** | **MessageMetadataSetRequest**|  | |


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

# **setCommunityChannelMessageMetadata**
> CodeOnlyResponse setCommunityChannelMessageMetadata(communityChannelMessageMetadataSetRequest)


### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    CommunityChannelMessageMetadataSetRequest
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
const apiInstance = new MessageManagementApi(configuration);

let communityChannelMessageMetadataSetRequest: CommunityChannelMessageMetadataSetRequest; //

const { status, data } = await apiInstance.setCommunityChannelMessageMetadata(
    communityChannelMessageMetadataSetRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMessageMetadataSetRequest** | **CommunityChannelMessageMetadataSetRequest**|  | |


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

# **updateCommunityChannelMessage**
> CodeOnlyResponse updateCommunityChannelMessage(communityChannelMessageUpdateRequest)


### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    CommunityChannelMessageUpdateRequest
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
const apiInstance = new MessageManagementApi(configuration);

let communityChannelMessageUpdateRequest: CommunityChannelMessageUpdateRequest; //

const { status, data } = await apiInstance.updateCommunityChannelMessage(
    communityChannelMessageUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **communityChannelMessageUpdateRequest** | **CommunityChannelMessageUpdateRequest**|  | |


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

# **updateDirectChannelMessage**
> CodeOnlyResponse updateDirectChannelMessage(directChannelMessageUpdateRequest)


### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    DirectChannelMessageUpdateRequest
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
const apiInstance = new MessageManagementApi(configuration);

let directChannelMessageUpdateRequest: DirectChannelMessageUpdateRequest; //

const { status, data } = await apiInstance.updateDirectChannelMessage(
    directChannelMessageUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **directChannelMessageUpdateRequest** | **DirectChannelMessageUpdateRequest**|  | |


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

# **updateGroupChannelMessage**
> CodeOnlyResponse updateGroupChannelMessage(groupChannelMessageUpdateRequest)


### Example

```typescript
import {
    MessageManagementApi,
    Configuration,
    GroupChannelMessageUpdateRequest
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
const apiInstance = new MessageManagementApi(configuration);

let groupChannelMessageUpdateRequest: GroupChannelMessageUpdateRequest; //

const { status, data } = await apiInstance.updateGroupChannelMessage(
    groupChannelMessageUpdateRequest
);

```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupChannelMessageUpdateRequest** | **GroupChannelMessageUpdateRequest**|  | |


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

