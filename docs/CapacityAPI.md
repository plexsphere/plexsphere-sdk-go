# \CapacityAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetDomainCapacity**](CapacityAPI.md#GetDomainCapacity) | **Get** /v1/domains/{domainId}/capacity | Return the capacity-and-scale snapshot for a Domain.



## GetDomainCapacity

> DomainCapacitySnapshot GetDomainCapacity(ctx, domainId).Execute()

Return the capacity-and-scale snapshot for a Domain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain's chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CapacityAPI.GetDomainCapacity(context.Background(), domainId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CapacityAPI.GetDomainCapacity``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDomainCapacity`: DomainCapacitySnapshot
	fmt.Fprintf(os.Stdout, "Response from `CapacityAPI.GetDomainCapacity`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDomainCapacityRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**DomainCapacitySnapshot**](DomainCapacitySnapshot.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

