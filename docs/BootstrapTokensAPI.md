# \BootstrapTokensAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetBootstrapTokenMetadata**](BootstrapTokensAPI.md#GetBootstrapTokenMetadata) | **Get** /v1/projects/{project_id}/bootstrap-tokens/{id} | Fetch BootstrapToken metadata by identifier.
[**IssueBootstrapToken**](BootstrapTokensAPI.md#IssueBootstrapToken) | **Post** /v1/projects/{project_id}/bootstrap-tokens | Issue a BootstrapToken for a Project.
[**ListBootstrapTokens**](BootstrapTokensAPI.md#ListBootstrapTokens) | **Get** /v1/projects/{project_id}/bootstrap-tokens | List BootstrapTokens issued for a Project.
[**PostRegister**](BootstrapTokensAPI.md#PostRegister) | **Post** /v1/register | Redeem a BootstrapToken to enrol a Node into a Domain.
[**RevokeBootstrapToken**](BootstrapTokensAPI.md#RevokeBootstrapToken) | **Delete** /v1/projects/{project_id}/bootstrap-tokens/{id} | Revoke a BootstrapToken.



## GetBootstrapTokenMetadata

> BootstrapTokenMetadata GetBootstrapTokenMetadata(ctx, projectId, id).Execute()

Fetch BootstrapToken metadata by identifier.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The BootstrapToken aggregate is scoped per Project so every administration endpoint requires the Project identifier in the path. 
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | BootstrapToken identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BootstrapTokensAPI.GetBootstrapTokenMetadata(context.Background(), projectId, id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BootstrapTokensAPI.GetBootstrapTokenMetadata``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBootstrapTokenMetadata`: BootstrapTokenMetadata
	fmt.Fprintf(os.Stdout, "Response from `BootstrapTokensAPI.GetBootstrapTokenMetadata`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The BootstrapToken aggregate is scoped per Project so every administration endpoint requires the Project identifier in the path.  | 
**id** | **string** | BootstrapToken identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetBootstrapTokenMetadataRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**BootstrapTokenMetadata**](BootstrapTokenMetadata.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## IssueBootstrapToken

> BootstrapTokenIssueResponse IssueBootstrapToken(ctx, projectId).BootstrapTokenIssueRequest(bootstrapTokenIssueRequest).Execute()

Issue a BootstrapToken for a Project.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The BootstrapToken aggregate is scoped per Project so every administration endpoint requires the Project identifier in the path. 
	bootstrapTokenIssueRequest := *openapiclient.NewBootstrapTokenIssueRequest(openapiclient.BootstrapTokenIssueRequest_kind("node"), "EnvPrefix_example", int32(123)) // BootstrapTokenIssueRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BootstrapTokensAPI.IssueBootstrapToken(context.Background(), projectId).BootstrapTokenIssueRequest(bootstrapTokenIssueRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BootstrapTokensAPI.IssueBootstrapToken``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `IssueBootstrapToken`: BootstrapTokenIssueResponse
	fmt.Fprintf(os.Stdout, "Response from `BootstrapTokensAPI.IssueBootstrapToken`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The BootstrapToken aggregate is scoped per Project so every administration endpoint requires the Project identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiIssueBootstrapTokenRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **bootstrapTokenIssueRequest** | [**BootstrapTokenIssueRequest**](BootstrapTokenIssueRequest.md) |  | 

### Return type

[**BootstrapTokenIssueResponse**](BootstrapTokenIssueResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListBootstrapTokens

> BootstrapTokenList ListBootstrapTokens(ctx, projectId).Cursor(cursor).Limit(limit).Execute()

List BootstrapTokens issued for a Project.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The BootstrapToken aggregate is scoped per Project so every administration endpoint requires the Project identifier in the path. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page .  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BootstrapTokensAPI.ListBootstrapTokens(context.Background(), projectId).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BootstrapTokensAPI.ListBootstrapTokens``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListBootstrapTokens`: BootstrapTokenList
	fmt.Fprintf(os.Stdout, "Response from `BootstrapTokensAPI.ListBootstrapTokens`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The BootstrapToken aggregate is scoped per Project so every administration endpoint requires the Project identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListBootstrapTokensRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page .  | [default to 50]

### Return type

[**BootstrapTokenList**](BootstrapTokenList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostRegister

> RegisterResponse PostRegister(ctx).RegisterRequest(registerRequest).Execute()

Redeem a BootstrapToken to enrol a Node into a Domain.



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
	registerRequest := *openapiclient.NewRegisterRequest("ProjectId_example", "ResourceId_example", "BootstrapToken_example", "Nonce_example", "PublicKey_example") // RegisterRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BootstrapTokensAPI.PostRegister(context.Background()).RegisterRequest(registerRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BootstrapTokensAPI.PostRegister``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostRegister`: RegisterResponse
	fmt.Fprintf(os.Stdout, "Response from `BootstrapTokensAPI.PostRegister`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostRegisterRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **registerRequest** | [**RegisterRequest**](RegisterRequest.md) |  | 

### Return type

[**RegisterResponse**](RegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RevokeBootstrapToken

> RevokeBootstrapToken(ctx, projectId, id).Execute()

Revoke a BootstrapToken.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The BootstrapToken aggregate is scoped per Project so every administration endpoint requires the Project identifier in the path. 
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | BootstrapToken identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.BootstrapTokensAPI.RevokeBootstrapToken(context.Background(), projectId, id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BootstrapTokensAPI.RevokeBootstrapToken``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The BootstrapToken aggregate is scoped per Project so every administration endpoint requires the Project identifier in the path.  | 
**id** | **string** | BootstrapToken identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiRevokeBootstrapTokenRequest struct via the builder pattern


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

