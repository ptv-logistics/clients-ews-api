
# RoadDistanceResponse


## Properties

Name | Type
------------ | -------------
`distance` | number
`tollDistance` | number
`start` | [ResponseLocation](ResponseLocation.md)
`destination` | [ResponseLocation](ResponseLocation.md)
`dataVersion` | string
`region` | string

## Example

```typescript
import type { RoadDistanceResponse } from ''

// TODO: Update the object below with actual values
const example = {
  "distance": 1422,
  "tollDistance": 985,
  "start": null,
  "destination": null,
  "dataVersion": null,
  "region": null,
} satisfies RoadDistanceResponse

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RoadDistanceResponse
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


