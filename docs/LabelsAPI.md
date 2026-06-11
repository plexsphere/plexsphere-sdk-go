# \LabelsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateLabelDefinition**](LabelsAPI.md#CreateLabelDefinition) | **Post** /v1/label-definitions | Create a Label Definition at a specific scope.
[**DeleteLabelDefinition**](LabelsAPI.md#DeleteLabelDefinition) | **Delete** /v1/label-definitions/{id} | Delete a Label Definition.
[**DeleteObjectLabel**](LabelsAPI.md#DeleteObjectLabel) | **Delete** /v1/objects/{kind}/{id}/labels | Remove a Label Assignment from an object.
[**GetLabelDefinition**](LabelsAPI.md#GetLabelDefinition) | **Get** /v1/label-definitions/{id} | Fetch a Label Definition by identifier.
[**ListLabelDefinitions**](LabelsAPI.md#ListLabelDefinitions) | **Get** /v1/label-definitions | List Label Definitions in a scope.
[**ListObjectLabels**](LabelsAPI.md#ListObjectLabels) | **Get** /v1/objects/{kind}/{id}/labels | List Label Assignments attached to an object.
[**PreviewLabelSelector**](LabelsAPI.md#PreviewLabelSelector) | **Post** /v1/labels/selectors/preview | Parse a label selector and return its AST or errors inline.
[**PutObjectLabel**](LabelsAPI.md#PutObjectLabel) | **Put** /v1/objects/{kind}/{id}/labels | Upsert a Label Assignment on an object.
[**UpdateLabelDefinition**](LabelsAPI.md#UpdateLabelDefinition) | **Patch** /v1/label-definitions/{id} | Update mutable fields on a Label Definition.



## CreateLabelDefinition

> LabelDefinition CreateLabelDefinition(ctx).LabelDefinitionRequest(labelDefinitionRequest).Execute()

Create a Label Definition at a specific scope.



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
	labelDefinitionRequest := *openapiclient.NewLabelDefinitionRequest(openapiclient.LabelDefinitionRequest_scope("platform"), "LocalKey_example", *openapiclient.NewLabelValueSchema(openapiclient.ValueSchemaKind("string")), []string{"ApplicableKinds_example"}) // LabelDefinitionRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LabelsAPI.CreateLabelDefinition(context.Background()).LabelDefinitionRequest(labelDefinitionRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LabelsAPI.CreateLabelDefinition``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateLabelDefinition`: LabelDefinition
	fmt.Fprintf(os.Stdout, "Response from `LabelsAPI.CreateLabelDefinition`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateLabelDefinitionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **labelDefinitionRequest** | [**LabelDefinitionRequest**](LabelDefinitionRequest.md) |  | 

### Return type

[**LabelDefinition**](LabelDefinition.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteLabelDefinition

> DeleteLabelDefinition(ctx, id).Execute()

Delete a Label Definition.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Label Definition identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.LabelsAPI.DeleteLabelDefinition(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LabelsAPI.DeleteLabelDefinition``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Label Definition identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteLabelDefinitionRequest struct via the builder pattern


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


## DeleteObjectLabel

> DeleteObjectLabel(ctx, kind, id).QualifiedKey(qualifiedKey).Execute()

Remove a Label Assignment from an object.



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
	kind := "kind_example" // string | Lowercase object-kind discriminator.
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Object identifier (UUIDv7).
	qualifiedKey := "qualifiedKey_example" // string | Fully-qualified Label key (e.g. `platform/env` or `acme:checkout/owner`). DECISION: addressed by qualified_key rather than definition_id so the client does not need a Definition lookup to issue the delete. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.LabelsAPI.DeleteObjectLabel(context.Background(), kind, id).QualifiedKey(qualifiedKey).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LabelsAPI.DeleteObjectLabel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**kind** | **string** | Lowercase object-kind discriminator. | 
**id** | **string** | Object identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteObjectLabelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **qualifiedKey** | **string** | Fully-qualified Label key (e.g. &#x60;platform/env&#x60; or &#x60;acme:checkout/owner&#x60;). DECISION: addressed by qualified_key rather than definition_id so the client does not need a Definition lookup to issue the delete.  | 

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


## GetLabelDefinition

> LabelDefinition GetLabelDefinition(ctx, id).Execute()

Fetch a Label Definition by identifier.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Label Definition identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LabelsAPI.GetLabelDefinition(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LabelsAPI.GetLabelDefinition``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetLabelDefinition`: LabelDefinition
	fmt.Fprintf(os.Stdout, "Response from `LabelsAPI.GetLabelDefinition`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Label Definition identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetLabelDefinitionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**LabelDefinition**](LabelDefinition.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListLabelDefinitions

> LabelDefinitionListResponse ListLabelDefinitions(ctx).Scope(scope).Cursor(cursor).Limit(limit).Execute()

List Label Definitions in a scope.



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
	scope := "scope_example" // string | Scope selector. Accepts the literal `platform`, or `domain:<uuid>`, or `project:<uuid>`. DECISION: scope is a single string rather than a pair of query params because the three forms are mutually exclusive and the SpiceDB scope-object derivation treats them as a single coordinate . 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page .  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LabelsAPI.ListLabelDefinitions(context.Background()).Scope(scope).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LabelsAPI.ListLabelDefinitions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListLabelDefinitions`: LabelDefinitionListResponse
	fmt.Fprintf(os.Stdout, "Response from `LabelsAPI.ListLabelDefinitions`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListLabelDefinitionsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **scope** | **string** | Scope selector. Accepts the literal &#x60;platform&#x60;, or &#x60;domain:&lt;uuid&gt;&#x60;, or &#x60;project:&lt;uuid&gt;&#x60;. DECISION: scope is a single string rather than a pair of query params because the three forms are mutually exclusive and the SpiceDB scope-object derivation treats them as a single coordinate .  | 
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page .  | [default to 50]

### Return type

[**LabelDefinitionListResponse**](LabelDefinitionListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListObjectLabels

> LabelAssignmentList ListObjectLabels(ctx, kind, id).Execute()

List Label Assignments attached to an object.



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
	kind := "kind_example" // string | Lowercase object-kind discriminator (resource, node, project, domain, workload, network, …). 
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Object identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LabelsAPI.ListObjectLabels(context.Background(), kind, id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LabelsAPI.ListObjectLabels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListObjectLabels`: LabelAssignmentList
	fmt.Fprintf(os.Stdout, "Response from `LabelsAPI.ListObjectLabels`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**kind** | **string** | Lowercase object-kind discriminator (resource, node, project, domain, workload, network, …).  | 
**id** | **string** | Object identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiListObjectLabelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**LabelAssignmentList**](LabelAssignmentList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PreviewLabelSelector

> LabelSelectorPreviewResponse PreviewLabelSelector(ctx).LabelSelectorPreviewRequest(labelSelectorPreviewRequest).Execute()

Parse a label selector and return its AST or errors inline.



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
	labelSelectorPreviewRequest := *openapiclient.NewLabelSelectorPreviewRequest("Expression_example") // LabelSelectorPreviewRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LabelsAPI.PreviewLabelSelector(context.Background()).LabelSelectorPreviewRequest(labelSelectorPreviewRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LabelsAPI.PreviewLabelSelector``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PreviewLabelSelector`: LabelSelectorPreviewResponse
	fmt.Fprintf(os.Stdout, "Response from `LabelsAPI.PreviewLabelSelector`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPreviewLabelSelectorRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **labelSelectorPreviewRequest** | [**LabelSelectorPreviewRequest**](LabelSelectorPreviewRequest.md) |  | 

### Return type

[**LabelSelectorPreviewResponse**](LabelSelectorPreviewResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PutObjectLabel

> LabelAssignment PutObjectLabel(ctx, kind, id).LabelAssignmentRequest(labelAssignmentRequest).Execute()

Upsert a Label Assignment on an object.



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
	kind := "kind_example" // string | Lowercase object-kind discriminator.
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Object identifier (UUIDv7).
	labelAssignmentRequest := *openapiclient.NewLabelAssignmentRequest("DefinitionId_example", interface{}(123)) // LabelAssignmentRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LabelsAPI.PutObjectLabel(context.Background(), kind, id).LabelAssignmentRequest(labelAssignmentRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LabelsAPI.PutObjectLabel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PutObjectLabel`: LabelAssignment
	fmt.Fprintf(os.Stdout, "Response from `LabelsAPI.PutObjectLabel`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**kind** | **string** | Lowercase object-kind discriminator. | 
**id** | **string** | Object identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiPutObjectLabelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **labelAssignmentRequest** | [**LabelAssignmentRequest**](LabelAssignmentRequest.md) |  | 

### Return type

[**LabelAssignment**](LabelAssignment.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateLabelDefinition

> LabelDefinition UpdateLabelDefinition(ctx, id).LabelDefinitionUpdateRequest(labelDefinitionUpdateRequest).Execute()

Update mutable fields on a Label Definition.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Label Definition identifier (UUIDv7).
	labelDefinitionUpdateRequest := *openapiclient.NewLabelDefinitionUpdateRequest() // LabelDefinitionUpdateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.LabelsAPI.UpdateLabelDefinition(context.Background(), id).LabelDefinitionUpdateRequest(labelDefinitionUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `LabelsAPI.UpdateLabelDefinition``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateLabelDefinition`: LabelDefinition
	fmt.Fprintf(os.Stdout, "Response from `LabelsAPI.UpdateLabelDefinition`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Label Definition identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateLabelDefinitionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **labelDefinitionUpdateRequest** | [**LabelDefinitionUpdateRequest**](LabelDefinitionUpdateRequest.md) |  | 

### Return type

[**LabelDefinition**](LabelDefinition.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

