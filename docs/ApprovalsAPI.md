# \ApprovalsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ApproveApproval**](ApprovalsAPI.md#ApproveApproval) | **Post** /v1/approvals/{id}/approve | Approve a pending Approval.
[**BreakGlassApproval**](ApprovalsAPI.md#BreakGlassApproval) | **Post** /v1/approvals/{id}/break-glass | Force a pending Approval via the emergency override.
[**GetApproval**](ApprovalsAPI.md#GetApproval) | **Get** /v1/approvals/{id} | Inspect a single Approval.
[**ListApprovals**](ApprovalsAPI.md#ListApprovals) | **Get** /v1/approvals | List dual-control Approvals.
[**RejectApproval**](ApprovalsAPI.md#RejectApproval) | **Post** /v1/approvals/{id}/reject | Reject a pending Approval.



## ApproveApproval

> Approval ApproveApproval(ctx, id).Execute()

Approve a pending Approval.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Approval identifier (UUIDv7). Bound on `/v1/approvals/{id}`, `/v1/approvals/{id}/approve`, `/v1/approvals/{id}/reject`, and `/v1/approvals/{id}/break-glass` for the dual-control approval read + decision surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ApprovalsAPI.ApproveApproval(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ApprovalsAPI.ApproveApproval``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ApproveApproval`: Approval
	fmt.Fprintf(os.Stdout, "Response from `ApprovalsAPI.ApproveApproval`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Approval identifier (UUIDv7). Bound on &#x60;/v1/approvals/{id}&#x60;, &#x60;/v1/approvals/{id}/approve&#x60;, &#x60;/v1/approvals/{id}/reject&#x60;, and &#x60;/v1/approvals/{id}/break-glass&#x60; for the dual-control approval read + decision surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiApproveApprovalRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**Approval**](Approval.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## BreakGlassApproval

> Approval BreakGlassApproval(ctx, id).BreakGlassRequest(breakGlassRequest).Execute()

Force a pending Approval via the emergency override.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Approval identifier (UUIDv7). Bound on `/v1/approvals/{id}`, `/v1/approvals/{id}/approve`, `/v1/approvals/{id}/reject`, and `/v1/approvals/{id}/break-glass` for the dual-control approval read + decision surface. 
	breakGlassRequest := *openapiclient.NewBreakGlassRequest("Reason_example") // BreakGlassRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ApprovalsAPI.BreakGlassApproval(context.Background(), id).BreakGlassRequest(breakGlassRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ApprovalsAPI.BreakGlassApproval``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `BreakGlassApproval`: Approval
	fmt.Fprintf(os.Stdout, "Response from `ApprovalsAPI.BreakGlassApproval`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Approval identifier (UUIDv7). Bound on &#x60;/v1/approvals/{id}&#x60;, &#x60;/v1/approvals/{id}/approve&#x60;, &#x60;/v1/approvals/{id}/reject&#x60;, and &#x60;/v1/approvals/{id}/break-glass&#x60; for the dual-control approval read + decision surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiBreakGlassApprovalRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **breakGlassRequest** | [**BreakGlassRequest**](BreakGlassRequest.md) |  | 

### Return type

[**Approval**](Approval.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetApproval

> Approval GetApproval(ctx, id).Execute()

Inspect a single Approval.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Approval identifier (UUIDv7). Bound on `/v1/approvals/{id}`, `/v1/approvals/{id}/approve`, `/v1/approvals/{id}/reject`, and `/v1/approvals/{id}/break-glass` for the dual-control approval read + decision surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ApprovalsAPI.GetApproval(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ApprovalsAPI.GetApproval``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetApproval`: Approval
	fmt.Fprintf(os.Stdout, "Response from `ApprovalsAPI.GetApproval`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Approval identifier (UUIDv7). Bound on &#x60;/v1/approvals/{id}&#x60;, &#x60;/v1/approvals/{id}/approve&#x60;, &#x60;/v1/approvals/{id}/reject&#x60;, and &#x60;/v1/approvals/{id}/break-glass&#x60; for the dual-control approval read + decision surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetApprovalRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**Approval**](Approval.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListApprovals

> ApprovalList ListApprovals(ctx).Status(status).DomainId(domainId).Cursor(cursor).Limit(limit).Execute()

List dual-control Approvals.



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
	status := openapiclient.ApprovalState("proposed") // ApprovalState | Optional lifecycle filter. When present, only Approvals in the named state are returned.  (optional)
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional owning-Domain filter. When present, only Approvals belonging to the named Domain are returned.  (optional)
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ApprovalsAPI.ListApprovals(context.Background()).Status(status).DomainId(domainId).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ApprovalsAPI.ListApprovals``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListApprovals`: ApprovalList
	fmt.Fprintf(os.Stdout, "Response from `ApprovalsAPI.ListApprovals`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListApprovalsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | [**ApprovalState**](ApprovalState.md) | Optional lifecycle filter. When present, only Approvals in the named state are returned.  | 
 **domainId** | **string** | Optional owning-Domain filter. When present, only Approvals belonging to the named Domain are returned.  | 
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**ApprovalList**](ApprovalList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RejectApproval

> Approval RejectApproval(ctx, id).RejectApprovalRequest(rejectApprovalRequest).Execute()

Reject a pending Approval.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Approval identifier (UUIDv7). Bound on `/v1/approvals/{id}`, `/v1/approvals/{id}/approve`, `/v1/approvals/{id}/reject`, and `/v1/approvals/{id}/break-glass` for the dual-control approval read + decision surface. 
	rejectApprovalRequest := *openapiclient.NewRejectApprovalRequest("Reason_example") // RejectApprovalRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ApprovalsAPI.RejectApproval(context.Background(), id).RejectApprovalRequest(rejectApprovalRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ApprovalsAPI.RejectApproval``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RejectApproval`: Approval
	fmt.Fprintf(os.Stdout, "Response from `ApprovalsAPI.RejectApproval`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Approval identifier (UUIDv7). Bound on &#x60;/v1/approvals/{id}&#x60;, &#x60;/v1/approvals/{id}/approve&#x60;, &#x60;/v1/approvals/{id}/reject&#x60;, and &#x60;/v1/approvals/{id}/break-glass&#x60; for the dual-control approval read + decision surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRejectApprovalRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **rejectApprovalRequest** | [**RejectApprovalRequest**](RejectApprovalRequest.md) |  | 

### Return type

[**Approval**](Approval.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

