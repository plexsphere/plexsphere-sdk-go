# \AuthAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DeleteAuthSession**](AuthAPI.md#DeleteAuthSession) | **Delete** /v1/auth/whoami | Sign the current caller out.
[**DeleteAuthTokenByID**](AuthAPI.md#DeleteAuthTokenByID) | **Delete** /v1/auth/tokens/{id} | Immediately revoke an API token.
[**GetAuthCallback**](AuthAPI.md#GetAuthCallback) | **Get** /v1/auth/callback | OIDC redirect callback — exchanges &#x60;code&#x60; for a session.
[**GetAuthTokens**](AuthAPI.md#GetAuthTokens) | **Get** /v1/auth/tokens | List the caller&#39;s API tokens (no plaintext).
[**GetAuthWhoami**](AuthAPI.md#GetAuthWhoami) | **Get** /v1/auth/whoami | Describe the authenticated principal.
[**PostAuthDeviceApprove**](AuthAPI.md#PostAuthDeviceApprove) | **Post** /v1/auth/device/approve | Approve a pending RFC 8628 device-authorization session.
[**PostAuthDeviceCode**](AuthAPI.md#PostAuthDeviceCode) | **Post** /v1/auth/device-code | Initiate an RFC 8628 device-authorization flow.
[**PostAuthDeviceToken**](AuthAPI.md#PostAuthDeviceToken) | **Post** /v1/auth/device-token | Poll for the RFC 8628 device-authorization result.
[**PostAuthServiceToken**](AuthAPI.md#PostAuthServiceToken) | **Post** /v1/auth/service/token | Issue an access token for a ServiceIdentity.
[**PostAuthSignIn**](AuthAPI.md#PostAuthSignIn) | **Post** /v1/auth/sign-in | Initiate an end-user OIDC sign-in (authorization code + PKCE).
[**PostAuthSignOutGlobal**](AuthAPI.md#PostAuthSignOutGlobal) | **Post** /v1/auth/sign-out/global | Sign out of every active session for the caller.
[**PostAuthTokenRotate**](AuthAPI.md#PostAuthTokenRotate) | **Post** /v1/auth/tokens/{id}/rotate | Rotate an API token; old plaintext is retired with Sunset.
[**PostAuthTokens**](AuthAPI.md#PostAuthTokens) | **Post** /v1/auth/tokens | Issue a new API token (psk-shaped) for the caller identity.



## DeleteAuthSession

> DeleteAuthSession(ctx).Execute()

Sign the current caller out.



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

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AuthAPI.DeleteAuthSession(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.DeleteAuthSession``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteAuthSessionRequest struct via the builder pattern


### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteAuthTokenByID

> DeleteAuthTokenByID(ctx, id).Execute()

Immediately revoke an API token.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Token identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AuthAPI.DeleteAuthTokenByID(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.DeleteAuthTokenByID``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Token identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteAuthTokenByIDRequest struct via the builder pattern


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


## GetAuthCallback

> GetAuthCallback(ctx).Code(code).State(state).Execute()

OIDC redirect callback — exchanges `code` for a session.



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
	code := "code_example" // string | Authorization code issued by the IdP.
	state := "state_example" // string | Opaque value used to correlate the redirect.

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AuthAPI.GetAuthCallback(context.Background()).Code(code).State(state).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.GetAuthCallback``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetAuthCallbackRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **code** | **string** | Authorization code issued by the IdP. | 
 **state** | **string** | Opaque value used to correlate the redirect. | 

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


## GetAuthTokens

> []APITokenSummary GetAuthTokens(ctx).Execute()

List the caller's API tokens (no plaintext).



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

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.GetAuthTokens(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.GetAuthTokens``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAuthTokens`: []APITokenSummary
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.GetAuthTokens`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiGetAuthTokensRequest struct via the builder pattern


### Return type

[**[]APITokenSummary**](APITokenSummary.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAuthWhoami

> Whoami GetAuthWhoami(ctx).Execute()

Describe the authenticated principal.



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

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.GetAuthWhoami(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.GetAuthWhoami``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAuthWhoami`: Whoami
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.GetAuthWhoami`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiGetAuthWhoamiRequest struct via the builder pattern


### Return type

[**Whoami**](Whoami.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAuthDeviceApprove

> DeviceApproveResponse PostAuthDeviceApprove(ctx).DeviceApproveRequest(deviceApproveRequest).Execute()

Approve a pending RFC 8628 device-authorization session.



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
	deviceApproveRequest := *openapiclient.NewDeviceApproveRequest("UserCode_example") // DeviceApproveRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.PostAuthDeviceApprove(context.Background()).DeviceApproveRequest(deviceApproveRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.PostAuthDeviceApprove``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAuthDeviceApprove`: DeviceApproveResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.PostAuthDeviceApprove`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthDeviceApproveRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deviceApproveRequest** | [**DeviceApproveRequest**](DeviceApproveRequest.md) |  | 

### Return type

[**DeviceApproveResponse**](DeviceApproveResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAuthDeviceCode

> DeviceCodeResponse PostAuthDeviceCode(ctx).DeviceCodeRequest(deviceCodeRequest).Execute()

Initiate an RFC 8628 device-authorization flow.



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
	deviceCodeRequest := *openapiclient.NewDeviceCodeRequest("DomainId_example", "IdpBindingId_example") // DeviceCodeRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.PostAuthDeviceCode(context.Background()).DeviceCodeRequest(deviceCodeRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.PostAuthDeviceCode``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAuthDeviceCode`: DeviceCodeResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.PostAuthDeviceCode`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthDeviceCodeRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deviceCodeRequest** | [**DeviceCodeRequest**](DeviceCodeRequest.md) |  | 

### Return type

[**DeviceCodeResponse**](DeviceCodeResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAuthDeviceToken

> ServiceTokenResponse PostAuthDeviceToken(ctx).DeviceTokenRequest(deviceTokenRequest).Execute()

Poll for the RFC 8628 device-authorization result.



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
	deviceTokenRequest := *openapiclient.NewDeviceTokenRequest("DeviceCode_example") // DeviceTokenRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.PostAuthDeviceToken(context.Background()).DeviceTokenRequest(deviceTokenRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.PostAuthDeviceToken``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAuthDeviceToken`: ServiceTokenResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.PostAuthDeviceToken`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthDeviceTokenRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **deviceTokenRequest** | [**DeviceTokenRequest**](DeviceTokenRequest.md) |  | 

### Return type

[**ServiceTokenResponse**](ServiceTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAuthServiceToken

> ServiceTokenResponse PostAuthServiceToken(ctx).ServiceTokenRequest(serviceTokenRequest).Execute()

Issue an access token for a ServiceIdentity.



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
	serviceTokenRequest := *openapiclient.NewServiceTokenRequest(openapiclient.ServiceTokenRequest_grant_type("client_credentials")) // ServiceTokenRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.PostAuthServiceToken(context.Background()).ServiceTokenRequest(serviceTokenRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.PostAuthServiceToken``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAuthServiceToken`: ServiceTokenResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.PostAuthServiceToken`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthServiceTokenRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **serviceTokenRequest** | [**ServiceTokenRequest**](ServiceTokenRequest.md) |  | 

### Return type

[**ServiceTokenResponse**](ServiceTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAuthSignIn

> SignInResponse PostAuthSignIn(ctx).SignInRequest(signInRequest).Execute()

Initiate an end-user OIDC sign-in (authorization code + PKCE).



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
	signInRequest := *openapiclient.NewSignInRequest() // SignInRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.PostAuthSignIn(context.Background()).SignInRequest(signInRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.PostAuthSignIn``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAuthSignIn`: SignInResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.PostAuthSignIn`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthSignInRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **signInRequest** | [**SignInRequest**](SignInRequest.md) |  | 

### Return type

[**SignInResponse**](SignInResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAuthSignOutGlobal

> PostAuthSignOutGlobal(ctx).Execute()

Sign out of every active session for the caller.



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

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AuthAPI.PostAuthSignOutGlobal(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.PostAuthSignOutGlobal``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthSignOutGlobalRequest struct via the builder pattern


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


## PostAuthTokenRotate

> APITokenRotateResponse PostAuthTokenRotate(ctx, id).Execute()

Rotate an API token; old plaintext is retired with Sunset.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Token identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.PostAuthTokenRotate(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.PostAuthTokenRotate``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAuthTokenRotate`: APITokenRotateResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.PostAuthTokenRotate`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Token identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthTokenRotateRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**APITokenRotateResponse**](APITokenRotateResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAuthTokens

> APITokenIssueResponse PostAuthTokens(ctx).APITokenIssueRequest(aPITokenIssueRequest).Execute()

Issue a new API token (psk-shaped) for the caller identity.



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
	aPITokenIssueRequest := *openapiclient.NewAPITokenIssueRequest("IdentityRef_example", openapiclient.APITokenIssueRequest_env_prefix("dev")) // APITokenIssueRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuthAPI.PostAuthTokens(context.Background()).APITokenIssueRequest(aPITokenIssueRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuthAPI.PostAuthTokens``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAuthTokens`: APITokenIssueResponse
	fmt.Fprintf(os.Stdout, "Response from `AuthAPI.PostAuthTokens`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAuthTokensRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **aPITokenIssueRequest** | [**APITokenIssueRequest**](APITokenIssueRequest.md) |  | 

### Return type

[**APITokenIssueResponse**](APITokenIssueResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

