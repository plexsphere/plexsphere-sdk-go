# \AdminAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DeleteAdminGroupByID**](AdminAPI.md#DeleteAdminGroupByID) | **Delete** /v1/admin/groups/{id} | Delete a Group.
[**DeleteAdminGroupMember**](AdminAPI.md#DeleteAdminGroupMember) | **Delete** /v1/admin/groups/{id}/members/{principal_id} | Remove a principal from a Group.
[**DeleteAdminIdPByID**](AdminAPI.md#DeleteAdminIdPByID) | **Delete** /v1/admin/idp/{id} | Delete an IdP binding.
[**DeleteAdminTokenByID**](AdminAPI.md#DeleteAdminTokenByID) | **Delete** /v1/admin/tokens/{id} | Revoke any API token (admin).
[**GetAdminGroupByID**](AdminAPI.md#GetAdminGroupByID) | **Get** /v1/admin/groups/{id} | Fetch a Group by identifier.
[**GetAdminGroupList**](AdminAPI.md#GetAdminGroupList) | **Get** /v1/admin/groups | List Groups within a Domain.
[**GetAdminGroupMembers**](AdminAPI.md#GetAdminGroupMembers) | **Get** /v1/admin/groups/{id}/members | List members of a Group.
[**GetAdminIdPByID**](AdminAPI.md#GetAdminIdPByID) | **Get** /v1/admin/idp/{id} | Read an IdP binding by identifier.
[**GetAdminIdPList**](AdminAPI.md#GetAdminIdPList) | **Get** /v1/admin/idp | List IdP bindings (optionally filtered by Domain).
[**GetAdminPlatformIdPList**](AdminAPI.md#GetAdminPlatformIdPList) | **Get** /v1/admin/platform-idp | List platform-scoped (shared) IdP bindings.
[**GetAdminTokens**](AdminAPI.md#GetAdminTokens) | **Get** /v1/admin/tokens | List API tokens for any owner (admin).
[**PatchAdminGroup**](AdminAPI.md#PatchAdminGroup) | **Patch** /v1/admin/groups/{id} | Update mutable fields on a Group.
[**PatchAdminIdP**](AdminAPI.md#PatchAdminIdP) | **Patch** /v1/admin/idp/{id} | Partially update an IdP binding.
[**PatchAdminIdPStatus**](AdminAPI.md#PatchAdminIdPStatus) | **Patch** /v1/admin/idp/{id}/status | Activate or deactivate an IdP binding.
[**PostAdminGroup**](AdminAPI.md#PostAdminGroup) | **Post** /v1/admin/groups | Create a Group within a Domain.
[**PostAdminGroupMember**](AdminAPI.md#PostAdminGroupMember) | **Post** /v1/admin/groups/{id}/members | Add a principal to a Group.
[**PostAdminIdP**](AdminAPI.md#PostAdminIdP) | **Post** /v1/admin/idp | Create an IdP binding for a Domain.
[**PostAdminPlatformIdP**](AdminAPI.md#PostAdminPlatformIdP) | **Post** /v1/admin/platform-idp | Create a platform-scoped (shared) IdP binding.
[**PostAdminTokenRotate**](AdminAPI.md#PostAdminTokenRotate) | **Post** /v1/admin/tokens/{id}/rotate | Rotate any API token (admin).
[**PostAdminTokens**](AdminAPI.md#PostAdminTokens) | **Post** /v1/admin/tokens | Issue an API token on behalf of any principal (admin).



## DeleteAdminGroupByID

> DeleteAdminGroupByID(ctx, id).Execute()

Delete a Group.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Group identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AdminAPI.DeleteAdminGroupByID(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.DeleteAdminGroupByID``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Group identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteAdminGroupByIDRequest struct via the builder pattern


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


## DeleteAdminGroupMember

> DeleteAdminGroupMember(ctx, id, principalId).Kind(kind).Execute()

Remove a principal from a Group.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Group identifier (UUIDv7).
	principalId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Principal identifier (UUIDv7).
	kind := openapiclient.DeleteAdminGroupMember_kind_parameter("user") // DeleteAdminGroupMemberKindParameter | Principal discriminator. DECISION: `kind` is REQUIRED because the underlying `group_memberships` table uses XOR columns (`principal_user_id` / `principal_service_identity_id` / `principal_group_id`) and the repo needs the discriminator to target the correct column — there is no `principal_id`-only index. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AdminAPI.DeleteAdminGroupMember(context.Background(), id, principalId).Kind(kind).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.DeleteAdminGroupMember``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Group identifier (UUIDv7). | 
**principalId** | **string** | Principal identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteAdminGroupMemberRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **kind** | [**DeleteAdminGroupMemberKindParameter**](DeleteAdminGroupMemberKindParameter.md) | Principal discriminator. DECISION: &#x60;kind&#x60; is REQUIRED because the underlying &#x60;group_memberships&#x60; table uses XOR columns (&#x60;principal_user_id&#x60; / &#x60;principal_service_identity_id&#x60; / &#x60;principal_group_id&#x60;) and the repo needs the discriminator to target the correct column — there is no &#x60;principal_id&#x60;-only index.  | 

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


## DeleteAdminIdPByID

> DeleteAdminIdPByID(ctx, id).Execute()

Delete an IdP binding.

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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Binding identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AdminAPI.DeleteAdminIdPByID(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.DeleteAdminIdPByID``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Binding identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteAdminIdPByIDRequest struct via the builder pattern


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


## DeleteAdminTokenByID

> DeleteAdminTokenByID(ctx, id).Execute()

Revoke any API token (admin).



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
	r, err := apiClient.AdminAPI.DeleteAdminTokenByID(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.DeleteAdminTokenByID``: %v\n", err)
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

Other parameters are passed through a pointer to a apiDeleteAdminTokenByIDRequest struct via the builder pattern


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


## GetAdminGroupByID

> GroupResponse GetAdminGroupByID(ctx, id).Execute()

Fetch a Group by identifier.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Group identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.GetAdminGroupByID(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.GetAdminGroupByID``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAdminGroupByID`: GroupResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.GetAdminGroupByID`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Group identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetAdminGroupByIDRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**GroupResponse**](GroupResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminGroupList

> GroupListResponse GetAdminGroupList(ctx).DomainId(domainId).Cursor(cursor).Limit(limit).Execute()

List Groups within a Domain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain. DECISION: `domain_id` is REQUIRED here (unlike the IdP list endpoint where it is optional) because Group slugs are scoped per-Domain and listing across domains would require cross-domain cursor merging that the repo layer does not support and is not needed by the admin UI. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page .  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.GetAdminGroupList(context.Background()).DomainId(domainId).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.GetAdminGroupList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAdminGroupList`: GroupListResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.GetAdminGroupList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetAdminGroupListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainId** | **string** | Owning Domain. DECISION: &#x60;domain_id&#x60; is REQUIRED here (unlike the IdP list endpoint where it is optional) because Group slugs are scoped per-Domain and listing across domains would require cross-domain cursor merging that the repo layer does not support and is not needed by the admin UI.  | 
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page .  | [default to 50]

### Return type

[**GroupListResponse**](GroupListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminGroupMembers

> GroupMembershipListResponse GetAdminGroupMembers(ctx, id).Execute()

List members of a Group.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Group identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.GetAdminGroupMembers(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.GetAdminGroupMembers``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAdminGroupMembers`: GroupMembershipListResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.GetAdminGroupMembers`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Group identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetAdminGroupMembersRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**GroupMembershipListResponse**](GroupMembershipListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminIdPByID

> IdPBindingResponse GetAdminIdPByID(ctx, id).Execute()

Read an IdP binding by identifier.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Binding identifier (UUIDv7).

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.GetAdminIdPByID(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.GetAdminIdPByID``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAdminIdPByID`: IdPBindingResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.GetAdminIdPByID`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Binding identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetAdminIdPByIDRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**IdPBindingResponse**](IdPBindingResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminIdPList

> []IdPBindingResponse GetAdminIdPList(ctx).DomainId(domainId).Execute()

List IdP bindings (optionally filtered by Domain).

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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional Domain filter. (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.GetAdminIdPList(context.Background()).DomainId(domainId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.GetAdminIdPList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAdminIdPList`: []IdPBindingResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.GetAdminIdPList`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetAdminIdPListRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainId** | **string** | Optional Domain filter. | 

### Return type

[**[]IdPBindingResponse**](IdPBindingResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminPlatformIdPList

> []IdPBindingResponse GetAdminPlatformIdPList(ctx).Execute()

List platform-scoped (shared) IdP bindings.



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
	resp, r, err := apiClient.AdminAPI.GetAdminPlatformIdPList(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.GetAdminPlatformIdPList``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAdminPlatformIdPList`: []IdPBindingResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.GetAdminPlatformIdPList`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiGetAdminPlatformIdPListRequest struct via the builder pattern


### Return type

[**[]IdPBindingResponse**](IdPBindingResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAdminTokens

> []APITokenSummary GetAdminTokens(ctx).IdentityRef(identityRef).Execute()

List API tokens for any owner (admin).



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
	identityRef := "identityRef_example" // string | Owner reference in the canonical `user:<uuid>` or `service:<uuid>` form mirroring `APITokenIssueRequest`. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.GetAdminTokens(context.Background()).IdentityRef(identityRef).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.GetAdminTokens``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAdminTokens`: []APITokenSummary
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.GetAdminTokens`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetAdminTokensRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **identityRef** | **string** | Owner reference in the canonical &#x60;user:&lt;uuid&gt;&#x60; or &#x60;service:&lt;uuid&gt;&#x60; form mirroring &#x60;APITokenIssueRequest&#x60;.  | 

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


## PatchAdminGroup

> GroupResponse PatchAdminGroup(ctx, id).GroupUpdateRequest(groupUpdateRequest).Execute()

Update mutable fields on a Group.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Group identifier (UUIDv7).
	groupUpdateRequest := *openapiclient.NewGroupUpdateRequest("DisplayName_example") // GroupUpdateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.PatchAdminGroup(context.Background(), id).GroupUpdateRequest(groupUpdateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.PatchAdminGroup``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PatchAdminGroup`: GroupResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.PatchAdminGroup`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Group identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiPatchAdminGroupRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **groupUpdateRequest** | [**GroupUpdateRequest**](GroupUpdateRequest.md) |  | 

### Return type

[**GroupResponse**](GroupResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PatchAdminIdP

> IdPBindingResponse PatchAdminIdP(ctx, id).IdPBindingPatchRequest(idPBindingPatchRequest).Execute()

Partially update an IdP binding.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Binding identifier (UUIDv7).
	idPBindingPatchRequest := *openapiclient.NewIdPBindingPatchRequest() // IdPBindingPatchRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.PatchAdminIdP(context.Background(), id).IdPBindingPatchRequest(idPBindingPatchRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.PatchAdminIdP``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PatchAdminIdP`: IdPBindingResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.PatchAdminIdP`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Binding identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiPatchAdminIdPRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **idPBindingPatchRequest** | [**IdPBindingPatchRequest**](IdPBindingPatchRequest.md) |  | 

### Return type

[**IdPBindingResponse**](IdPBindingResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PatchAdminIdPStatus

> IdPBindingResponse PatchAdminIdPStatus(ctx, id).IdPBindingStatusRequest(idPBindingStatusRequest).Execute()

Activate or deactivate an IdP binding.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Binding identifier (UUIDv7).
	idPBindingStatusRequest := *openapiclient.NewIdPBindingStatusRequest(openapiclient.IdPBindingStatusRequest_status("active")) // IdPBindingStatusRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.PatchAdminIdPStatus(context.Background(), id).IdPBindingStatusRequest(idPBindingStatusRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.PatchAdminIdPStatus``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PatchAdminIdPStatus`: IdPBindingResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.PatchAdminIdPStatus`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Binding identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiPatchAdminIdPStatusRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **idPBindingStatusRequest** | [**IdPBindingStatusRequest**](IdPBindingStatusRequest.md) |  | 

### Return type

[**IdPBindingResponse**](IdPBindingResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAdminGroup

> GroupResponse PostAdminGroup(ctx).GroupRequest(groupRequest).Execute()

Create a Group within a Domain.



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
	groupRequest := *openapiclient.NewGroupRequest("DomainId_example", "Slug_example", "DisplayName_example", openapiclient.GroupRequest_source("manual")) // GroupRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.PostAdminGroup(context.Background()).GroupRequest(groupRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.PostAdminGroup``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAdminGroup`: GroupResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.PostAdminGroup`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAdminGroupRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **groupRequest** | [**GroupRequest**](GroupRequest.md) |  | 

### Return type

[**GroupResponse**](GroupResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAdminGroupMember

> GroupMembershipResponse PostAdminGroupMember(ctx, id).GroupMembershipRequest(groupMembershipRequest).Execute()

Add a principal to a Group.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Group identifier (UUIDv7).
	groupMembershipRequest := *openapiclient.NewGroupMembershipRequest("PrincipalId_example", openapiclient.GroupMembershipRequest_principal_kind("user"), openapiclient.GroupMembershipRequest_source("manual")) // GroupMembershipRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.PostAdminGroupMember(context.Background(), id).GroupMembershipRequest(groupMembershipRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.PostAdminGroupMember``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAdminGroupMember`: GroupMembershipResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.PostAdminGroupMember`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Group identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostAdminGroupMemberRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **groupMembershipRequest** | [**GroupMembershipRequest**](GroupMembershipRequest.md) |  | 

### Return type

[**GroupMembershipResponse**](GroupMembershipResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAdminIdP

> IdPBindingResponse PostAdminIdP(ctx).IdPBindingRequest(idPBindingRequest).Execute()

Create an IdP binding for a Domain.



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
	idPBindingRequest := *openapiclient.NewIdPBindingRequest("DomainId_example", "Issuer_example", "ClientId_example", "ClientSecretRef_example", "DiscoveryUrl_example", openapiclient.IdPBindingRequest_jit_policy("allow")) // IdPBindingRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.PostAdminIdP(context.Background()).IdPBindingRequest(idPBindingRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.PostAdminIdP``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAdminIdP`: IdPBindingResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.PostAdminIdP`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAdminIdPRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **idPBindingRequest** | [**IdPBindingRequest**](IdPBindingRequest.md) |  | 

### Return type

[**IdPBindingResponse**](IdPBindingResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAdminPlatformIdP

> IdPBindingResponse PostAdminPlatformIdP(ctx).PlatformIdPBindingRequest(platformIdPBindingRequest).Execute()

Create a platform-scoped (shared) IdP binding.



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
	platformIdPBindingRequest := *openapiclient.NewPlatformIdPBindingRequest("Issuer_example", "ClientId_example", "ClientSecretRef_example", "DiscoveryUrl_example", "JitPolicy_example") // PlatformIdPBindingRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AdminAPI.PostAdminPlatformIdP(context.Background()).PlatformIdPBindingRequest(platformIdPBindingRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.PostAdminPlatformIdP``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAdminPlatformIdP`: IdPBindingResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.PostAdminPlatformIdP`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAdminPlatformIdPRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platformIdPBindingRequest** | [**PlatformIdPBindingRequest**](PlatformIdPBindingRequest.md) |  | 

### Return type

[**IdPBindingResponse**](IdPBindingResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostAdminTokenRotate

> APITokenRotateResponse PostAdminTokenRotate(ctx, id).Execute()

Rotate any API token (admin).



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
	resp, r, err := apiClient.AdminAPI.PostAdminTokenRotate(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.PostAdminTokenRotate``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAdminTokenRotate`: APITokenRotateResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.PostAdminTokenRotate`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Token identifier (UUIDv7). | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostAdminTokenRotateRequest struct via the builder pattern


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


## PostAdminTokens

> APITokenIssueResponse PostAdminTokens(ctx).APITokenIssueRequest(aPITokenIssueRequest).Execute()

Issue an API token on behalf of any principal (admin).



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
	resp, r, err := apiClient.AdminAPI.PostAdminTokens(context.Background()).APITokenIssueRequest(aPITokenIssueRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AdminAPI.PostAdminTokens``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostAdminTokens`: APITokenIssueResponse
	fmt.Fprintf(os.Stdout, "Response from `AdminAPI.PostAdminTokens`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostAdminTokensRequest struct via the builder pattern


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

