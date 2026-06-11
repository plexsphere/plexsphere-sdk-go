# \PolicyAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreatePolicy**](PolicyAPI.md#CreatePolicy) | **Post** /v1/projects/{project_id}/policies | Create a Policy in a Project.
[**DeletePolicy**](PolicyAPI.md#DeletePolicy) | **Delete** /v1/projects/{project_id}/policies/{policy_id} | Delete a Policy and cascade its revisions.
[**DiffPolicyRevisions**](PolicyAPI.md#DiffPolicyRevisions) | **Get** /v1/projects/{project_id}/policies/{policy_id}/diff | Compute the diff between two Policy revisions.
[**DryRunPolicy**](PolicyAPI.md#DryRunPolicy) | **Post** /v1/projects/{project_id}/policies/{policy_id}/dry-run | Evaluate a candidate Policy revision without persisting.
[**GetPolicy**](PolicyAPI.md#GetPolicy) | **Get** /v1/projects/{project_id}/policies/{policy_id} | Fetch a Policy with its head revision.
[**GetPolicyRevision**](PolicyAPI.md#GetPolicyRevision) | **Get** /v1/projects/{project_id}/policies/{policy_id}/revisions/{revision_id} | Fetch a historical Policy revision.
[**ListPolicies**](PolicyAPI.md#ListPolicies) | **Get** /v1/projects/{project_id}/policies | List Policies in a Project.
[**ListPolicyRevisions**](PolicyAPI.md#ListPolicyRevisions) | **Get** /v1/projects/{project_id}/policies/{policy_id}/revisions | List a Policy&#39;s revision history.
[**UpdatePolicy**](PolicyAPI.md#UpdatePolicy) | **Patch** /v1/projects/{project_id}/policies/{policy_id} | Update a Policy by landing a new revision.



## CreatePolicy

> Policy CreatePolicy(ctx, projectId).PolicyCreateRequest(policyCreateRequest).Execute()

Create a Policy in a Project.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/...` operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target. 
	policyCreateRequest := *openapiclient.NewPolicyCreateRequest("Slug_example", *openapiclient.NewPolicySelector("Source_example", "Destination_example"), []openapiclient.PolicyRule{*openapiclient.NewPolicyRule(openapiclient.PolicyAction("allow"), openapiclient.PolicyProtocol("tcp"), "SourceCidr_example", "DestinationCidr_example")}) // PolicyCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.PolicyAPI.CreatePolicy(context.Background(), projectId).PolicyCreateRequest(policyCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PolicyAPI.CreatePolicy``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreatePolicy`: Policy
	fmt.Fprintf(os.Stdout, "Response from `PolicyAPI.CreatePolicy`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/...&#x60; operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreatePolicyRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **policyCreateRequest** | [**PolicyCreateRequest**](PolicyCreateRequest.md) |  | 

### Return type

[**Policy**](Policy.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeletePolicy

> DeletePolicy(ctx, projectId, policyId).Execute()

Delete a Policy and cascade its revisions.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/...` operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target. 
	policyId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Policy identifier (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/{policy_id}/...` operation. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.PolicyAPI.DeletePolicy(context.Background(), projectId, policyId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PolicyAPI.DeletePolicy``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/...&#x60; operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target.  | 
**policyId** | **string** | Policy identifier (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/{policy_id}/...&#x60; operation.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeletePolicyRequest struct via the builder pattern


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


## DiffPolicyRevisions

> PolicyDiff DiffPolicyRevisions(ctx, projectId, policyId).FromRevision(fromRevision).ToRevision(toRevision).Execute()

Compute the diff between two Policy revisions.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/...` operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target. 
	policyId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Policy identifier (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/{policy_id}/...` operation. 
	fromRevision := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Identifier of the source revision.
	toRevision := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Identifier of the target revision.

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.PolicyAPI.DiffPolicyRevisions(context.Background(), projectId, policyId).FromRevision(fromRevision).ToRevision(toRevision).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PolicyAPI.DiffPolicyRevisions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DiffPolicyRevisions`: PolicyDiff
	fmt.Fprintf(os.Stdout, "Response from `PolicyAPI.DiffPolicyRevisions`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/...&#x60; operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target.  | 
**policyId** | **string** | Policy identifier (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/{policy_id}/...&#x60; operation.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDiffPolicyRevisionsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **fromRevision** | **string** | Identifier of the source revision. | 
 **toRevision** | **string** | Identifier of the target revision. | 

### Return type

[**PolicyDiff**](PolicyDiff.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DryRunPolicy

> PolicyDryRunResponse DryRunPolicy(ctx, projectId, policyId).PolicyDryRunRequest(policyDryRunRequest).Execute()

Evaluate a candidate Policy revision without persisting.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/...` operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target. 
	policyId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Policy identifier (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/{policy_id}/...` operation. 
	policyDryRunRequest := *openapiclient.NewPolicyDryRunRequest(*openapiclient.NewPolicySelector("Source_example", "Destination_example"), []openapiclient.PolicyRule{*openapiclient.NewPolicyRule(openapiclient.PolicyAction("allow"), openapiclient.PolicyProtocol("tcp"), "SourceCidr_example", "DestinationCidr_example")}) // PolicyDryRunRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.PolicyAPI.DryRunPolicy(context.Background(), projectId, policyId).PolicyDryRunRequest(policyDryRunRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PolicyAPI.DryRunPolicy``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DryRunPolicy`: PolicyDryRunResponse
	fmt.Fprintf(os.Stdout, "Response from `PolicyAPI.DryRunPolicy`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/...&#x60; operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target.  | 
**policyId** | **string** | Policy identifier (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/{policy_id}/...&#x60; operation.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDryRunPolicyRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **policyDryRunRequest** | [**PolicyDryRunRequest**](PolicyDryRunRequest.md) |  | 

### Return type

[**PolicyDryRunResponse**](PolicyDryRunResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetPolicy

> Policy GetPolicy(ctx, projectId, policyId).Execute()

Fetch a Policy with its head revision.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/...` operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target. 
	policyId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Policy identifier (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/{policy_id}/...` operation. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.PolicyAPI.GetPolicy(context.Background(), projectId, policyId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PolicyAPI.GetPolicy``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetPolicy`: Policy
	fmt.Fprintf(os.Stdout, "Response from `PolicyAPI.GetPolicy`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/...&#x60; operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target.  | 
**policyId** | **string** | Policy identifier (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/{policy_id}/...&#x60; operation.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetPolicyRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**Policy**](Policy.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetPolicyRevision

> PolicyRevision GetPolicyRevision(ctx, projectId, policyId, revisionId).Execute()

Fetch a historical Policy revision.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/...` operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target. 
	policyId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Policy identifier (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/{policy_id}/...` operation. 
	revisionId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Revision identifier (UUIDv7). Bound on `/v1/projects/{project_id}/policies/{policy_id}/revisions/{revision_id}`. Revisions that do not belong to the addressed Policy surface as `404 revision_not_visible`. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.PolicyAPI.GetPolicyRevision(context.Background(), projectId, policyId, revisionId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PolicyAPI.GetPolicyRevision``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetPolicyRevision`: PolicyRevision
	fmt.Fprintf(os.Stdout, "Response from `PolicyAPI.GetPolicyRevision`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/...&#x60; operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target.  | 
**policyId** | **string** | Policy identifier (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/{policy_id}/...&#x60; operation.  | 
**revisionId** | **string** | Revision identifier (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/policies/{policy_id}/revisions/{revision_id}&#x60;. Revisions that do not belong to the addressed Policy surface as &#x60;404 revision_not_visible&#x60;.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetPolicyRevisionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------




### Return type

[**PolicyRevision**](PolicyRevision.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListPolicies

> PolicyListResponse ListPolicies(ctx, projectId).Cursor(cursor).Limit(limit).Execute()

List Policies in a Project.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/...` operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. Clamped to 200 server-side.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.PolicyAPI.ListPolicies(context.Background(), projectId).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PolicyAPI.ListPolicies``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListPolicies`: PolicyListResponse
	fmt.Fprintf(os.Stdout, "Response from `PolicyAPI.ListPolicies`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/...&#x60; operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListPoliciesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. Clamped to 200 server-side.  | [default to 50]

### Return type

[**PolicyListResponse**](PolicyListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListPolicyRevisions

> PolicyRevisionListResponse ListPolicyRevisions(ctx, projectId, policyId).Cursor(cursor).Limit(limit).Execute()

List a Policy's revision history.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/...` operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target. 
	policyId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Policy identifier (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/{policy_id}/...` operation. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. Clamped to 200 server-side.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.PolicyAPI.ListPolicyRevisions(context.Background(), projectId, policyId).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PolicyAPI.ListPolicyRevisions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListPolicyRevisions`: PolicyRevisionListResponse
	fmt.Fprintf(os.Stdout, "Response from `PolicyAPI.ListPolicyRevisions`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/...&#x60; operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target.  | 
**policyId** | **string** | Policy identifier (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/{policy_id}/...&#x60; operation.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListPolicyRevisionsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. Clamped to 200 server-side.  | [default to 50]

### Return type

[**PolicyRevisionListResponse**](PolicyRevisionListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdatePolicy

> Policy UpdatePolicy(ctx, projectId, policyId).PolicyUpdateRequest(policyUpdateRequest).Execute()

Update a Policy by landing a new revision.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/...` operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target. 
	policyId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Policy identifier (UUIDv7). Bound on every `/v1/projects/{project_id}/policies/{policy_id}/...` operation. 
	policyUpdateRequest := *openapiclient.NewPolicyUpdateRequest() // PolicyUpdateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.PolicyAPI.UpdatePolicy(context.Background(), projectId, policyId).PolicyUpdateRequest(policyUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `PolicyAPI.UpdatePolicy``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdatePolicy`: Policy
	fmt.Fprintf(os.Stdout, "Response from `PolicyAPI.UpdatePolicy`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/...&#x60; operation — the Policy aggregate is per-Project and the dual ReBAC check uses the Project as the second relation target.  | 
**policyId** | **string** | Policy identifier (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/policies/{policy_id}/...&#x60; operation.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdatePolicyRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **policyUpdateRequest** | [**PolicyUpdateRequest**](PolicyUpdateRequest.md) |  | 

### Return type

[**Policy**](Policy.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

