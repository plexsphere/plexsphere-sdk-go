# \SinksAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateSink**](SinksAPI.md#CreateSink) | **Post** /v1/domains/{id}/sinks | Declare a telemetry sink for a Domain.
[**CreateTelemetryRoute**](SinksAPI.md#CreateTelemetryRoute) | **Post** /v1/projects/{id}/telemetry-routes | Create a Telemetry Route for a Project.
[**DeleteSink**](SinksAPI.md#DeleteSink) | **Delete** /v1/sinks/{id} | Delete a tenant sink.
[**DeleteTelemetryRoute**](SinksAPI.md#DeleteTelemetryRoute) | **Delete** /v1/telemetry-routes/{id} | Delete a Telemetry Route.
[**GetSink**](SinksAPI.md#GetSink) | **Get** /v1/sinks/{id} | Read a single sink.
[**GetTelemetryRoute**](SinksAPI.md#GetTelemetryRoute) | **Get** /v1/telemetry-routes/{id} | Read a single Telemetry Route.
[**GrantSinkEnablement**](SinksAPI.md#GrantSinkEnablement) | **Post** /v1/sinks/{id}/sink-enablements | Grant a sink to a Project (owner push).
[**ListBuiltInSinks**](SinksAPI.md#ListBuiltInSinks) | **Get** /v1/sinks/built-in | List the built-in sinks the platform operates.
[**ListDomainSinks**](SinksAPI.md#ListDomainSinks) | **Get** /v1/domains/{id}/sinks | List the tenant sinks a Domain declares.
[**ListSinkEnablements**](SinksAPI.md#ListSinkEnablements) | **Get** /v1/projects/{id}/sink-enablements | List the sink enablements owned by a Project.
[**ListTelemetryRoutes**](SinksAPI.md#ListTelemetryRoutes) | **Get** /v1/projects/{id}/telemetry-routes | List the Telemetry Routes a Project holds.
[**RequestSinkEnablement**](SinksAPI.md#RequestSinkEnablement) | **Post** /v1/projects/{id}/sink-enablements | Request a sink enablement for a Project.
[**RevokeSinkEnablement**](SinksAPI.md#RevokeSinkEnablement) | **Post** /v1/sink-enablements/{id}/revoke | Revoke a sink enablement.
[**UpdateSink**](SinksAPI.md#UpdateSink) | **Put** /v1/sinks/{id} | Replace a tenant sink&#39;s mutable state.
[**UpdateTelemetryRoute**](SinksAPI.md#UpdateTelemetryRoute) | **Put** /v1/telemetry-routes/{id} | Replace a Telemetry Route&#39;s state.



## CreateSink

> Sink CreateSink(ctx, id).SinkCreateRequest(sinkCreateRequest).Execute()

Declare a telemetry sink for a Domain.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Domain identifier (UUIDv7). Bound on `/v1/domains/{id}` for the tenancy CRUD surface. 
	sinkCreateRequest := *openapiclient.NewSinkCreateRequest("Slug_example", "DisplayName_example", openapiclient.TenantSinkType("otlp"), "Endpoint_example") // SinkCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.CreateSink(context.Background(), id).SinkCreateRequest(sinkCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.CreateSink``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateSink`: Sink
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.CreateSink`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateSinkRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **sinkCreateRequest** | [**SinkCreateRequest**](SinkCreateRequest.md) |  | 

### Return type

[**Sink**](Sink.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateTelemetryRoute

> TelemetryRoute CreateTelemetryRoute(ctx, id).TelemetryRouteRequest(telemetryRouteRequest).Execute()

Create a Telemetry Route for a Project.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Project identifier (UUIDv7). Bound on `/v1/projects/{id}` for the tenancy CRUD surface, on `/v1/projects/{id}/credentials` for the operator-facing OpenBao Credential Broker inventory list, on `/v1/projects/{id}/credential-assignments` and `/v1/projects/{id}/cloud-assignments` for the assignment request/list surfaces, on `/v1/projects/{id}/blueprints` for the project-scoped Blueprint offer list, and on `/v1/projects/{id}/sink-enablements` and `/v1/projects/{id}/telemetry-routes` for the sink-enablement and Telemetry Route surfaces. 
	telemetryRouteRequest := *openapiclient.NewTelemetryRouteRequest(openapiclient.TelemetrySignal("metrics"), []string{"SinkIds_example"}) // TelemetryRouteRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.CreateTelemetryRoute(context.Background(), id).TelemetryRouteRequest(telemetryRouteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.CreateTelemetryRoute``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateTelemetryRoute`: TelemetryRoute
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.CreateTelemetryRoute`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface, on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list, on &#x60;/v1/projects/{id}/credential-assignments&#x60; and &#x60;/v1/projects/{id}/cloud-assignments&#x60; for the assignment request/list surfaces, on &#x60;/v1/projects/{id}/blueprints&#x60; for the project-scoped Blueprint offer list, and on &#x60;/v1/projects/{id}/sink-enablements&#x60; and &#x60;/v1/projects/{id}/telemetry-routes&#x60; for the sink-enablement and Telemetry Route surfaces.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateTelemetryRouteRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **telemetryRouteRequest** | [**TelemetryRouteRequest**](TelemetryRouteRequest.md) |  | 

### Return type

[**TelemetryRoute**](TelemetryRoute.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteSink

> DeleteSink(ctx, id).Execute()

Delete a tenant sink.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Sink identifier (UUIDv7). Bound on `/v1/sinks/{id}` for the single-sink read, replace, and delete, and on `/v1/sinks/{id}/sink-enablements` for the owner-push grant. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.SinksAPI.DeleteSink(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.DeleteSink``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Sink identifier (UUIDv7). Bound on &#x60;/v1/sinks/{id}&#x60; for the single-sink read, replace, and delete, and on &#x60;/v1/sinks/{id}/sink-enablements&#x60; for the owner-push grant.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteSinkRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

 (empty response body)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteTelemetryRoute

> DeleteTelemetryRoute(ctx, id).Execute()

Delete a Telemetry Route.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Telemetry Route identifier (UUIDv7). Bound on `/v1/telemetry-routes/{id}` for the single-route read, replace, and delete. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.SinksAPI.DeleteTelemetryRoute(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.DeleteTelemetryRoute``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Telemetry Route identifier (UUIDv7). Bound on &#x60;/v1/telemetry-routes/{id}&#x60; for the single-route read, replace, and delete.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteTelemetryRouteRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

 (empty response body)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetSink

> Sink GetSink(ctx, id).Execute()

Read a single sink.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Sink identifier (UUIDv7). Bound on `/v1/sinks/{id}` for the single-sink read, replace, and delete, and on `/v1/sinks/{id}/sink-enablements` for the owner-push grant. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.GetSink(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.GetSink``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetSink`: Sink
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.GetSink`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Sink identifier (UUIDv7). Bound on &#x60;/v1/sinks/{id}&#x60; for the single-sink read, replace, and delete, and on &#x60;/v1/sinks/{id}/sink-enablements&#x60; for the owner-push grant.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetSinkRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**Sink**](Sink.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetTelemetryRoute

> TelemetryRoute GetTelemetryRoute(ctx, id).Execute()

Read a single Telemetry Route.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Telemetry Route identifier (UUIDv7). Bound on `/v1/telemetry-routes/{id}` for the single-route read, replace, and delete. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.GetTelemetryRoute(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.GetTelemetryRoute``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetTelemetryRoute`: TelemetryRoute
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.GetTelemetryRoute`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Telemetry Route identifier (UUIDv7). Bound on &#x60;/v1/telemetry-routes/{id}&#x60; for the single-route read, replace, and delete.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetTelemetryRouteRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**TelemetryRoute**](TelemetryRoute.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GrantSinkEnablement

> SinkEnablement GrantSinkEnablement(ctx, id).SinkEnablementGrantBody(sinkEnablementGrantBody).Execute()

Grant a sink to a Project (owner push).



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Sink identifier (UUIDv7). Bound on `/v1/sinks/{id}` for the single-sink read, replace, and delete, and on `/v1/sinks/{id}/sink-enablements` for the owner-push grant. 
	sinkEnablementGrantBody := *openapiclient.NewSinkEnablementGrantBody("ProjectId_example") // SinkEnablementGrantBody | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.GrantSinkEnablement(context.Background(), id).SinkEnablementGrantBody(sinkEnablementGrantBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.GrantSinkEnablement``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GrantSinkEnablement`: SinkEnablement
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.GrantSinkEnablement`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Sink identifier (UUIDv7). Bound on &#x60;/v1/sinks/{id}&#x60; for the single-sink read, replace, and delete, and on &#x60;/v1/sinks/{id}/sink-enablements&#x60; for the owner-push grant.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGrantSinkEnablementRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **sinkEnablementGrantBody** | [**SinkEnablementGrantBody**](SinkEnablementGrantBody.md) |  | 

### Return type

[**SinkEnablement**](SinkEnablement.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListBuiltInSinks

> SinkList ListBuiltInSinks(ctx).Execute()

List the built-in sinks the platform operates.



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
	resp, r, err := apiClient.SinksAPI.ListBuiltInSinks(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.ListBuiltInSinks``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListBuiltInSinks`: SinkList
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.ListBuiltInSinks`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiListBuiltInSinksRequest struct via the builder pattern


### Return type

[**SinkList**](SinkList.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListDomainSinks

> SinkList ListDomainSinks(ctx, id).Execute()

List the tenant sinks a Domain declares.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Domain identifier (UUIDv7). Bound on `/v1/domains/{id}` for the tenancy CRUD surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.ListDomainSinks(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.ListDomainSinks``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListDomainSinks`: SinkList
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.ListDomainSinks`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListDomainSinksRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**SinkList**](SinkList.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListSinkEnablements

> SinkEnablementPage ListSinkEnablements(ctx, id).Cursor(cursor).Limit(limit).Execute()

List the sink enablements owned by a Project.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Project identifier (UUIDv7). Bound on `/v1/projects/{id}` for the tenancy CRUD surface, on `/v1/projects/{id}/credentials` for the operator-facing OpenBao Credential Broker inventory list, on `/v1/projects/{id}/credential-assignments` and `/v1/projects/{id}/cloud-assignments` for the assignment request/list surfaces, on `/v1/projects/{id}/blueprints` for the project-scoped Blueprint offer list, and on `/v1/projects/{id}/sink-enablements` and `/v1/projects/{id}/telemetry-routes` for the sink-enablement and Telemetry Route surfaces. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. A value outside [1, 200] is rejected with a `400` Problem rather than silently clamped.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.ListSinkEnablements(context.Background(), id).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.ListSinkEnablements``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListSinkEnablements`: SinkEnablementPage
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.ListSinkEnablements`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface, on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list, on &#x60;/v1/projects/{id}/credential-assignments&#x60; and &#x60;/v1/projects/{id}/cloud-assignments&#x60; for the assignment request/list surfaces, on &#x60;/v1/projects/{id}/blueprints&#x60; for the project-scoped Blueprint offer list, and on &#x60;/v1/projects/{id}/sink-enablements&#x60; and &#x60;/v1/projects/{id}/telemetry-routes&#x60; for the sink-enablement and Telemetry Route surfaces.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListSinkEnablementsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. A value outside [1, 200] is rejected with a &#x60;400&#x60; Problem rather than silently clamped.  | [default to 50]

### Return type

[**SinkEnablementPage**](SinkEnablementPage.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListTelemetryRoutes

> TelemetryRouteList ListTelemetryRoutes(ctx, id).Execute()

List the Telemetry Routes a Project holds.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Project identifier (UUIDv7). Bound on `/v1/projects/{id}` for the tenancy CRUD surface, on `/v1/projects/{id}/credentials` for the operator-facing OpenBao Credential Broker inventory list, on `/v1/projects/{id}/credential-assignments` and `/v1/projects/{id}/cloud-assignments` for the assignment request/list surfaces, on `/v1/projects/{id}/blueprints` for the project-scoped Blueprint offer list, and on `/v1/projects/{id}/sink-enablements` and `/v1/projects/{id}/telemetry-routes` for the sink-enablement and Telemetry Route surfaces. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.ListTelemetryRoutes(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.ListTelemetryRoutes``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListTelemetryRoutes`: TelemetryRouteList
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.ListTelemetryRoutes`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface, on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list, on &#x60;/v1/projects/{id}/credential-assignments&#x60; and &#x60;/v1/projects/{id}/cloud-assignments&#x60; for the assignment request/list surfaces, on &#x60;/v1/projects/{id}/blueprints&#x60; for the project-scoped Blueprint offer list, and on &#x60;/v1/projects/{id}/sink-enablements&#x60; and &#x60;/v1/projects/{id}/telemetry-routes&#x60; for the sink-enablement and Telemetry Route surfaces.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListTelemetryRoutesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**TelemetryRouteList**](TelemetryRouteList.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RequestSinkEnablement

> SinkEnablement RequestSinkEnablement(ctx, id).SinkEnablementRequestBody(sinkEnablementRequestBody).Execute()

Request a sink enablement for a Project.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Project identifier (UUIDv7). Bound on `/v1/projects/{id}` for the tenancy CRUD surface, on `/v1/projects/{id}/credentials` for the operator-facing OpenBao Credential Broker inventory list, on `/v1/projects/{id}/credential-assignments` and `/v1/projects/{id}/cloud-assignments` for the assignment request/list surfaces, on `/v1/projects/{id}/blueprints` for the project-scoped Blueprint offer list, and on `/v1/projects/{id}/sink-enablements` and `/v1/projects/{id}/telemetry-routes` for the sink-enablement and Telemetry Route surfaces. 
	sinkEnablementRequestBody := *openapiclient.NewSinkEnablementRequestBody("SinkId_example") // SinkEnablementRequestBody | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.RequestSinkEnablement(context.Background(), id).SinkEnablementRequestBody(sinkEnablementRequestBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.RequestSinkEnablement``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RequestSinkEnablement`: SinkEnablement
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.RequestSinkEnablement`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface, on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list, on &#x60;/v1/projects/{id}/credential-assignments&#x60; and &#x60;/v1/projects/{id}/cloud-assignments&#x60; for the assignment request/list surfaces, on &#x60;/v1/projects/{id}/blueprints&#x60; for the project-scoped Blueprint offer list, and on &#x60;/v1/projects/{id}/sink-enablements&#x60; and &#x60;/v1/projects/{id}/telemetry-routes&#x60; for the sink-enablement and Telemetry Route surfaces.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRequestSinkEnablementRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **sinkEnablementRequestBody** | [**SinkEnablementRequestBody**](SinkEnablementRequestBody.md) |  | 

### Return type

[**SinkEnablement**](SinkEnablement.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RevokeSinkEnablement

> SinkEnablement RevokeSinkEnablement(ctx, id).SinkEnablementRevokeBody(sinkEnablementRevokeBody).Execute()

Revoke a sink enablement.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Sink enablement identifier (UUIDv7). Bound on `/v1/sink-enablements/{id}/revoke` for the grant withdrawal. 
	sinkEnablementRevokeBody := *openapiclient.NewSinkEnablementRevokeBody("Reason_example") // SinkEnablementRevokeBody | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.RevokeSinkEnablement(context.Background(), id).SinkEnablementRevokeBody(sinkEnablementRevokeBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.RevokeSinkEnablement``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RevokeSinkEnablement`: SinkEnablement
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.RevokeSinkEnablement`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Sink enablement identifier (UUIDv7). Bound on &#x60;/v1/sink-enablements/{id}/revoke&#x60; for the grant withdrawal.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRevokeSinkEnablementRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **sinkEnablementRevokeBody** | [**SinkEnablementRevokeBody**](SinkEnablementRevokeBody.md) |  | 

### Return type

[**SinkEnablement**](SinkEnablement.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateSink

> Sink UpdateSink(ctx, id).SinkUpdateRequest(sinkUpdateRequest).Execute()

Replace a tenant sink's mutable state.



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
    "time"
	openapiclient "github.com/plexsphere/plexsphere-sdk-go"
)

func main() {
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Sink identifier (UUIDv7). Bound on `/v1/sinks/{id}` for the single-sink read, replace, and delete, and on `/v1/sinks/{id}/sink-enablements` for the owner-push grant. 
	sinkUpdateRequest := *openapiclient.NewSinkUpdateRequest(time.Now(), "Slug_example", "DisplayName_example", openapiclient.TenantSinkType("otlp"), "Endpoint_example") // SinkUpdateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.UpdateSink(context.Background(), id).SinkUpdateRequest(sinkUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.UpdateSink``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateSink`: Sink
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.UpdateSink`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Sink identifier (UUIDv7). Bound on &#x60;/v1/sinks/{id}&#x60; for the single-sink read, replace, and delete, and on &#x60;/v1/sinks/{id}/sink-enablements&#x60; for the owner-push grant.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateSinkRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **sinkUpdateRequest** | [**SinkUpdateRequest**](SinkUpdateRequest.md) |  | 

### Return type

[**Sink**](Sink.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateTelemetryRoute

> TelemetryRoute UpdateTelemetryRoute(ctx, id).TelemetryRouteRequest(telemetryRouteRequest).Execute()

Replace a Telemetry Route's state.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Telemetry Route identifier (UUIDv7). Bound on `/v1/telemetry-routes/{id}` for the single-route read, replace, and delete. 
	telemetryRouteRequest := *openapiclient.NewTelemetryRouteRequest(openapiclient.TelemetrySignal("metrics"), []string{"SinkIds_example"}) // TelemetryRouteRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.SinksAPI.UpdateTelemetryRoute(context.Background(), id).TelemetryRouteRequest(telemetryRouteRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `SinksAPI.UpdateTelemetryRoute``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateTelemetryRoute`: TelemetryRoute
	fmt.Fprintf(os.Stdout, "Response from `SinksAPI.UpdateTelemetryRoute`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Telemetry Route identifier (UUIDv7). Bound on &#x60;/v1/telemetry-routes/{id}&#x60; for the single-route read, replace, and delete.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateTelemetryRouteRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **telemetryRouteRequest** | [**TelemetryRouteRequest**](TelemetryRouteRequest.md) |  | 

### Return type

[**TelemetryRoute**](TelemetryRoute.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

