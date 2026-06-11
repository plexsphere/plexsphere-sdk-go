# \ResourceAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateResource**](ResourceAPI.md#CreateResource) | **Post** /v1/projects/{project_id}/resources | Create a Resource (adopted or broker-provisioned).
[**DeleteResource**](ResourceAPI.md#DeleteResource) | **Delete** /v1/resources/{id} | Delete a Resource (graceful for provisioned).
[**GetResource**](ResourceAPI.md#GetResource) | **Get** /v1/resources/{id} | Fetch a Resource by identifier.
[**ListProjectResources**](ResourceAPI.md#ListProjectResources) | **Get** /v1/projects/{project_id}/resources | List Resources inside a Project.



## CreateResource

> ResourceResponse CreateResource(ctx, projectId).ResourceCreateRequest(resourceCreateRequest).Execute()

Create a Resource (adopted or broker-provisioned).



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceCreateRequest := *openapiclient.NewResourceCreateRequest(openapiclient.ResourceOrigin("adopted"), "Kind_example") // ResourceCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ResourceAPI.CreateResource(context.Background(), projectId).ResourceCreateRequest(resourceCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ResourceAPI.CreateResource``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateResource`: ResourceResponse
	fmt.Fprintf(os.Stdout, "Response from `ResourceAPI.CreateResource`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateResourceRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **resourceCreateRequest** | [**ResourceCreateRequest**](ResourceCreateRequest.md) |  | 

### Return type

[**ResourceResponse**](ResourceResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteResource

> DeleteResource(ctx, id).Execute()

Delete a Resource (graceful for provisioned).



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Resource identifier (UUIDv7). Bound on `/v1/resources/{id}` for the Tenancy Resource read + delete surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.ResourceAPI.DeleteResource(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ResourceAPI.DeleteResource``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Resource identifier (UUIDv7). Bound on &#x60;/v1/resources/{id}&#x60; for the Tenancy Resource read + delete surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteResourceRequest struct via the builder pattern


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


## GetResource

> ResourceResponse GetResource(ctx, id).Execute()

Fetch a Resource by identifier.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Resource identifier (UUIDv7). Bound on `/v1/resources/{id}` for the Tenancy Resource read + delete surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ResourceAPI.GetResource(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ResourceAPI.GetResource``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetResource`: ResourceResponse
	fmt.Fprintf(os.Stdout, "Response from `ResourceAPI.GetResource`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Resource identifier (UUIDv7). Bound on &#x60;/v1/resources/{id}&#x60; for the Tenancy Resource read + delete surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetResourceRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**ResourceResponse**](ResourceResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListProjectResources

> ResourceList ListProjectResources(ctx, projectId).Cursor(cursor).Limit(limit).Execute()

List Resources inside a Project.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ResourceAPI.ListProjectResources(context.Background(), projectId).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ResourceAPI.ListProjectResources``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListProjectResources`: ResourceList
	fmt.Fprintf(os.Stdout, "Response from `ResourceAPI.ListProjectResources`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListProjectResourcesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**ResourceList**](ResourceList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

