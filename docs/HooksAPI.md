# \HooksAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ListHooks**](HooksAPI.md#ListHooks) | **Get** /v1/hooks | List discovered hooks across Domains.



## ListHooks

> HookList ListHooks(ctx).DomainId(domainId).ProjectId(projectId).ImageDigestMatch(imageDigestMatch).Cursor(cursor).Limit(limit).Execute()

List discovered hooks across Domains.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional owning-Domain filter. When present, only hooks on the named Domain are returned.  (optional)
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional Project filter. When present, only hooks on Nodes in the named Project are returned.  (optional)
	imageDigestMatch := true // bool | Optional drift filter. When `true`, only hooks whose discovered image digest matches the declared digest are returned; when `false`, only mismatches are returned.  (optional)
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.HooksAPI.ListHooks(context.Background()).DomainId(domainId).ProjectId(projectId).ImageDigestMatch(imageDigestMatch).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `HooksAPI.ListHooks``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListHooks`: HookList
	fmt.Fprintf(os.Stdout, "Response from `HooksAPI.ListHooks`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListHooksRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainId** | **string** | Optional owning-Domain filter. When present, only hooks on the named Domain are returned.  | 
 **projectId** | **string** | Optional Project filter. When present, only hooks on Nodes in the named Project are returned.  | 
 **imageDigestMatch** | **bool** | Optional drift filter. When &#x60;true&#x60;, only hooks whose discovered image digest matches the declared digest are returned; when &#x60;false&#x60;, only mismatches are returned.  | 
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**HookList**](HookList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

