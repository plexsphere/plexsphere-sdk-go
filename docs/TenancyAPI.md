# \TenancyAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateDomain**](TenancyAPI.md#CreateDomain) | **Post** /v1/domains | Create a tenancy Domain.
[**CreateInvitation**](TenancyAPI.md#CreateInvitation) | **Post** /v1/domains/{id}/invitations | Stage a pending Invitation on a Domain.
[**CreateProject**](TenancyAPI.md#CreateProject) | **Post** /v1/projects | Create a tenancy Project.
[**DeleteDomain**](TenancyAPI.md#DeleteDomain) | **Delete** /v1/domains/{id} | Delete a Domain.
[**DeleteProject**](TenancyAPI.md#DeleteProject) | **Delete** /v1/projects/{id} | Delete a Project.
[**GetDomain**](TenancyAPI.md#GetDomain) | **Get** /v1/domains/{id} | Fetch a Domain by identifier.
[**GetIdentity**](TenancyAPI.md#GetIdentity) | **Get** /v1/domains/{id}/identities/{principalId} | Fetch a single Domain principal by identifier.
[**GetInvitation**](TenancyAPI.md#GetInvitation) | **Get** /v1/domains/{id}/invitations/{invitationId} | Fetch a single Invitation by identifier.
[**GetProject**](TenancyAPI.md#GetProject) | **Get** /v1/projects/{id} | Fetch a Project by identifier.
[**ListDomains**](TenancyAPI.md#ListDomains) | **Get** /v1/domains | List tenancy Domains.
[**ListIdentities**](TenancyAPI.md#ListIdentities) | **Get** /v1/domains/{id}/identities | List principals (users + service identities) on a Domain.
[**ListInvitations**](TenancyAPI.md#ListInvitations) | **Get** /v1/domains/{id}/invitations | List Invitations on a Domain.
[**ListProjects**](TenancyAPI.md#ListProjects) | **Get** /v1/projects | List tenancy Projects.
[**PatchDomain**](TenancyAPI.md#PatchDomain) | **Patch** /v1/domains/{id} | Patch mutable fields on a Domain.
[**PatchProject**](TenancyAPI.md#PatchProject) | **Patch** /v1/projects/{id} | Patch mutable fields on a Project.
[**RevokeInvitation**](TenancyAPI.md#RevokeInvitation) | **Delete** /v1/domains/{id}/invitations/{invitationId} | Revoke a pending Invitation.



## CreateDomain

> DomainResponse CreateDomain(ctx).DomainCreateRequest(domainCreateRequest).Execute()

Create a tenancy Domain.



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
	domainCreateRequest := *openapiclient.NewDomainCreateRequest("Name_example", "Slug_example", "10.42.0.0/16") // DomainCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.CreateDomain(context.Background()).DomainCreateRequest(domainCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.CreateDomain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateDomain`: DomainResponse
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.CreateDomain`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateDomainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **domainCreateRequest** | [**DomainCreateRequest**](DomainCreateRequest.md) |  | 

### Return type

[**DomainResponse**](DomainResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateInvitation

> InvitationResponse CreateInvitation(ctx, id).InvitationCreateRequest(invitationCreateRequest).Execute()

Stage a pending Invitation on a Domain.



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
	invitationCreateRequest := *openapiclient.NewInvitationCreateRequest("ExternalSubject_example") // InvitationCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.CreateInvitation(context.Background(), id).InvitationCreateRequest(invitationCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.CreateInvitation``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateInvitation`: InvitationResponse
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.CreateInvitation`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateInvitationRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **invitationCreateRequest** | [**InvitationCreateRequest**](InvitationCreateRequest.md) |  | 

### Return type

[**InvitationResponse**](InvitationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateProject

> ProjectResponse CreateProject(ctx).ProjectCreateRequest(projectCreateRequest).Execute()

Create a tenancy Project.



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
	projectCreateRequest := *openapiclient.NewProjectCreateRequest("DomainId_example", "Name_example", "Slug_example") // ProjectCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.CreateProject(context.Background()).ProjectCreateRequest(projectCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.CreateProject``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateProject`: ProjectResponse
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.CreateProject`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateProjectRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **projectCreateRequest** | [**ProjectCreateRequest**](ProjectCreateRequest.md) |  | 

### Return type

[**ProjectResponse**](ProjectResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteDomain

> DeleteDomain(ctx, id).Execute()

Delete a Domain.



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
	r, err := apiClient.TenancyAPI.DeleteDomain(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.DeleteDomain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteDomainRequest struct via the builder pattern


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


## DeleteProject

> DeleteProject(ctx, id).Execute()

Delete a Project.



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

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.TenancyAPI.DeleteProject(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.DeleteProject``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface and on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteProjectRequest struct via the builder pattern


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


## GetDomain

> DomainResponse GetDomain(ctx, id).Execute()

Fetch a Domain by identifier.



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
	resp, r, err := apiClient.TenancyAPI.GetDomain(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.GetDomain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDomain`: DomainResponse
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.GetDomain`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDomainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**DomainResponse**](DomainResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetIdentity

> IdentityDetail GetIdentity(ctx, id, principalId).Execute()

Fetch a single Domain principal by identifier.



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
	principalId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Principal identifier (UUIDv7). Bound on `/v1/domains/{id}/identities/{principalId}` for the per-Domain identity-read surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.GetIdentity(context.Background(), id, principalId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.GetIdentity``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetIdentity`: IdentityDetail
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.GetIdentity`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 
**principalId** | **string** | Principal identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}/identities/{principalId}&#x60; for the per-Domain identity-read surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetIdentityRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**IdentityDetail**](IdentityDetail.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetInvitation

> InvitationResponse GetInvitation(ctx, id, invitationId).Execute()

Fetch a single Invitation by identifier.



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
	invitationId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Invitation identifier (UUIDv7). Bound on `/v1/domains/{id}/invitations/{invitationId}` for the per- Domain invitation read / revoke surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.GetInvitation(context.Background(), id, invitationId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.GetInvitation``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetInvitation`: InvitationResponse
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.GetInvitation`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 
**invitationId** | **string** | Invitation identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}/invitations/{invitationId}&#x60; for the per- Domain invitation read / revoke surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetInvitationRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**InvitationResponse**](InvitationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetProject

> ProjectResponse GetProject(ctx, id).Execute()

Fetch a Project by identifier.



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

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.GetProject(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.GetProject``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetProject`: ProjectResponse
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.GetProject`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface and on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetProjectRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**ProjectResponse**](ProjectResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListDomains

> DomainList ListDomains(ctx).Cursor(cursor).Limit(limit).Execute()

List tenancy Domains.



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
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.ListDomains(context.Background()).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.ListDomains``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListDomains`: DomainList
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.ListDomains`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListDomainsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  | [default to 50]

### Return type

[**DomainList**](DomainList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListIdentities

> IdentityList ListIdentities(ctx, id).Cursor(cursor).Limit(limit).Kind(kind).Execute()

List principals (users + service identities) on a Domain.



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
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400 invalid_cursor` .  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  (optional) (default to 50)
	kind := openapiclient.IdentityKind("user") // IdentityKind | Optional principal-kind filter. Values outside the closed set surface as `400 invalid_kind`.  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.ListIdentities(context.Background(), id).Cursor(cursor).Limit(limit).Kind(kind).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.ListIdentities``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListIdentities`: IdentityList
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.ListIdentities`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListIdentitiesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400 invalid_cursor&#x60; .  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  | [default to 50]
 **kind** | [**IdentityKind**](IdentityKind.md) | Optional principal-kind filter. Values outside the closed set surface as &#x60;400 invalid_kind&#x60;.  | 

### Return type

[**IdentityList**](IdentityList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListInvitations

> InvitationList ListInvitations(ctx, id).Cursor(cursor).Limit(limit).Status(status).Execute()

List Invitations on a Domain.



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
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400 invalid_cursor` .  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  (optional) (default to 50)
	status := openapiclient.ListInvitations_status_parameter("pending") // ListInvitationsStatusParameter | Optional status filter. Values outside the closed set surface as `400 invalid_status`. Defaults to `all` .  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.ListInvitations(context.Background(), id).Cursor(cursor).Limit(limit).Status(status).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.ListInvitations``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListInvitations`: InvitationList
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.ListInvitations`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListInvitationsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400 invalid_cursor&#x60; .  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  | [default to 50]
 **status** | [**ListInvitationsStatusParameter**](ListInvitationsStatusParameter.md) | Optional status filter. Values outside the closed set surface as &#x60;400 invalid_status&#x60;. Defaults to &#x60;all&#x60; .  | 

### Return type

[**InvitationList**](InvitationList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListProjects

> ProjectList ListProjects(ctx).Cursor(cursor).Limit(limit).DomainId(domainId).Execute()

List tenancy Projects.



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
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  (optional) (default to 50)
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional filter scoping the page to a single parent Domain. Omit to page across every Domain the caller is authorised to see.  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.ListProjects(context.Background()).Cursor(cursor).Limit(limit).DomainId(domainId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.ListProjects``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListProjects`: ProjectList
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.ListProjects`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListProjectsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  | [default to 50]
 **domainId** | **string** | Optional filter scoping the page to a single parent Domain. Omit to page across every Domain the caller is authorised to see.  | 

### Return type

[**ProjectList**](ProjectList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PatchDomain

> DomainResponse PatchDomain(ctx, id).DomainPatchRequest(domainPatchRequest).Execute()

Patch mutable fields on a Domain.



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
	domainPatchRequest := *openapiclient.NewDomainPatchRequest() // DomainPatchRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.PatchDomain(context.Background(), id).DomainPatchRequest(domainPatchRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.PatchDomain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PatchDomain`: DomainResponse
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.PatchDomain`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiPatchDomainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **domainPatchRequest** | [**DomainPatchRequest**](DomainPatchRequest.md) |  | 

### Return type

[**DomainResponse**](DomainResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PatchProject

> ProjectResponse PatchProject(ctx, id).ProjectPatchRequest(projectPatchRequest).Execute()

Patch mutable fields on a Project.



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
	projectPatchRequest := *openapiclient.NewProjectPatchRequest() // ProjectPatchRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.TenancyAPI.PatchProject(context.Background(), id).ProjectPatchRequest(projectPatchRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.PatchProject``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PatchProject`: ProjectResponse
	fmt.Fprintf(os.Stdout, "Response from `TenancyAPI.PatchProject`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface and on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiPatchProjectRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **projectPatchRequest** | [**ProjectPatchRequest**](ProjectPatchRequest.md) |  | 

### Return type

[**ProjectResponse**](ProjectResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RevokeInvitation

> RevokeInvitation(ctx, id, invitationId).Execute()

Revoke a pending Invitation.



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
	invitationId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Invitation identifier (UUIDv7). Bound on `/v1/domains/{id}/invitations/{invitationId}` for the per- Domain invitation read / revoke surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.TenancyAPI.RevokeInvitation(context.Background(), id, invitationId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `TenancyAPI.RevokeInvitation``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Domain identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}&#x60; for the tenancy CRUD surface.  | 
**invitationId** | **string** | Invitation identifier (UUIDv7). Bound on &#x60;/v1/domains/{id}/invitations/{invitationId}&#x60; for the per- Domain invitation read / revoke surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRevokeInvitationRequest struct via the builder pattern


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

