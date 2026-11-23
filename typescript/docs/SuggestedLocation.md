
# SuggestedLocation

A location suggested for the input.

## Properties

Name | Type
------------ | -------------
`country` | string
`postalCode` | string
`locality` | string
`type` | [LocationType](LocationType.md)

## Example

```typescript
import type { SuggestedLocation } from ''

// TODO: Update the object below with actual values
const example = {
  "country": DE,
  "postalCode": 76131,
  "locality": Karlsruhe,
  "type": null,
} satisfies SuggestedLocation

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as SuggestedLocation
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


