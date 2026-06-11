# \AuthzAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateRelationTuple**](AuthzAPI.md#CreateRelationTuple) | **Post** /v1/authz/relation-tuples | Create a relation tuple under a Project.
[**DeleteRelationTuple**](AuthzAPI.md#DeleteRelationTuple) | **Delete** /v1/authz/relation-tuples/{id} | Delete a relation tuple.
[**ListRelationTuples**](AuthzAPI.md#ListRelationTuples) | **Get** /v1/authz/relation-tuples | List relation tuples scoped to a Project.
[**PatchRelationTuple**](AuthzAPI.md#PatchRelationTuple) | **Patch** /v1/authz/relation-tuples/{id} | Replace a relation tuple&#39;s contents (delete-then-write).
[**PostAuthzCheck**](AuthzAPI.md#PostAuthzCheck) | **Post** /v1/authz/check | Run a ReBAC permission check.
[**PostAuthzLookupResources**](AuthzAPI.md#PostAuthzLookupResources) | **Post** /v1/authz/lookup-resources | List the resources a subject can reach via a relation.
[**PostAuthzLookupSubjects**](AuthzAPI.md#PostAuthzLookupSubjects) | **Post** /v1/authz/lookup-subjects | List the subjects that can reach a resource via a relation.



## CreateRelationTuple

> RelationTuple CreateRelationTuple(ctx).ProjectId(projectId).RelationTupleCreateRequest(relationTupleCreateRequest).Execute()

Create a relation tuple under a Project.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7).
	relationTupleCreateRequest := *openapiclient.NewRelationTupleCreateRequest("Subject_example", "Relation_example", "Resource_example") // RelationTupleCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthzAPI.CreateRelationTuple(context.Background()).ProjectId(projectId).RelationTupleCreateRequest(relationTupleCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthzAPI.CreateRelationTuple``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateRelationTuple`: RelationTuple
	fmt.Fprintf(os.Stdout, "Response from `AuthzAPI.CreateRelationTuple`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateRelationTupleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectId** | **string** | Owning Project (UUIDv7). | 
 **relationTupleCreateRequest** | [**RelationTupleCreateRequest**](RelationTupleCreateRequest.md) |  | 

### Return type

[**RelationTuple**](RelationTuple.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteRelationTuple

> DeleteRelationTuple(ctx, id).Execute()

Delete a relation tuple.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Relation tuple identifier (UUIDv7). Bound on `/v1/authz/relation-tuples/{id}` for the per-tuple PATCH / DELETE surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AuthzAPI.DeleteRelationTuple(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthzAPI.DeleteRelationTuple``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Relation tuple identifier (UUIDv7). Bound on &#x60;/v1/authz/relation-tuples/{id}&#x60; for the per-tuple PATCH / DELETE surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteRelationTupleRequest struct via the builder pattern


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


## ListRelationTuples

> RelationTupleList ListRelationTuples(ctx).ProjectId(projectId).Cursor(cursor).Limit(limit).Execute()

List relation tuples scoped to a Project.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Relation-tuple administration is scoped per Project so every list call resolves to a single Project's tuples. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthzAPI.ListRelationTuples(context.Background()).ProjectId(projectId).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthzAPI.ListRelationTuples``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListRelationTuples`: RelationTupleList
	fmt.Fprintf(os.Stdout, "Response from `AuthzAPI.ListRelationTuples`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListRelationTuplesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectId** | **string** | Owning Project (UUIDv7). Relation-tuple administration is scoped per Project so every list call resolves to a single Project&#39;s tuples.  | 
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  | [default to 50]

### Return type

[**RelationTupleList**](RelationTupleList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PatchRelationTuple

> RelationTuple PatchRelationTuple(ctx, id).RelationTuplePatchRequest(relationTuplePatchRequest).Execute()

Replace a relation tuple's contents (delete-then-write).



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Relation tuple identifier (UUIDv7). Bound on `/v1/authz/relation-tuples/{id}` for the per-tuple PATCH / DELETE surface. 
	relationTuplePatchRequest := *openapiclient.NewRelationTuplePatchRequest("Subject_example", "Relation_example", "Resource_example") // RelationTuplePatchRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthzAPI.PatchRelationTuple(context.Background(), id).RelationTuplePatchRequest(relationTuplePatchRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthzAPI.PatchRelationTuple``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PatchRelationTuple`: RelationTuple
	fmt.Fprintf(os.Stdout, "Response from `AuthzAPI.PatchRelationTuple`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Relation tuple identifier (UUIDv7). Bound on &#x60;/v1/authz/relation-tuples/{id}&#x60; for the per-tuple PATCH / DELETE surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiPatchRelationTupleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **relationTuplePatchRequest** | [**RelationTuplePatchRequest**](RelationTuplePatchRequest.md) |  | 

### Return type

[**RelationTuple**](RelationTuple.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAuthzCheck

> RebacCheckResponse PostAuthzCheck(ctx).RebacCheckRequest(rebacCheckRequest).Execute()

Run a ReBAC permission check.



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
	rebacCheckRequest := *openapiclient.NewRebacCheckRequest("Subject_example", "Relation_example", "Resource_example") // RebacCheckRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthzAPI.PostAuthzCheck(context.Background()).RebacCheckRequest(rebacCheckRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthzAPI.PostAuthzCheck``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAuthzCheck`: RebacCheckResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthzAPI.PostAuthzCheck`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthzCheckRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rebacCheckRequest** | [**RebacCheckRequest**](RebacCheckRequest.md) |  | 

### Return type

[**RebacCheckResponse**](RebacCheckResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAuthzLookupResources

> RebacLookupResponse PostAuthzLookupResources(ctx).LookupResourcesRequest(lookupResourcesRequest).Execute()

List the resources a subject can reach via a relation.



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
	lookupResourcesRequest := *openapiclient.NewLookupResourcesRequest("Subject_example", "Relation_example", "ResourceType_example") // LookupResourcesRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthzAPI.PostAuthzLookupResources(context.Background()).LookupResourcesRequest(lookupResourcesRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthzAPI.PostAuthzLookupResources``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAuthzLookupResources`: RebacLookupResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthzAPI.PostAuthzLookupResources`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthzLookupResourcesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lookupResourcesRequest** | [**LookupResourcesRequest**](LookupResourcesRequest.md) |  | 

### Return type

[**RebacLookupResponse**](RebacLookupResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAuthzLookupSubjects

> RebacLookupResponse PostAuthzLookupSubjects(ctx).LookupSubjectsRequest(lookupSubjectsRequest).Execute()

List the subjects that can reach a resource via a relation.



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
	lookupSubjectsRequest := *openapiclient.NewLookupSubjectsRequest("SubjectType_example", "Relation_example", "Resource_example") // LookupSubjectsRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthzAPI.PostAuthzLookupSubjects(context.Background()).LookupSubjectsRequest(lookupSubjectsRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthzAPI.PostAuthzLookupSubjects``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAuthzLookupSubjects`: RebacLookupResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthzAPI.PostAuthzLookupSubjects`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthzLookupSubjectsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lookupSubjectsRequest** | [**LookupSubjectsRequest**](LookupSubjectsRequest.md) |  | 

### Return type

[**RebacLookupResponse**](RebacLookupResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

