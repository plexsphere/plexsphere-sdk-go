# \HooksAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DeleteManagedPush**](HooksAPI.md#DeleteManagedPush) | **Delete** /v1/domains/{domainId}/managed-push | Detach a Domain&#39;s managed-push target.
[**GetManagedHookPush**](HooksAPI.md#GetManagedHookPush) | **Get** /v1/domains/{domainId}/managed-push/hooks/{pushId} | Read a single recorded managed-hook push.
[**GetManagedPush**](HooksAPI.md#GetManagedPush) | **Get** /v1/domains/{domainId}/managed-push | Read the managed-push target configured for a Domain.
[**ListHooks**](HooksAPI.md#ListHooks) | **Get** /v1/hooks | List discovered hooks across Domains.
[**PushManagedHook**](HooksAPI.md#PushManagedHook) | **Post** /v1/domains/{domainId}/managed-push/hooks | Apply a PlexdHook to a Domain&#39;s managed-push cluster.
[**PutManagedPush**](HooksAPI.md#PutManagedPush) | **Put** /v1/domains/{domainId}/managed-push | Attach or replace a Domain&#39;s managed-push target.
[**RollbackManagedHookPush**](HooksAPI.md#RollbackManagedHookPush) | **Post** /v1/domains/{domainId}/managed-push/hooks/{pushId}:rollback | Roll back a recorded managed-hook push.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain's chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.HooksAPI.DeleteManagedPush(context.Background(), domainId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `HooksAPI.DeleteManagedPush``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteManagedPushRequest struct via the builder pattern


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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain's chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path. 
	pushId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Recorded managed-hook push identifier (UUIDv7). Bound on `/v1/domains/{domainId}/managed-push/hooks/{pushId}` and its `:rollback` sub-resource for the single-push read and rollback. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.HooksAPI.GetManagedHookPush(context.Background(), domainId, pushId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `HooksAPI.GetManagedHookPush``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetManagedHookPush`: ManagedHookPush
	fmt.Fprintf(os.Stdout, "Response from `HooksAPI.GetManagedHookPush`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 
**pushId** | **string** | Recorded managed-hook push identifier (UUIDv7). Bound on &#x60;/v1/domains/{domainId}/managed-push/hooks/{pushId}&#x60; and its &#x60;:rollback&#x60; sub-resource for the single-push read and rollback.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetManagedHookPushRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**ManagedHookPush**](ManagedHookPush.md)

### Authorization

No authorization required

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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain's chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.HooksAPI.GetManagedPush(context.Background(), domainId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `HooksAPI.GetManagedPush``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetManagedPush`: ManagedPushTarget
	fmt.Fprintf(os.Stdout, "Response from `HooksAPI.GetManagedPush`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetManagedPushRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**ManagedPushTarget**](ManagedPushTarget.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain's chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path. 
	managedHookPushRequest := *openapiclient.NewManagedHookPushRequest("Namespace_example", "Name_example", "ImageDigest_example") // ManagedHookPushRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.HooksAPI.PushManagedHook(context.Background(), domainId).ManagedHookPushRequest(managedHookPushRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `HooksAPI.PushManagedHook``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PushManagedHook`: ManagedHookPush
	fmt.Fprintf(os.Stdout, "Response from `HooksAPI.PushManagedHook`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiPushManagedHookRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **managedHookPushRequest** | [**ManagedHookPushRequest**](ManagedHookPushRequest.md) |  | 

### Return type

[**ManagedHookPush**](ManagedHookPush.md)

### Authorization

No authorization required

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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain's chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path. 
	managedPushAttachRequest := *openapiclient.NewManagedPushAttachRequest(string(123), false) // ManagedPushAttachRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.HooksAPI.PutManagedPush(context.Background(), domainId).ManagedPushAttachRequest(managedPushAttachRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `HooksAPI.PutManagedPush``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PutManagedPush`: ManagedPushTarget
	fmt.Fprintf(os.Stdout, "Response from `HooksAPI.PutManagedPush`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiPutManagedPushRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **managedPushAttachRequest** | [**ManagedPushAttachRequest**](ManagedPushAttachRequest.md) |  | 

### Return type

[**ManagedPushTarget**](ManagedPushTarget.md)

### Authorization

No authorization required

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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain's chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path. 
	pushId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Recorded managed-hook push identifier (UUIDv7). Bound on `/v1/domains/{domainId}/managed-push/hooks/{pushId}` and its `:rollback` sub-resource for the single-push read and rollback. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.HooksAPI.RollbackManagedHookPush(context.Background(), domainId, pushId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `HooksAPI.RollbackManagedHookPush``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RollbackManagedHookPush`: ManagedHookPush
	fmt.Fprintf(os.Stdout, "Response from `HooksAPI.RollbackManagedHookPush`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 
**pushId** | **string** | Recorded managed-hook push identifier (UUIDv7). Bound on &#x60;/v1/domains/{domainId}/managed-push/hooks/{pushId}&#x60; and its &#x60;:rollback&#x60; sub-resource for the single-push read and rollback.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRollbackManagedHookPushRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**ManagedHookPush**](ManagedHookPush.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

