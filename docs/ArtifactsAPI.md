# \ArtifactsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetPlexdArtifact**](ArtifactsAPI.md#GetPlexdArtifact) | **Get** /v1/artifacts/plexd/{version} | Fetch one indexed plexd release by version.
[**GetPlexdArtifactSignature**](ArtifactsAPI.md#GetPlexdArtifactSignature) | **Get** /v1/artifacts/plexd/{version}/sigstore | Fetch the verbatim Sigstore bundle for a plexd release.
[**ListPlexdArtifacts**](ArtifactsAPI.md#ListPlexdArtifacts) | **Get** /v1/artifacts/plexd | List indexed plexd releases.



## GetPlexdArtifact

> PlexdArtifact GetPlexdArtifact(ctx, version).Authorization(authorization).Execute()

Fetch one indexed plexd release by version.



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
	version := "version_example" // string | plexd release version the registry indexes — the upstream release tag, for example a semver tag such as `v1.4.2`. Bound on `/v1/artifacts/plexd/{version}` and its `.sigstore` companion for the read-only plexd release registry surface. 
	authorization := "authorization_example" // string | `Bearer <access token>` — the operator bearer credential the request authenticates with. A missing, malformed, or rejected token surfaces as `401`. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ArtifactsAPI.GetPlexdArtifact(context.Background(), version).Authorization(authorization).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ArtifactsAPI.GetPlexdArtifact``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetPlexdArtifact`: PlexdArtifact
	fmt.Fprintf(os.Stdout, "Response from `ArtifactsAPI.GetPlexdArtifact`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**version** | **string** | plexd release version the registry indexes — the upstream release tag, for example a semver tag such as &#x60;v1.4.2&#x60;. Bound on &#x60;/v1/artifacts/plexd/{version}&#x60; and its &#x60;.sigstore&#x60; companion for the read-only plexd release registry surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetPlexdArtifactRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **authorization** | **string** | &#x60;Bearer &lt;access token&gt;&#x60; — the operator bearer credential the request authenticates with. A missing, malformed, or rejected token surfaces as &#x60;401&#x60;.  | 

### Return type

[**PlexdArtifact**](PlexdArtifact.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetPlexdArtifactSignature

> *os.File GetPlexdArtifactSignature(ctx, version).Authorization(authorization).Execute()

Fetch the verbatim Sigstore bundle for a plexd release.



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
	version := "version_example" // string | plexd release version the registry indexes — the upstream release tag, for example a semver tag such as `v1.4.2`. Bound on `/v1/artifacts/plexd/{version}` and its `.sigstore` companion for the read-only plexd release registry surface. 
	authorization := "authorization_example" // string | `Bearer <access token>` — the operator bearer credential the request authenticates with. A missing, malformed, or rejected token surfaces as `401`. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ArtifactsAPI.GetPlexdArtifactSignature(context.Background(), version).Authorization(authorization).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ArtifactsAPI.GetPlexdArtifactSignature``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetPlexdArtifactSignature`: *os.File
	fmt.Fprintf(os.Stdout, "Response from `ArtifactsAPI.GetPlexdArtifactSignature`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**version** | **string** | plexd release version the registry indexes — the upstream release tag, for example a semver tag such as &#x60;v1.4.2&#x60;. Bound on &#x60;/v1/artifacts/plexd/{version}&#x60; and its &#x60;.sigstore&#x60; companion for the read-only plexd release registry surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetPlexdArtifactSignatureRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **authorization** | **string** | &#x60;Bearer &lt;access token&gt;&#x60; — the operator bearer credential the request authenticates with. A missing, malformed, or rejected token surfaces as &#x60;401&#x60;.  | 

### Return type

[***os.File**](*os.File.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListPlexdArtifacts

> PlexdArtifactRefList ListPlexdArtifacts(ctx).Authorization(authorization).Cursor(cursor).Limit(limit).Execute()

List indexed plexd releases.



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
	authorization := "authorization_example" // string | `Bearer <access token>` — the operator bearer credential the request authenticates with. A missing, malformed, or rejected token surfaces as `401`. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ArtifactsAPI.ListPlexdArtifacts(context.Background()).Authorization(authorization).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ArtifactsAPI.ListPlexdArtifacts``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListPlexdArtifacts`: PlexdArtifactRefList
	fmt.Fprintf(os.Stdout, "Response from `ArtifactsAPI.ListPlexdArtifacts`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListPlexdArtifactsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorization** | **string** | &#x60;Bearer &lt;access token&gt;&#x60; — the operator bearer credential the request authenticates with. A missing, malformed, or rejected token surfaces as &#x60;401&#x60;.  | 
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**PlexdArtifactRefList**](PlexdArtifactRefList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

