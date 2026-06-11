# \BridgeAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ConfigureBridgeRelay**](BridgeAPI.md#ConfigureBridgeRelay) | **Put** /v1/projects/{project_id}/resources/{resource_id}/bridge/relay | Configure the bridge relay (last-writer-wins replace).
[**CreateBridgeIngressRule**](BridgeAPI.md#CreateBridgeIngressRule) | **Post** /v1/projects/{project_id}/resources/{resource_id}/bridge/ingress | Create a bridge public-ingress rule.
[**CreateBridgeSiteToSiteTunnel**](BridgeAPI.md#CreateBridgeSiteToSiteTunnel) | **Post** /v1/projects/{project_id}/resources/{resource_id}/bridge/site-to-site | Create a bridge site-to-site tunnel.
[**CreateBridgeUserAccessProvider**](BridgeAPI.md#CreateBridgeUserAccessProvider) | **Post** /v1/projects/{project_id}/resources/{resource_id}/bridge/user-access | Create a bridge user-access provider.
[**DeleteBridgeIngressRule**](BridgeAPI.md#DeleteBridgeIngressRule) | **Delete** /v1/projects/{project_id}/resources/{resource_id}/bridge/ingress/{slug} | Delete a bridge public-ingress rule.
[**DeleteBridgeSiteToSiteTunnel**](BridgeAPI.md#DeleteBridgeSiteToSiteTunnel) | **Delete** /v1/projects/{project_id}/resources/{resource_id}/bridge/site-to-site/{slug} | Delete a bridge site-to-site tunnel.
[**DeleteBridgeUserAccessProvider**](BridgeAPI.md#DeleteBridgeUserAccessProvider) | **Delete** /v1/projects/{project_id}/resources/{resource_id}/bridge/user-access/{slug} | Delete a bridge user-access provider.
[**GetBridgeIngressRule**](BridgeAPI.md#GetBridgeIngressRule) | **Get** /v1/projects/{project_id}/resources/{resource_id}/bridge/ingress/{slug} | Fetch a bridge public-ingress rule by slug.
[**GetBridgeRelay**](BridgeAPI.md#GetBridgeRelay) | **Get** /v1/projects/{project_id}/resources/{resource_id}/bridge/relay | Fetch the bridge relay configuration.
[**GetBridgeSiteToSiteTunnel**](BridgeAPI.md#GetBridgeSiteToSiteTunnel) | **Get** /v1/projects/{project_id}/resources/{resource_id}/bridge/site-to-site/{slug} | Fetch a bridge site-to-site tunnel by slug.
[**GetBridgeUserAccessProvider**](BridgeAPI.md#GetBridgeUserAccessProvider) | **Get** /v1/projects/{project_id}/resources/{resource_id}/bridge/user-access/{slug} | Fetch a bridge user-access provider by slug.
[**ListBridgeIngressRules**](BridgeAPI.md#ListBridgeIngressRules) | **Get** /v1/projects/{project_id}/resources/{resource_id}/bridge/ingress | List the bridge public-ingress rules.
[**ListBridgeSiteToSiteTunnels**](BridgeAPI.md#ListBridgeSiteToSiteTunnels) | **Get** /v1/projects/{project_id}/resources/{resource_id}/bridge/site-to-site | List the bridge site-to-site tunnels.
[**ListBridgeUserAccessProviders**](BridgeAPI.md#ListBridgeUserAccessProviders) | **Get** /v1/projects/{project_id}/resources/{resource_id}/bridge/user-access | List the bridge user-access providers.
[**UpdateBridgeIngressRule**](BridgeAPI.md#UpdateBridgeIngressRule) | **Patch** /v1/projects/{project_id}/resources/{resource_id}/bridge/ingress/{slug} | Replace a bridge public-ingress rule&#39;s configuration.
[**UpdateBridgeSiteToSiteTunnel**](BridgeAPI.md#UpdateBridgeSiteToSiteTunnel) | **Patch** /v1/projects/{project_id}/resources/{resource_id}/bridge/site-to-site/{slug} | Replace a bridge site-to-site tunnel&#39;s configuration.
[**UpdateBridgeUserAccessProvider**](BridgeAPI.md#UpdateBridgeUserAccessProvider) | **Patch** /v1/projects/{project_id}/resources/{resource_id}/bridge/user-access/{slug} | Replace a bridge user-access provider&#39;s configuration.



## ConfigureBridgeRelay

> BridgeRelayResponse ConfigureBridgeRelay(ctx, projectId, resourceId).BridgeRelayConfigureRequest(bridgeRelayConfigureRequest).Execute()

Configure the bridge relay (last-writer-wins replace).



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	bridgeRelayConfigureRequest := *openapiclient.NewBridgeRelayConfigureRequest(false, int32(123)) // BridgeRelayConfigureRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.ConfigureBridgeRelay(context.Background(), projectId, resourceId).BridgeRelayConfigureRequest(bridgeRelayConfigureRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.ConfigureBridgeRelay``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ConfigureBridgeRelay`: BridgeRelayResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.ConfigureBridgeRelay`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiConfigureBridgeRelayRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **bridgeRelayConfigureRequest** | [**BridgeRelayConfigureRequest**](BridgeRelayConfigureRequest.md) |  | 

### Return type

[**BridgeRelayResponse**](BridgeRelayResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateBridgeIngressRule

> BridgeIngressRuleResponse CreateBridgeIngressRule(ctx, projectId, resourceId).BridgeIngressRuleCreateRequest(bridgeIngressRuleCreateRequest).Execute()

Create a bridge public-ingress rule.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	bridgeIngressRuleCreateRequest := *openapiclient.NewBridgeIngressRuleCreateRequest("Slug_example", "SniHost_example", "TargetNodeId_example", int32(123)) // BridgeIngressRuleCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.CreateBridgeIngressRule(context.Background(), projectId, resourceId).BridgeIngressRuleCreateRequest(bridgeIngressRuleCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.CreateBridgeIngressRule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateBridgeIngressRule`: BridgeIngressRuleResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.CreateBridgeIngressRule`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateBridgeIngressRuleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **bridgeIngressRuleCreateRequest** | [**BridgeIngressRuleCreateRequest**](BridgeIngressRuleCreateRequest.md) |  | 

### Return type

[**BridgeIngressRuleResponse**](BridgeIngressRuleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateBridgeSiteToSiteTunnel

> BridgeSiteToSiteTunnelResponse CreateBridgeSiteToSiteTunnel(ctx, projectId, resourceId).BridgeSiteToSiteTunnelCreateRequest(bridgeSiteToSiteTunnelCreateRequest).Execute()

Create a bridge site-to-site tunnel.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	bridgeSiteToSiteTunnelCreateRequest := *openapiclient.NewBridgeSiteToSiteTunnelCreateRequest("Slug_example", openapiclient.BridgeSiteToSiteTunnelKind("wireguard"), "RemoteHost_example", int32(123), "AuthSecretRef_example", []string{"AllowedSubnets_example"}, openapiclient.BridgeSiteToSiteTunnelRoutingPolicy("bidirectional")) // BridgeSiteToSiteTunnelCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.CreateBridgeSiteToSiteTunnel(context.Background(), projectId, resourceId).BridgeSiteToSiteTunnelCreateRequest(bridgeSiteToSiteTunnelCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.CreateBridgeSiteToSiteTunnel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateBridgeSiteToSiteTunnel`: BridgeSiteToSiteTunnelResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.CreateBridgeSiteToSiteTunnel`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateBridgeSiteToSiteTunnelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **bridgeSiteToSiteTunnelCreateRequest** | [**BridgeSiteToSiteTunnelCreateRequest**](BridgeSiteToSiteTunnelCreateRequest.md) |  | 

### Return type

[**BridgeSiteToSiteTunnelResponse**](BridgeSiteToSiteTunnelResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateBridgeUserAccessProvider

> BridgeUserAccessProviderResponse CreateBridgeUserAccessProvider(ctx, projectId, resourceId).BridgeUserAccessProviderCreateRequest(bridgeUserAccessProviderCreateRequest).Execute()

Create a bridge user-access provider.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	bridgeUserAccessProviderCreateRequest := *openapiclient.NewBridgeUserAccessProviderCreateRequest("Slug_example", openapiclient.BridgeUserAccessProviderKind("netbird"), "InterfaceName_example", int32(123), int32(123), "AuthSecretRef_example", map[string]interface{}{"key": interface{}(123)}) // BridgeUserAccessProviderCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.CreateBridgeUserAccessProvider(context.Background(), projectId, resourceId).BridgeUserAccessProviderCreateRequest(bridgeUserAccessProviderCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.CreateBridgeUserAccessProvider``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateBridgeUserAccessProvider`: BridgeUserAccessProviderResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.CreateBridgeUserAccessProvider`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateBridgeUserAccessProviderRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **bridgeUserAccessProviderCreateRequest** | [**BridgeUserAccessProviderCreateRequest**](BridgeUserAccessProviderCreateRequest.md) |  | 

### Return type

[**BridgeUserAccessProviderResponse**](BridgeUserAccessProviderResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteBridgeIngressRule

> DeleteBridgeIngressRule(ctx, projectId, resourceId, slug).Execute()

Delete a bridge public-ingress rule.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	slug := "slug_example" // string | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the `/{slug}` sub-resource operations. Unique per `(resource_id, slug)` within its aggregate kind. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.BridgeAPI.DeleteBridgeIngressRule(context.Background(), projectId, resourceId, slug).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.DeleteBridgeIngressRule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 
**slug** | **string** | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the &#x60;/{slug}&#x60; sub-resource operations. Unique per &#x60;(resource_id, slug)&#x60; within its aggregate kind.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteBridgeIngressRuleRequest struct via the builder pattern


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


## DeleteBridgeSiteToSiteTunnel

> DeleteBridgeSiteToSiteTunnel(ctx, projectId, resourceId, slug).Execute()

Delete a bridge site-to-site tunnel.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	slug := "slug_example" // string | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the `/{slug}` sub-resource operations. Unique per `(resource_id, slug)` within its aggregate kind. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.BridgeAPI.DeleteBridgeSiteToSiteTunnel(context.Background(), projectId, resourceId, slug).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.DeleteBridgeSiteToSiteTunnel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 
**slug** | **string** | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the &#x60;/{slug}&#x60; sub-resource operations. Unique per &#x60;(resource_id, slug)&#x60; within its aggregate kind.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteBridgeSiteToSiteTunnelRequest struct via the builder pattern


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


## DeleteBridgeUserAccessProvider

> DeleteBridgeUserAccessProvider(ctx, projectId, resourceId, slug).Execute()

Delete a bridge user-access provider.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	slug := "slug_example" // string | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the `/{slug}` sub-resource operations. Unique per `(resource_id, slug)` within its aggregate kind. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.BridgeAPI.DeleteBridgeUserAccessProvider(context.Background(), projectId, resourceId, slug).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.DeleteBridgeUserAccessProvider``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 
**slug** | **string** | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the &#x60;/{slug}&#x60; sub-resource operations. Unique per &#x60;(resource_id, slug)&#x60; within its aggregate kind.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteBridgeUserAccessProviderRequest struct via the builder pattern


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


## GetBridgeIngressRule

> BridgeIngressRuleResponse GetBridgeIngressRule(ctx, projectId, resourceId, slug).Execute()

Fetch a bridge public-ingress rule by slug.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	slug := "slug_example" // string | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the `/{slug}` sub-resource operations. Unique per `(resource_id, slug)` within its aggregate kind. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.GetBridgeIngressRule(context.Background(), projectId, resourceId, slug).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.GetBridgeIngressRule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBridgeIngressRule`: BridgeIngressRuleResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.GetBridgeIngressRule`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 
**slug** | **string** | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the &#x60;/{slug}&#x60; sub-resource operations. Unique per &#x60;(resource_id, slug)&#x60; within its aggregate kind.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetBridgeIngressRuleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------




### Return type

[**BridgeIngressRuleResponse**](BridgeIngressRuleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetBridgeRelay

> BridgeRelayResponse GetBridgeRelay(ctx, projectId, resourceId).Execute()

Fetch the bridge relay configuration.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.GetBridgeRelay(context.Background(), projectId, resourceId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.GetBridgeRelay``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBridgeRelay`: BridgeRelayResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.GetBridgeRelay`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetBridgeRelayRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**BridgeRelayResponse**](BridgeRelayResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetBridgeSiteToSiteTunnel

> BridgeSiteToSiteTunnelResponse GetBridgeSiteToSiteTunnel(ctx, projectId, resourceId, slug).Execute()

Fetch a bridge site-to-site tunnel by slug.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	slug := "slug_example" // string | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the `/{slug}` sub-resource operations. Unique per `(resource_id, slug)` within its aggregate kind. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.GetBridgeSiteToSiteTunnel(context.Background(), projectId, resourceId, slug).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.GetBridgeSiteToSiteTunnel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBridgeSiteToSiteTunnel`: BridgeSiteToSiteTunnelResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.GetBridgeSiteToSiteTunnel`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 
**slug** | **string** | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the &#x60;/{slug}&#x60; sub-resource operations. Unique per &#x60;(resource_id, slug)&#x60; within its aggregate kind.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetBridgeSiteToSiteTunnelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------




### Return type

[**BridgeSiteToSiteTunnelResponse**](BridgeSiteToSiteTunnelResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetBridgeUserAccessProvider

> BridgeUserAccessProviderResponse GetBridgeUserAccessProvider(ctx, projectId, resourceId, slug).Execute()

Fetch a bridge user-access provider by slug.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	slug := "slug_example" // string | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the `/{slug}` sub-resource operations. Unique per `(resource_id, slug)` within its aggregate kind. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.GetBridgeUserAccessProvider(context.Background(), projectId, resourceId, slug).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.GetBridgeUserAccessProvider``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBridgeUserAccessProvider`: BridgeUserAccessProviderResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.GetBridgeUserAccessProvider`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 
**slug** | **string** | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the &#x60;/{slug}&#x60; sub-resource operations. Unique per &#x60;(resource_id, slug)&#x60; within its aggregate kind.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetBridgeUserAccessProviderRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------




### Return type

[**BridgeUserAccessProviderResponse**](BridgeUserAccessProviderResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListBridgeIngressRules

> BridgeIngressRuleList ListBridgeIngressRules(ctx, projectId, resourceId).Execute()

List the bridge public-ingress rules.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.ListBridgeIngressRules(context.Background(), projectId, resourceId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.ListBridgeIngressRules``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListBridgeIngressRules`: BridgeIngressRuleList
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.ListBridgeIngressRules`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListBridgeIngressRulesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**BridgeIngressRuleList**](BridgeIngressRuleList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListBridgeSiteToSiteTunnels

> BridgeSiteToSiteTunnelList ListBridgeSiteToSiteTunnels(ctx, projectId, resourceId).Execute()

List the bridge site-to-site tunnels.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.ListBridgeSiteToSiteTunnels(context.Background(), projectId, resourceId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.ListBridgeSiteToSiteTunnels``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListBridgeSiteToSiteTunnels`: BridgeSiteToSiteTunnelList
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.ListBridgeSiteToSiteTunnels`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListBridgeSiteToSiteTunnelsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**BridgeSiteToSiteTunnelList**](BridgeSiteToSiteTunnelList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListBridgeUserAccessProviders

> BridgeUserAccessProviderList ListBridgeUserAccessProviders(ctx, projectId, resourceId).Execute()

List the bridge user-access providers.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.ListBridgeUserAccessProviders(context.Background(), projectId, resourceId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.ListBridgeUserAccessProviders``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListBridgeUserAccessProviders`: BridgeUserAccessProviderList
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.ListBridgeUserAccessProviders`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListBridgeUserAccessProvidersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**BridgeUserAccessProviderList**](BridgeUserAccessProviderList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateBridgeIngressRule

> BridgeIngressRuleResponse UpdateBridgeIngressRule(ctx, projectId, resourceId, slug).BridgeIngressRuleUpdateRequest(bridgeIngressRuleUpdateRequest).Execute()

Replace a bridge public-ingress rule's configuration.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	slug := "slug_example" // string | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the `/{slug}` sub-resource operations. Unique per `(resource_id, slug)` within its aggregate kind. 
	bridgeIngressRuleUpdateRequest := *openapiclient.NewBridgeIngressRuleUpdateRequest("SniHost_example", "TargetNodeId_example", int32(123)) // BridgeIngressRuleUpdateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.UpdateBridgeIngressRule(context.Background(), projectId, resourceId, slug).BridgeIngressRuleUpdateRequest(bridgeIngressRuleUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.UpdateBridgeIngressRule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateBridgeIngressRule`: BridgeIngressRuleResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.UpdateBridgeIngressRule`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 
**slug** | **string** | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the &#x60;/{slug}&#x60; sub-resource operations. Unique per &#x60;(resource_id, slug)&#x60; within its aggregate kind.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateBridgeIngressRuleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **bridgeIngressRuleUpdateRequest** | [**BridgeIngressRuleUpdateRequest**](BridgeIngressRuleUpdateRequest.md) |  | 

### Return type

[**BridgeIngressRuleResponse**](BridgeIngressRuleResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateBridgeSiteToSiteTunnel

> BridgeSiteToSiteTunnelResponse UpdateBridgeSiteToSiteTunnel(ctx, projectId, resourceId, slug).BridgeSiteToSiteTunnelUpdateRequest(bridgeSiteToSiteTunnelUpdateRequest).Execute()

Replace a bridge site-to-site tunnel's configuration.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	slug := "slug_example" // string | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the `/{slug}` sub-resource operations. Unique per `(resource_id, slug)` within its aggregate kind. 
	bridgeSiteToSiteTunnelUpdateRequest := *openapiclient.NewBridgeSiteToSiteTunnelUpdateRequest(openapiclient.BridgeSiteToSiteTunnelKind("wireguard"), "RemoteHost_example", int32(123), "AuthSecretRef_example", []string{"AllowedSubnets_example"}, openapiclient.BridgeSiteToSiteTunnelRoutingPolicy("bidirectional")) // BridgeSiteToSiteTunnelUpdateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.UpdateBridgeSiteToSiteTunnel(context.Background(), projectId, resourceId, slug).BridgeSiteToSiteTunnelUpdateRequest(bridgeSiteToSiteTunnelUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.UpdateBridgeSiteToSiteTunnel``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateBridgeSiteToSiteTunnel`: BridgeSiteToSiteTunnelResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.UpdateBridgeSiteToSiteTunnel`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 
**slug** | **string** | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the &#x60;/{slug}&#x60; sub-resource operations. Unique per &#x60;(resource_id, slug)&#x60; within its aggregate kind.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateBridgeSiteToSiteTunnelRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **bridgeSiteToSiteTunnelUpdateRequest** | [**BridgeSiteToSiteTunnelUpdateRequest**](BridgeSiteToSiteTunnelUpdateRequest.md) |  | 

### Return type

[**BridgeSiteToSiteTunnelResponse**](BridgeSiteToSiteTunnelResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateBridgeUserAccessProvider

> BridgeUserAccessProviderResponse UpdateBridgeUserAccessProvider(ctx, projectId, resourceId, slug).BridgeUserAccessProviderUpdateRequest(bridgeUserAccessProviderUpdateRequest).Execute()

Replace a bridge user-access provider's configuration.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/resources` for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under `/v1/projects/{project_id}/resources/{resource_id}/bridge/...`. 
	resourceId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Addressed bridge Resource (UUIDv7). Bound on every `/v1/projects/{project_id}/resources/{resource_id}/bridge/...` operation. A Resource that exists but is not kind `bridge` surfaces as `409 resource_not_bridge` on every mutating call. 
	slug := "slug_example" // string | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the `/{slug}` sub-resource operations. Unique per `(resource_id, slug)` within its aggregate kind. 
	bridgeUserAccessProviderUpdateRequest := *openapiclient.NewBridgeUserAccessProviderUpdateRequest(openapiclient.BridgeUserAccessProviderKind("netbird"), "InterfaceName_example", int32(123), int32(123), "AuthSecretRef_example", map[string]interface{}{"key": interface{}(123)}) // BridgeUserAccessProviderUpdateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.BridgeAPI.UpdateBridgeUserAccessProvider(context.Background(), projectId, resourceId, slug).BridgeUserAccessProviderUpdateRequest(bridgeUserAccessProviderUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BridgeAPI.UpdateBridgeUserAccessProvider``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateBridgeUserAccessProvider`: BridgeUserAccessProviderResponse
	fmt.Fprintf(os.Stdout, "Response from `BridgeAPI.UpdateBridgeUserAccessProvider`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/resources&#x60; for the Resource collection — create and list. Reused by the Bridge Orchestrator surface under &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60;.  | 
**resourceId** | **string** | Addressed bridge Resource (UUIDv7). Bound on every &#x60;/v1/projects/{project_id}/resources/{resource_id}/bridge/...&#x60; operation. A Resource that exists but is not kind &#x60;bridge&#x60; surfaces as &#x60;409 resource_not_bridge&#x60; on every mutating call.  | 
**slug** | **string** | Stable slug of a bridge user-access provider, public-ingress rule, or site-to-site tunnel. Bound on the &#x60;/{slug}&#x60; sub-resource operations. Unique per &#x60;(resource_id, slug)&#x60; within its aggregate kind.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateBridgeUserAccessProviderRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



 **bridgeUserAccessProviderUpdateRequest** | [**BridgeUserAccessProviderUpdateRequest**](BridgeUserAccessProviderUpdateRequest.md) |  | 

### Return type

[**BridgeUserAccessProviderResponse**](BridgeUserAccessProviderResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

