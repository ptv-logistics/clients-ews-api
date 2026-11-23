
# ResponseLocation

The complete location used for start or destination of the relation.

## Properties

Name | Type
------------ | -------------
`country` | string
`postalCode` | string
`locality` | string
`latitude` | number
`longitude` | number
`type` | [LocationType](LocationType.md)

## Example

```typescript
import type { ResponseLocation } from ''

// TODO: Update the object below with actual values
const example = {
  "country": DE,
  "postalCode": 76131,
  "locality": Karlsruhe,
  "latitude": 49.013465,
  "longitude": 8.428155,
  "type": null,
} satisfies ResponseLocation

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ResponseLocation
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


