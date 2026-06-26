# \BlueprintCatalogAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**BrowseCatalogSource**](BlueprintCatalogAPI.md#BrowseCatalogSource) | **Get** /v1/blueprint-catalogs/{id}/blueprints | Browse the Blueprints a catalog source offers.
[**DeregisterCatalogSource**](BlueprintCatalogAPI.md#DeregisterCatalogSource) | **Delete** /v1/blueprint-catalogs/{id} | Deregister a Blueprint catalog source.
[**GetCatalogSource**](BlueprintCatalogAPI.md#GetCatalogSource) | **Get** /v1/blueprint-catalogs/{id} | Fetch a Blueprint catalog source by identifier.
[**ImportFromCatalogSource**](BlueprintCatalogAPI.md#ImportFromCatalogSource) | **Post** /v1/blueprint-catalogs/{id}/import | Import Blueprints from a catalog source.
[**ListCatalogSources**](BlueprintCatalogAPI.md#ListCatalogSources) | **Get** /v1/blueprint-catalogs | List the registered Blueprint catalog sources.
[**RegisterCatalogSource**](BlueprintCatalogAPI.md#RegisterCatalogSource) | **Post** /v1/blueprint-catalogs | Register a Blueprint catalog source.



## BrowseCatalogSource

> CatalogBrowseResponse BrowseCatalogSource(ctx, id).Execute()

Browse the Blueprints a catalog source offers.



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/plexsphere/plexsphere-sdk-go"
)

func main() {
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Catalog source identifier (UUIDv7). Bound on the `/v1/blueprint-catalogs/{id}` family — get, deregister, browse, and import. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlueprintCatalogAPI.BrowseCatalogSource(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlueprintCatalogAPI.BrowseCatalogSource``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BrowseCatalogSource`: CatalogBrowseResponse
	fmt.Fprintf(os.Stdout, "Response from `BlueprintCatalogAPI.BrowseCatalogSource`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Catalog source identifier (UUIDv7). Bound on the &#x60;/v1/blueprint-catalogs/{id}&#x60; family — get, deregister, browse, and import.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiBrowseCatalogSourceRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**CatalogBrowseResponse**](CatalogBrowseResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeregisterCatalogSource

> DeregisterCatalogSource(ctx, id).Execute()

Deregister a Blueprint catalog source.



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/plexsphere/plexsphere-sdk-go"
)

func main() {
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Catalog source identifier (UUIDv7). Bound on the `/v1/blueprint-catalogs/{id}` family — get, deregister, browse, and import. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.BlueprintCatalogAPI.DeregisterCatalogSource(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlueprintCatalogAPI.DeregisterCatalogSource``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Catalog source identifier (UUIDv7). Bound on the &#x60;/v1/blueprint-catalogs/{id}&#x60; family — get, deregister, browse, and import.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeregisterCatalogSourceRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetCatalogSource

> CatalogSourceResponse GetCatalogSource(ctx, id).Execute()

Fetch a Blueprint catalog source by identifier.



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/plexsphere/plexsphere-sdk-go"
)

func main() {
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Catalog source identifier (UUIDv7). Bound on the `/v1/blueprint-catalogs/{id}` family — get, deregister, browse, and import. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlueprintCatalogAPI.GetCatalogSource(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlueprintCatalogAPI.GetCatalogSource``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetCatalogSource`: CatalogSourceResponse
	fmt.Fprintf(os.Stdout, "Response from `BlueprintCatalogAPI.GetCatalogSource`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Catalog source identifier (UUIDv7). Bound on the &#x60;/v1/blueprint-catalogs/{id}&#x60; family — get, deregister, browse, and import.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetCatalogSourceRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**CatalogSourceResponse**](CatalogSourceResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ImportFromCatalogSource

> ImportResult ImportFromCatalogSource(ctx, id).ImportRequest(importRequest).Execute()

Import Blueprints from a catalog source.



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/plexsphere/plexsphere-sdk-go"
)

func main() {
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Catalog source identifier (UUIDv7). Bound on the `/v1/blueprint-catalogs/{id}` family — get, deregister, browse, and import. 
	importRequest := *openapiclient.NewImportRequest() // ImportRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlueprintCatalogAPI.ImportFromCatalogSource(context.Background(), id).ImportRequest(importRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlueprintCatalogAPI.ImportFromCatalogSource``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ImportFromCatalogSource`: ImportResult
	fmt.Fprintf(os.Stdout, "Response from `BlueprintCatalogAPI.ImportFromCatalogSource`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Catalog source identifier (UUIDv7). Bound on the &#x60;/v1/blueprint-catalogs/{id}&#x60; family — get, deregister, browse, and import.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiImportFromCatalogSourceRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **importRequest** | [**ImportRequest**](ImportRequest.md) |  | 

### Return type

[**ImportResult**](ImportResult.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCatalogSources

> CatalogSourceList ListCatalogSources(ctx).Execute()

List the registered Blueprint catalog sources.



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/plexsphere/plexsphere-sdk-go"
)

func main() {

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlueprintCatalogAPI.ListCatalogSources(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlueprintCatalogAPI.ListCatalogSources``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCatalogSources`: CatalogSourceList
	fmt.Fprintf(os.Stdout, "Response from `BlueprintCatalogAPI.ListCatalogSources`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiListCatalogSourcesRequest struct via the builder pattern


### Return type

[**CatalogSourceList**](CatalogSourceList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RegisterCatalogSource

> CatalogSourceResponse RegisterCatalogSource(ctx).CatalogSourceCreateRequest(catalogSourceCreateRequest).Execute()

Register a Blueprint catalog source.



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/plexsphere/plexsphere-sdk-go"
)

func main() {
	catalogSourceCreateRequest := *openapiclient.NewCatalogSourceCreateRequest("Name_example", *openapiclient.NewOciReference("Registry_example", "Repository_example"), *openapiclient.NewVerificationPolicy(openapiclient.VerificationPolicy_mode("pinned")), *openapiclient.NewTrackingPolicy(openapiclient.TrackingPolicy_mode("pinned")), openapiclient.CatalogSourceCreateRequest_status("active")) // CatalogSourceCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlueprintCatalogAPI.RegisterCatalogSource(context.Background()).CatalogSourceCreateRequest(catalogSourceCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlueprintCatalogAPI.RegisterCatalogSource``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RegisterCatalogSource`: CatalogSourceResponse
	fmt.Fprintf(os.Stdout, "Response from `BlueprintCatalogAPI.RegisterCatalogSource`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRegisterCatalogSourceRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **catalogSourceCreateRequest** | [**CatalogSourceCreateRequest**](CatalogSourceCreateRequest.md) |  | 

### Return type

[**CatalogSourceResponse**](CatalogSourceResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

