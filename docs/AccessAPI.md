# \AccessAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AttachSession**](AccessAPI.md#AttachSession) | **Get** /v1/projects/{project_id}/sessions/{session_id}/attach | Attach to a live SSH session as a bidirectional WebSocket stream.
[**GetSession**](AccessAPI.md#GetSession) | **Get** /v1/projects/{project_id}/sessions/{session_id} | Inspect a single mediated session.
[**IssueSession**](AccessAPI.md#IssueSession) | **Post** /v1/projects/{project_id}/sessions | Issue a short-lived, session-scoped JWT for a mediated target.
[**ListSessions**](AccessAPI.md#ListSessions) | **Get** /v1/projects/{project_id}/sessions | List mediated sessions for a Project.
[**PostNodeSessionCallback**](AccessAPI.md#PostNodeSessionCallback) | **Post** /v1/nodes/{id}/sessions/{session_id} | Report per-kind session activity from a Node.
[**RevokeSession**](AccessAPI.md#RevokeSession) | **Post** /v1/projects/{project_id}/sessions/{session_id}:revoke | Instantly revoke a live mediated session.



## AttachSession

> AttachSession(ctx, projectId, sessionId).Execute()

Attach to a live SSH session as a bidirectional WebSocket stream.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The Access Orchestrator issue, list, read, and revoke operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path. 
	sessionId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Session identifier (UUIDv7). Bound on `/v1/projects/{project_id}/sessions/{session_id}`, its `:revoke` sub-resource, and its `/attach` WebSocket gateway for the single-Session read, revoke, and attach. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AccessAPI.AttachSession(context.Background(), projectId, sessionId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AccessAPI.AttachSession``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The Access Orchestrator issue, list, read, and revoke operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path.  | 
**sessionId** | **string** | Session identifier (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/sessions/{session_id}&#x60;, its &#x60;:revoke&#x60; sub-resource, and its &#x60;/attach&#x60; WebSocket gateway for the single-Session read, revoke, and attach.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiAttachSessionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

 (empty response body)

### Authorization

[operatorBearer](../README.md#operatorBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetSession

> Session GetSession(ctx, projectId, sessionId).Execute()

Inspect a single mediated session.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The Access Orchestrator issue, list, read, and revoke operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path. 
	sessionId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Session identifier (UUIDv7). Bound on `/v1/projects/{project_id}/sessions/{session_id}`, its `:revoke` sub-resource, and its `/attach` WebSocket gateway for the single-Session read, revoke, and attach. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AccessAPI.GetSession(context.Background(), projectId, sessionId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AccessAPI.GetSession``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetSession`: Session
	fmt.Fprintf(os.Stdout, "Response from `AccessAPI.GetSession`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The Access Orchestrator issue, list, read, and revoke operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path.  | 
**sessionId** | **string** | Session identifier (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/sessions/{session_id}&#x60;, its &#x60;:revoke&#x60; sub-resource, and its &#x60;/attach&#x60; WebSocket gateway for the single-Session read, revoke, and attach.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetSessionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**Session**](Session.md)

### Authorization

[operatorBearer](../README.md#operatorBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## IssueSession

> IssuedSession IssueSession(ctx, projectId).IssueSessionRequest(issueSessionRequest).Execute()

Issue a short-lived, session-scoped JWT for a mediated target.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The Access Orchestrator issue, list, read, and revoke operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path. 
	issueSessionRequest := *openapiclient.NewIssueSessionRequest("ResourceId_example", openapiclient.SessionKind("ssh"), *openapiclient.NewSessionTarget()) // IssueSessionRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AccessAPI.IssueSession(context.Background(), projectId).IssueSessionRequest(issueSessionRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AccessAPI.IssueSession``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `IssueSession`: IssuedSession
	fmt.Fprintf(os.Stdout, "Response from `AccessAPI.IssueSession`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The Access Orchestrator issue, list, read, and revoke operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiIssueSessionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **issueSessionRequest** | [**IssueSessionRequest**](IssueSessionRequest.md) |  | 

### Return type

[**IssuedSession**](IssuedSession.md)

### Authorization

[operatorBearer](../README.md#operatorBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListSessions

> SessionList ListSessions(ctx, projectId).Status(status).Kind(kind).IdentityId(identityId).Cursor(cursor).Limit(limit).Execute()

List mediated sessions for a Project.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The Access Orchestrator issue, list, read, and revoke operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path. 
	status := openapiclient.SessionStatus("active") // SessionStatus | Optional aggregate-status filter. When present, only Sessions whose status equals the named value are returned.  (optional)
	kind := openapiclient.SessionKind("ssh") // SessionKind | Optional kind filter. When present, only Sessions of the named kind are returned.  (optional)
	identityId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional identity filter. When present, only Sessions issued to the named Identity are returned.  (optional)
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AccessAPI.ListSessions(context.Background(), projectId).Status(status).Kind(kind).IdentityId(identityId).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AccessAPI.ListSessions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListSessions`: SessionList
	fmt.Fprintf(os.Stdout, "Response from `AccessAPI.ListSessions`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The Access Orchestrator issue, list, read, and revoke operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListSessionsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **status** | [**SessionStatus**](SessionStatus.md) | Optional aggregate-status filter. When present, only Sessions whose status equals the named value are returned.  | 
 **kind** | [**SessionKind**](SessionKind.md) | Optional kind filter. When present, only Sessions of the named kind are returned.  | 
 **identityId** | **string** | Optional identity filter. When present, only Sessions issued to the named Identity are returned.  | 
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**SessionList**](SessionList.md)

### Authorization

[operatorBearer](../README.md#operatorBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostNodeSessionCallback

> PostNodeSessionCallback(ctx, id, sessionId).Authorization(authorization).SessionActivityRequest(sessionActivityRequest).Execute()

Report per-kind session activity from a Node.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the callback scope.
	sessionId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Session identifier (UUIDv7) the activity belongs to.
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path `id`; a credential belonging to a different Node surfaces as 403 `nsk_node_mismatch`. 
	sessionActivityRequest := *openapiclient.NewSessionActivityRequest() // SessionActivityRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AccessAPI.PostNodeSessionCallback(context.Background(), id, sessionId).Authorization(authorization).SessionActivityRequest(sessionActivityRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AccessAPI.PostNodeSessionCallback``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the callback scope. | 
**sessionId** | **string** | Session identifier (UUIDv7) the activity belongs to. | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostNodeSessionCallbackRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path &#x60;id&#x60;; a credential belonging to a different Node surfaces as 403 &#x60;nsk_node_mismatch&#x60;.  | 
 **sessionActivityRequest** | [**SessionActivityRequest**](SessionActivityRequest.md) |  | 

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RevokeSession

> RevokeSession(ctx, projectId, sessionId).RevokeSessionRequest(revokeSessionRequest).Execute()

Instantly revoke a live mediated session.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The Access Orchestrator issue, list, read, and revoke operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path. 
	sessionId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Session identifier (UUIDv7). Bound on `/v1/projects/{project_id}/sessions/{session_id}`, its `:revoke` sub-resource, and its `/attach` WebSocket gateway for the single-Session read, revoke, and attach. 
	revokeSessionRequest := *openapiclient.NewRevokeSessionRequest(openapiclient.RevokeReason("operator_request")) // RevokeSessionRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.AccessAPI.RevokeSession(context.Background(), projectId, sessionId).RevokeSessionRequest(revokeSessionRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AccessAPI.RevokeSession``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The Access Orchestrator issue, list, read, and revoke operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path.  | 
**sessionId** | **string** | Session identifier (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/sessions/{session_id}&#x60;, its &#x60;:revoke&#x60; sub-resource, and its &#x60;/attach&#x60; WebSocket gateway for the single-Session read, revoke, and attach.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRevokeSessionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **revokeSessionRequest** | [**RevokeSessionRequest**](RevokeSessionRequest.md) |  | 

### Return type

 (empty response body)

### Authorization

[operatorBearer](../README.md#operatorBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

