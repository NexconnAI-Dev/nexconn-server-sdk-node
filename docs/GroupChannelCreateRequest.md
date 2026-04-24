# GroupChannelCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channelId** | **string** | Legacy &#x60;groupId&#x60;. | [default to undefined]
**name** | **string** |  | [default to undefined]
**owner** | **string** | Group owner user ID. | [default to undefined]
**userIds** | **Array&lt;string&gt;** | Invited user IDs. The PDF limits this array to 30 users per request. | [optional] [default to undefined]
**groupProfile** | **{ [key: string]: any; }** | Group basic profile object. Common keys include &#x60;introduction&#x60;, &#x60;announcement&#x60;, and &#x60;portraitUrl&#x60;. | [optional] [default to undefined]
**permissions** | **{ [key: string]: any; }** | Group permission object defined by the source API. | [optional] [default to undefined]
**groupExtProfile** | **{ [key: string]: any; }** | Group extra profile object. Keys must start with &#x60;ext_&#x60; according to the PDF. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelCreateRequest } from 'nexconn-sdk-node';

const instance: GroupChannelCreateRequest = {
    channelId,
    name,
    owner,
    userIds,
    groupProfile,
    permissions,
    groupExtProfile,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
