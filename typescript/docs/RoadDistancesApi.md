# RoadDistancesApi

All URIs are relative to *https://api.myptv.com/ews/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getRelation**](RoadDistancesApi.md#getrelation) | **GET** /relations |  |
| [**getSuggestions**](RoadDistancesApi.md#getsuggestions) | **GET** /suggestions |  |



## getRelation

> RoadDistanceResponse getRelation(start, destination, region, dataVersion, results)



Gets the truck distance and additional information for a relation between two locations.

### Example

```ts
import {
  Configuration,
  RoadDistancesApi,
} from '';
import type { GetRelationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
  });
  const api = new RoadDistancesApi(config);

  const body = {
    // RequestLocation | The start of the relation. (optional)
    start: ...,
    // RequestLocation | The destination of the relation. (optional)
    destination: ...,
    // RegionType (optional)
    region: ...,
    // DataVersionType (optional)
    dataVersion: ...,
    // Array<ResultsType> | Comma-separated list that defines which results besides the distance will be returned. * `COORDINATES`     Response includes latitude and longitude of the reference locations of start and destination. * `TOLL_DISTANCE`     Response includes the distance of toll roads of the relation. (optional)
    results: ...,
  } satisfies GetRelationRequest;

  try {
    const data = await api.getRelation(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **start** | [](.md) | The start of the relation. | [Optional] [Defaults to `undefined`] |
| **destination** | [](.md) | The destination of the relation. | [Optional] [Defaults to `undefined`] |
| **region** | `RegionType` |  | [Optional] [Defaults to `undefined`] [Enum: BEST_QUALITY, EUROPE, GERMANY] |
| **dataVersion** | `DataVersionType` |  | [Optional] [Defaults to `undefined`] [Enum: V2016, V2017, V2018, V2019, V2020, V2021, V2022, V2023, V2024, V2025, V2026, LATEST] |
| **results** | `Array<ResultsType>` | Comma-separated list that defines which results besides the distance will be returned. * &#x60;COORDINATES&#x60;     Response includes latitude and longitude of the reference locations of start and destination. * &#x60;TOLL_DISTANCE&#x60;     Response includes the distance of toll roads of the relation. | [Optional] |

### Return type

[**RoadDistanceResponse**](RoadDistanceResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response on success. |  -  |
| **0** | Response on failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getSuggestions

> SuggestionsResponse getSuggestions(country, postalCode, locality, region, dataVersion, type, limit)



Gets suggestions for a location. Provide at least two characters in **postalCode** or **locality** to obtain results.

### Example

```ts
import {
  Configuration,
  RoadDistancesApi,
} from '';
import type { GetSuggestionsRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
  });
  const api = new RoadDistancesApi(config);

  const body = {
    // string | The country represented by its code according to [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). (optional)
    country: country_example,
    // string | The postal code or its initial characters. (optional)
    postalCode: postalCode_example,
    // string | The name or initial characters of the city or district in the language spoken in that country or region, always transliterated to Latin. The input will first be matched to city names and then to subdistrict names. (optional)
    locality: locality_example,
    // RegionType (optional)
    region: ...,
    // DataVersionType (optional)
    dataVersion: ...,
    // LocationType (optional)
    type: ...,
    // number (optional)
    limit: 56,
  } satisfies GetSuggestionsRequest;

  try {
    const data = await api.getSuggestions(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **country** | `string` | The country represented by its code according to [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). | [Optional] [Defaults to `undefined`] |
| **postalCode** | `string` | The postal code or its initial characters. | [Optional] [Defaults to `undefined`] |
| **locality** | `string` | The name or initial characters of the city or district in the language spoken in that country or region, always transliterated to Latin. The input will first be matched to city names and then to subdistrict names. | [Optional] [Defaults to `undefined`] |
| **region** | `RegionType` |  | [Optional] [Defaults to `undefined`] [Enum: BEST_QUALITY, EUROPE, GERMANY] |
| **dataVersion** | `DataVersionType` |  | [Optional] [Defaults to `undefined`] [Enum: V2016, V2017, V2018, V2019, V2020, V2021, V2022, V2023, V2024, V2025, V2026, LATEST] |
| **type** | `LocationType` |  | [Optional] [Defaults to `undefined`] [Enum: CITY, PORT, BORDER] |
| **limit** | `number` |  | [Optional] [Defaults to `10`] |

### Return type

[**SuggestionsResponse**](SuggestionsResponse.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Response on success. |  -  |
| **0** | Response on failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

