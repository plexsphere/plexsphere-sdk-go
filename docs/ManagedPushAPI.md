# \ManagedPushAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DeleteManagedPush**](ManagedPushAPI.md#DeleteManagedPush) | **Delete** /v1/domains/{domain_id}/managed-push | Detach a Domain&#39;s managed-push target.
[**GetManagedHookPush**](ManagedPushAPI.md#GetManagedHookPush) | **Get** /v1/domains/{domain_id}/managed-push/hooks/{push_id} | Read a single recorded managed-hook push.
[**GetManagedPush**](ManagedPushAPI.md#GetManagedPush) | **Get** /v1/domains/{domain_id}/managed-push | Read the managed-push target configured for a Domain.
[**PushManagedHook**](ManagedPushAPI.md#PushManagedHook) | **Post** /v1/domains/{domain_id}/managed-push/hooks | Apply a PlexdHook to a Domain&#39;s managed-push cluster.
[**PutManagedPush**](ManagedPushAPI.md#PutManagedPush) | **Put** /v1/domains/{domain_id}/managed-push | Attach or replace a Domain&#39;s managed-push target.
[**RollbackManagedHookPush**](ManagedPushAPI.md#RollbackManagedHookPush) | **Post** /v1/domains/{domain_id}/managed-push/hooks/{push_id}/rollback | Roll back a recorded managed-hook push.



## DeleteManagedPush

> DeleteManagedPush(ctx, domainId).Execute()

Detach a Domain's managed-push target.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.ManagedPushAPI.DeleteManagedPush(context.Background(), domainId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagedPushAPI.DeleteManagedPush``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteManagedPushRequest struct via the builder pattern


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


## GetManagedHookPush

> ManagedHookPush GetManagedHookPush(ctx, domainId, pushId).Execute()

Read a single recorded managed-hook push.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	pushId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Recorded managed-hook push identifier (UUIDv7). Bound on `/v1/domains/{domain_id}/managed-push/hooks/{push_id}` and its `/rollback` sub-resource for the single-push read and rollback. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ManagedPushAPI.GetManagedHookPush(context.Background(), domainId, pushId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagedPushAPI.GetManagedHookPush``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetManagedHookPush`: ManagedHookPush
	fmt.Fprintf(os.Stdout, "Response from `ManagedPushAPI.GetManagedHookPush`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 
**pushId** | **string** | Recorded managed-hook push identifier (UUIDv7). Bound on &#x60;/v1/domains/{domain_id}/managed-push/hooks/{push_id}&#x60; and its &#x60;/rollback&#x60; sub-resource for the single-push read and rollback.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetManagedHookPushRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**ManagedHookPush**](ManagedHookPush.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetManagedPush

> ManagedPushTarget GetManagedPush(ctx, domainId).Execute()

Read the managed-push target configured for a Domain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ManagedPushAPI.GetManagedPush(context.Background(), domainId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagedPushAPI.GetManagedPush``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetManagedPush`: ManagedPushTarget
	fmt.Fprintf(os.Stdout, "Response from `ManagedPushAPI.GetManagedPush`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetManagedPushRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**ManagedPushTarget**](ManagedPushTarget.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PushManagedHook

> ManagedHookPush PushManagedHook(ctx, domainId).ManagedHookPushRequest(managedHookPushRequest).Execute()

Apply a PlexdHook to a Domain's managed-push cluster.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	managedHookPushRequest := *openapiclient.NewManagedHookPushRequest("Namespace_example", "Name_example", "ImageDigest_example") // ManagedHookPushRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ManagedPushAPI.PushManagedHook(context.Background(), domainId).ManagedHookPushRequest(managedHookPushRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagedPushAPI.PushManagedHook``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PushManagedHook`: ManagedHookPush
	fmt.Fprintf(os.Stdout, "Response from `ManagedPushAPI.PushManagedHook`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiPushManagedHookRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **managedHookPushRequest** | [**ManagedHookPushRequest**](ManagedHookPushRequest.md) |  | 

### Return type

[**ManagedHookPush**](ManagedHookPush.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PutManagedPush

> ManagedPushTarget PutManagedPush(ctx, domainId).ManagedPushAttachRequest(managedPushAttachRequest).Execute()

Attach or replace a Domain's managed-push target.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	managedPushAttachRequest := *openapiclient.NewManagedPushAttachRequest(string(123), false) // ManagedPushAttachRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ManagedPushAPI.PutManagedPush(context.Background(), domainId).ManagedPushAttachRequest(managedPushAttachRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagedPushAPI.PutManagedPush``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PutManagedPush`: ManagedPushTarget
	fmt.Fprintf(os.Stdout, "Response from `ManagedPushAPI.PutManagedPush`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiPutManagedPushRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **managedPushAttachRequest** | [**ManagedPushAttachRequest**](ManagedPushAttachRequest.md) |  | 

### Return type

[**ManagedPushTarget**](ManagedPushTarget.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RollbackManagedHookPush

> ManagedHookPush RollbackManagedHookPush(ctx, domainId, pushId).Execute()

Roll back a recorded managed-hook push.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	pushId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Recorded managed-hook push identifier (UUIDv7). Bound on `/v1/domains/{domain_id}/managed-push/hooks/{push_id}` and its `/rollback` sub-resource for the single-push read and rollback. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ManagedPushAPI.RollbackManagedHookPush(context.Background(), domainId, pushId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagedPushAPI.RollbackManagedHookPush``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RollbackManagedHookPush`: ManagedHookPush
	fmt.Fprintf(os.Stdout, "Response from `ManagedPushAPI.RollbackManagedHookPush`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 
**pushId** | **string** | Recorded managed-hook push identifier (UUIDv7). Bound on &#x60;/v1/domains/{domain_id}/managed-push/hooks/{push_id}&#x60; and its &#x60;/rollback&#x60; sub-resource for the single-push read and rollback.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRollbackManagedHookPushRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**ManagedHookPush**](ManagedHookPush.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

