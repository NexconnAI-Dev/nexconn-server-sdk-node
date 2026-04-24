# ProfanityWordListedItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**word** | **string** | Profanity word content. | [optional] [default to undefined]
**replacement** | **string** | Replacement content. Empty means the word is blocked. | [optional] [default to undefined]
**filterType** | **string** | Result type. &#x60;0&#x60; means replacement word and &#x60;1&#x60; means blocked word. | [optional] [default to undefined]

## Example

```typescript
import { ProfanityWordListedItem } from 'nexconn-sdk-node';

const instance: ProfanityWordListedItem = {
    word,
    replacement,
    filterType,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
