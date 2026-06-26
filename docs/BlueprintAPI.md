# \BlueprintAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetBlueprint**](BlueprintAPI.md#GetBlueprint) | **Get** /v1/blueprints/{id} | Fetch a Blueprint by identifier.
[**ListBlueprints**](BlueprintAPI.md#ListBlueprints) | **Get** /v1/blueprints | List the Blueprint Catalog.
[**PublishBlueprintVersion**](BlueprintAPI.md#PublishBlueprintVersion) | **Post** /v1/blueprints/{id}/versions | Publish a Blueprint version.
[**RegisterBlueprint**](BlueprintAPI.md#RegisterBlueprint) | **Post** /v1/blueprints | Register a Blueprint Catalog entry.



## GetBlueprint

> BlueprintResponse GetBlueprint(ctx, id).Execute()

Fetch a Blueprint by identifier.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Blueprint identifier (UUIDv7). Bound on `/v1/blueprints/{id}` for the read-only Blueprint Catalog surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlueprintAPI.GetBlueprint(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlueprintAPI.GetBlueprint``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBlueprint`: BlueprintResponse
	fmt.Fprintf(os.Stdout, "Response from `BlueprintAPI.GetBlueprint`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Blueprint identifier (UUIDv7). Bound on &#x60;/v1/blueprints/{id}&#x60; for the read-only Blueprint Catalog surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetBlueprintRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**BlueprintResponse**](BlueprintResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListBlueprints

> BlueprintList ListBlueprints(ctx).Cursor(cursor).Limit(limit).Execute()

List the Blueprint Catalog.



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
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlueprintAPI.ListBlueprints(context.Background()).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlueprintAPI.ListBlueprints``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListBlueprints`: BlueprintList
	fmt.Fprintf(os.Stdout, "Response from `BlueprintAPI.ListBlueprints`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListBlueprintsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**BlueprintList**](BlueprintList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PublishBlueprintVersion

> BlueprintVersionResponse PublishBlueprintVersion(ctx, id).BlueprintVersionCreateRequest(blueprintVersionCreateRequest).Execute()

Publish a Blueprint version.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Blueprint identifier (UUIDv7). Bound on `/v1/blueprints/{id}` for the read-only Blueprint Catalog surface. 
	blueprintVersionCreateRequest := *openapiclient.NewBlueprintVersionCreateRequest("Version_example", map[string]interface{}{"key": interface{}(123)}, map[string]interface{}{"key": interface{}(123)}, map[string]interface{}{"key": interface{}(123)}, []string{"ProviderKinds_example"}, "InjectionStrategy_example") // BlueprintVersionCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlueprintAPI.PublishBlueprintVersion(context.Background(), id).BlueprintVersionCreateRequest(blueprintVersionCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlueprintAPI.PublishBlueprintVersion``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PublishBlueprintVersion`: BlueprintVersionResponse
	fmt.Fprintf(os.Stdout, "Response from `BlueprintAPI.PublishBlueprintVersion`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Blueprint identifier (UUIDv7). Bound on &#x60;/v1/blueprints/{id}&#x60; for the read-only Blueprint Catalog surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiPublishBlueprintVersionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **blueprintVersionCreateRequest** | [**BlueprintVersionCreateRequest**](BlueprintVersionCreateRequest.md) |  | 

### Return type

[**BlueprintVersionResponse**](BlueprintVersionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RegisterBlueprint

> BlueprintResponse RegisterBlueprint(ctx).BlueprintCreateRequest(blueprintCreateRequest).Execute()

Register a Blueprint Catalog entry.



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
	blueprintCreateRequest := *openapiclient.NewBlueprintCreateRequest("Slug_example", "DisplayName_example") // BlueprintCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BlueprintAPI.RegisterBlueprint(context.Background()).BlueprintCreateRequest(blueprintCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BlueprintAPI.RegisterBlueprint``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RegisterBlueprint`: BlueprintResponse
	fmt.Fprintf(os.Stdout, "Response from `BlueprintAPI.RegisterBlueprint`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRegisterBlueprintRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **blueprintCreateRequest** | [**BlueprintCreateRequest**](BlueprintCreateRequest.md) |  | 

### Return type

[**BlueprintResponse**](BlueprintResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

