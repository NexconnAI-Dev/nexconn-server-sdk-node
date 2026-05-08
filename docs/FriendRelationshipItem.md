# FriendRelationshipItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**userId** | **string** |  | [optional] [default to undefined]
**result** | **number** | Friend relationship result defined by the source API. &#x60;1&#x60; means both users are not friends, &#x60;2&#x60; and &#x60;3&#x60; are reserved, and &#x60;4&#x60; means the friendship is mutual.  | [optional] [default to undefined]

## Example

```typescript
import { FriendRelationshipItem } from '@nexconn/server-sdk';

const instance: FriendRelationshipItem = {
    userId,
    result,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
