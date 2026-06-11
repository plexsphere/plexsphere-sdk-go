# \CapabilitiesAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ListCapabilities**](CapabilitiesAPI.md#ListCapabilities) | **Get** /v1/projects/{project_id}/capabilities | List per-Node capability manifests in a Project.



## ListCapabilities

> CapabilityRowList ListCapabilities(ctx, projectId).NodeId(nodeId).Status(status).Cursor(cursor).Limit(limit).Execute()

List per-Node capability manifests in a Project.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). The capability inventory is scoped to Nodes in this Project. 
	nodeId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional Node filter. When present, only the capability row for the named Node is returned.  (optional)
	status := openapiclient.CapabilityStatus("match") // CapabilityStatus | Optional checksum-status filter. When present, only rows in the named status are returned.  (optional)
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CapabilitiesAPI.ListCapabilities(context.Background(), projectId).NodeId(nodeId).Status(status).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CapabilitiesAPI.ListCapabilities``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCapabilities`: CapabilityRowList
	fmt.Fprintf(os.Stdout, "Response from `CapabilitiesAPI.ListCapabilities`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). The capability inventory is scoped to Nodes in this Project.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListCapabilitiesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **nodeId** | **string** | Optional Node filter. When present, only the capability row for the named Node is returned.  | 
 **status** | [**CapabilityStatus**](CapabilityStatus.md) | Optional checksum-status filter. When present, only rows in the named status are returned.  | 
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**CapabilityRowList**](CapabilityRowList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

