# \IntegrityAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AcknowledgeIntegrityViolation**](IntegrityAPI.md#AcknowledgeIntegrityViolation) | **Post** /v1/integrity-violations/{id}/acknowledge | Acknowledge an open integrity violation.
[**ListIntegrityViolations**](IntegrityAPI.md#ListIntegrityViolations) | **Get** /v1/integrity-violations | List integrity violations across Domains.



## AcknowledgeIntegrityViolation

> IntegrityViolationRow AcknowledgeIntegrityViolation(ctx, id).IntegrityViolationAcknowledgeRequest(integrityViolationAcknowledgeRequest).Execute()

Acknowledge an open integrity violation.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Integrity-violation identifier (UUIDv7). Bound on `/v1/integrity-violations/{id}/acknowledge` for the triage acknowledge surface. 
	integrityViolationAcknowledgeRequest := *openapiclient.NewIntegrityViolationAcknowledgeRequest("Reason_example") // IntegrityViolationAcknowledgeRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.IntegrityAPI.AcknowledgeIntegrityViolation(context.Background(), id).IntegrityViolationAcknowledgeRequest(integrityViolationAcknowledgeRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `IntegrityAPI.AcknowledgeIntegrityViolation``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AcknowledgeIntegrityViolation`: IntegrityViolationRow
	fmt.Fprintf(os.Stdout, "Response from `IntegrityAPI.AcknowledgeIntegrityViolation`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Integrity-violation identifier (UUIDv7). Bound on &#x60;/v1/integrity-violations/{id}/acknowledge&#x60; for the triage acknowledge surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiAcknowledgeIntegrityViolationRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **integrityViolationAcknowledgeRequest** | [**IntegrityViolationAcknowledgeRequest**](IntegrityViolationAcknowledgeRequest.md) |  | 

### Return type

[**IntegrityViolationRow**](IntegrityViolationRow.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListIntegrityViolations

> IntegrityViolationList ListIntegrityViolations(ctx).DomainId(domainId).ProjectId(projectId).NodeId(nodeId).Kind(kind).Status(status).Cursor(cursor).Limit(limit).Execute()

List integrity violations across Domains.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional owning-Domain filter. When present, only violations on the named Domain are returned.  (optional)
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional Project filter. When present, only violations on Nodes in the named Project are returned.  (optional)
	nodeId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional Node filter. When present, only violations reported by the named Node are returned.  (optional)
	kind := openapiclient.IntegrityViolationKind("binary") // IntegrityViolationKind | Optional violation-kind filter. Composes with the other filters.  (optional)
	status := openapiclient.IntegrityViolationStatus("open") // IntegrityViolationStatus | Optional lifecycle-status filter. Composes with the other filters.  (optional)
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.IntegrityAPI.ListIntegrityViolations(context.Background()).DomainId(domainId).ProjectId(projectId).NodeId(nodeId).Kind(kind).Status(status).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `IntegrityAPI.ListIntegrityViolations``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListIntegrityViolations`: IntegrityViolationList
	fmt.Fprintf(os.Stdout, "Response from `IntegrityAPI.ListIntegrityViolations`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListIntegrityViolationsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainId** | **string** | Optional owning-Domain filter. When present, only violations on the named Domain are returned.  | 
 **projectId** | **string** | Optional Project filter. When present, only violations on Nodes in the named Project are returned.  | 
 **nodeId** | **string** | Optional Node filter. When present, only violations reported by the named Node are returned.  | 
 **kind** | [**IntegrityViolationKind**](IntegrityViolationKind.md) | Optional violation-kind filter. Composes with the other filters.  | 
 **status** | [**IntegrityViolationStatus**](IntegrityViolationStatus.md) | Optional lifecycle-status filter. Composes with the other filters.  | 
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**IntegrityViolationList**](IntegrityViolationList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

