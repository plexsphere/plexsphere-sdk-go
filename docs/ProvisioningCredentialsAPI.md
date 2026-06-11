# \ProvisioningCredentialsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetCredential**](ProvisioningCredentialsAPI.md#GetCredential) | **Get** /v1/credentials/{id} | Fetch a credential&#39;s lifecycle metadata.
[**ListProjectCredentials**](ProvisioningCredentialsAPI.md#ListProjectCredentials) | **Get** /v1/projects/{id}/credentials | List the OpenBao credentials owned by a Project.
[**RevokeCredential**](ProvisioningCredentialsAPI.md#RevokeCredential) | **Post** /v1/credentials/{id}/revoke | Revoke a credential.
[**RotateCredential**](ProvisioningCredentialsAPI.md#RotateCredential) | **Post** /v1/credentials/{id}/rotate | Rotate a credential&#39;s underlying secret.



## GetCredential

> CredentialResponse GetCredential(ctx, id).Execute()

Fetch a credential's lifecycle metadata.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Credential identifier (UUIDv7). Bound on `/v1/credentials/{id}`, `/v1/credentials/{id}/revoke`, and `/v1/credentials/{id}/rotate` for the operator-facing OpenBao Credential Broker read + lifecycle surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ProvisioningCredentialsAPI.GetCredential(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ProvisioningCredentialsAPI.GetCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetCredential`: CredentialResponse
	fmt.Fprintf(os.Stdout, "Response from `ProvisioningCredentialsAPI.GetCredential`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Credential identifier (UUIDv7). Bound on &#x60;/v1/credentials/{id}&#x60;, &#x60;/v1/credentials/{id}/revoke&#x60;, and &#x60;/v1/credentials/{id}/rotate&#x60; for the operator-facing OpenBao Credential Broker read + lifecycle surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**CredentialResponse**](CredentialResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListProjectCredentials

> CredentialList ListProjectCredentials(ctx, id).Cursor(cursor).Limit(limit).Execute()

List the OpenBao credentials owned by a Project.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Project identifier (UUIDv7). Bound on `/v1/projects/{id}` for the tenancy CRUD surface and on `/v1/projects/{id}/credentials` for the operator-facing OpenBao Credential Broker inventory list. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ProvisioningCredentialsAPI.ListProjectCredentials(context.Background(), id).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ProvisioningCredentialsAPI.ListProjectCredentials``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListProjectCredentials`: CredentialList
	fmt.Fprintf(os.Stdout, "Response from `ProvisioningCredentialsAPI.ListProjectCredentials`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface and on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListProjectCredentialsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**CredentialList**](CredentialList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RevokeCredential

> CredentialResponse RevokeCredential(ctx, id).CredentialRevokeRequest(credentialRevokeRequest).Execute()

Revoke a credential.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Credential identifier (UUIDv7). Bound on `/v1/credentials/{id}`, `/v1/credentials/{id}/revoke`, and `/v1/credentials/{id}/rotate` for the operator-facing OpenBao Credential Broker read + lifecycle surface. 
	credentialRevokeRequest := *openapiclient.NewCredentialRevokeRequest("Reason_example") // CredentialRevokeRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ProvisioningCredentialsAPI.RevokeCredential(context.Background(), id).CredentialRevokeRequest(credentialRevokeRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ProvisioningCredentialsAPI.RevokeCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RevokeCredential`: CredentialResponse
	fmt.Fprintf(os.Stdout, "Response from `ProvisioningCredentialsAPI.RevokeCredential`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Credential identifier (UUIDv7). Bound on &#x60;/v1/credentials/{id}&#x60;, &#x60;/v1/credentials/{id}/revoke&#x60;, and &#x60;/v1/credentials/{id}/rotate&#x60; for the operator-facing OpenBao Credential Broker read + lifecycle surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRevokeCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **credentialRevokeRequest** | [**CredentialRevokeRequest**](CredentialRevokeRequest.md) |  | 

### Return type

[**CredentialResponse**](CredentialResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RotateCredential

> CredentialResponse RotateCredential(ctx, id).CredentialRotateRequest(credentialRotateRequest).Execute()

Rotate a credential's underlying secret.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Credential identifier (UUIDv7). Bound on `/v1/credentials/{id}`, `/v1/credentials/{id}/revoke`, and `/v1/credentials/{id}/rotate` for the operator-facing OpenBao Credential Broker read + lifecycle surface. 
	credentialRotateRequest := *openapiclient.NewCredentialRotateRequest(int64(123), *openapiclient.NewCredentialRotateMaterial(string(123), int64(123))) // CredentialRotateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ProvisioningCredentialsAPI.RotateCredential(context.Background(), id).CredentialRotateRequest(credentialRotateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ProvisioningCredentialsAPI.RotateCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RotateCredential`: CredentialResponse
	fmt.Fprintf(os.Stdout, "Response from `ProvisioningCredentialsAPI.RotateCredential`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Credential identifier (UUIDv7). Bound on &#x60;/v1/credentials/{id}&#x60;, &#x60;/v1/credentials/{id}/revoke&#x60;, and &#x60;/v1/credentials/{id}/rotate&#x60; for the operator-facing OpenBao Credential Broker read + lifecycle surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRotateCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **credentialRotateRequest** | [**CredentialRotateRequest**](CredentialRotateRequest.md) |  | 

### Return type

[**CredentialResponse**](CredentialResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

