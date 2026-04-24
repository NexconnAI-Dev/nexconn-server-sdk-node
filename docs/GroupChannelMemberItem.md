# GroupChannelMemberItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** | Member user ID. | [optional] [default to undefined]
**role** | **number** | Member role. &#x60;1&#x60; regular member, &#x60;2&#x60; admin, &#x60;3&#x60; owner. | [optional] [default to undefined]
**nickname** | **string** | Member nickname in the group. | [optional] [default to undefined]
**extra** | **string** | Additional member profile information. | [optional] [default to undefined]
**joinedAt** | **number** | Timestamp when the member joined the group. | [optional] [default to undefined]

## Example

```typescript
import { GroupChannelMemberItem } from 'nexconn-sdk-node';

const instance: GroupChannelMemberItem = {
    userId,
    role,
    nickname,
    extra,
    joinedAt,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
