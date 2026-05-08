# ProfanityWordItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**word** | **string** | Profanity word content. | [default to undefined]
**replacement** | **string** | Replacement content. When omitted, messages containing the word are blocked instead of replaced. | [optional] [default to undefined]

## Example

```typescript
import { ProfanityWordItem } from '@nexconn/server-sdk';

const instance: ProfanityWordItem = {
    word,
    replacement,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
