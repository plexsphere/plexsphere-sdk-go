# \MeshAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DeleteNodeStateReport**](MeshAPI.md#DeleteNodeStateReport) | **Delete** /v1/nodes/{id}/state/reports/{key} | Delete an upstream node-state report entry for a Node.
[**FetchNodeSecret**](MeshAPI.md#FetchNodeSecret) | **Get** /v1/nodes/{id}/secrets/{name} | Fetch a Secret Store entry rewrapped under the calling Node&#39;s NSK.
[**GetDomainMeshTopology**](MeshAPI.md#GetDomainMeshTopology) | **Get** /v1/domains/{domainId}/mesh/topology | Return the mesh topology for a Domain.
[**GetNodeEvents**](MeshAPI.md#GetNodeEvents) | **Get** /v1/nodes/{id}/events | Stream signed envelope events for a Node over SSE.
[**GetNodeKeysRotatePreview**](MeshAPI.md#GetNodeKeysRotatePreview) | **Get** /v1/nodes/{id}/keys/rotate/preview | Preview the fleet impact of rotating a Node&#39;s mesh key.
[**GetNodeReachability**](MeshAPI.md#GetNodeReachability) | **Get** /v1/nodes/{id}/reachability | Read the reachability projection for a Node.
[**GetNodeState**](MeshAPI.md#GetNodeState) | **Get** /v1/nodes/{id}/state | Reconciliation pull for a Node — return the canonical NodeStateSnapshot.
[**PostKeysRotate**](MeshAPI.md#PostKeysRotate) | **Post** /v1/keys/rotate | Submit a freshly-generated Curve25519 key to complete a rotation.
[**PostNodeAudit**](MeshAPI.md#PostNodeAudit) | **Post** /v1/nodes/{id}/audit | Ingest a batch of normalised audit events for a Node.
[**PostNodeHeartbeat**](MeshAPI.md#PostNodeHeartbeat) | **Post** /v1/nodes/{id}/heartbeat | Record a Node liveness heartbeat and return reconcile/rotate hints.
[**PostNodeIntegrityViolations**](MeshAPI.md#PostNodeIntegrityViolations) | **Post** /v1/nodes/{id}/integrity-violations | Ingest a batch of integrity-violation reports for a Node.
[**PostNodeKeysRotate**](MeshAPI.md#PostNodeKeysRotate) | **Post** /v1/nodes/{id}/keys/rotate | Trigger a mesh-key rotation for a Node.
[**PostNodeLogs**](MeshAPI.md#PostNodeLogs) | **Post** /v1/nodes/{id}/logs | Ingest a batch of structured log lines for a Node.
[**PostNodeMetrics**](MeshAPI.md#PostNodeMetrics) | **Post** /v1/nodes/{id}/metrics | Ingest a batch of metric samples for a Node.
[**PutNodeCapabilities**](MeshAPI.md#PutNodeCapabilities) | **Put** /v1/nodes/{id}/capabilities | Record the per-Node capability manifest snapshot.
[**PutNodeEndpoint**](MeshAPI.md#PutNodeEndpoint) | **Put** /v1/nodes/{id}/endpoint | Record a NAT-observed Peer endpoint observation.
[**PutNodeStateReport**](MeshAPI.md#PutNodeStateReport) | **Put** /v1/nodes/{id}/state/reports/{key} | Record an upstream node-state report entry for a Node.



## DeleteNodeStateReport

> DeleteNodeStateReport(ctx, id, key).Authorization(authorization).Execute()

Delete an upstream node-state report entry for a Node.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the report-delete scope.
	key := "key_example" // string | Report entry key. Lower-case, starts with a letter, and is limited to letters, digits, dot, hyphen, and underscore (1 to 128 characters). 
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key. Only a Node proving possession of its NSK may delete a report; a missing, malformed, or revoked credential surfaces as 401. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.MeshAPI.DeleteNodeStateReport(context.Background(), id, key).Authorization(authorization).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.DeleteNodeStateReport``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the report-delete scope. | 
**key** | **string** | Report entry key. Lower-case, starts with a letter, and is limited to letters, digits, dot, hyphen, and underscore (1 to 128 characters).  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteNodeStateReportRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key. Only a Node proving possession of its NSK may delete a report; a missing, malformed, or revoked credential surfaces as 401.  | 

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


## FetchNodeSecret

> *os.File FetchNodeSecret(ctx, id, name).Authorization(authorization).Version(version).Execute()

Fetch a Secret Store entry rewrapped under the calling Node's NSK.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the secret-fetch scope.
	name := "name_example" // string | Secret name within the owning Project. Lower-case, starts with a letter, and is limited to letters, digits, hyphen, and underscore (1 to 63 characters). 
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. Only a Node proving possession of its NSK may fetch a secret; a missing, malformed, or revoked credential surfaces as 401. 
	version := int32(56) // int32 | Optional OpenBao KV v2 version to fetch. When omitted the current version is served. The version actually served is always reported in the `X-Plexsphere-Secret-Version` response header.  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.FetchNodeSecret(context.Background(), id, name).Authorization(authorization).Version(version).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.FetchNodeSecret``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `FetchNodeSecret`: *os.File
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.FetchNodeSecret`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the secret-fetch scope. | 
**name** | **string** | Secret name within the owning Project. Lower-case, starts with a letter, and is limited to letters, digits, hyphen, and underscore (1 to 63 characters).  | 

### Other Parameters

Other parameters are passed through a pointer to a apiFetchNodeSecretRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. Only a Node proving possession of its NSK may fetch a secret; a missing, malformed, or revoked credential surfaces as 401.  | 
 **version** | **int32** | Optional OpenBao KV v2 version to fetch. When omitted the current version is served. The version actually served is always reported in the &#x60;X-Plexsphere-Secret-Version&#x60; response header.  | 

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


## GetDomainMeshTopology

> MeshTopology GetDomainMeshTopology(ctx, domainId).Execute()

Return the mesh topology for a Domain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Domain identifier (UUIDv7) — the topology scope.

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.GetDomainMeshTopology(context.Background(), domainId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.GetDomainMeshTopology``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetDomainMeshTopology`: MeshTopology
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.GetDomainMeshTopology`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Domain identifier (UUIDv7) — the topology scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetDomainMeshTopologyRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**MeshTopology**](MeshTopology.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetNodeEvents

> string GetNodeEvents(ctx, id).LastEventID(lastEventID).Execute()

Stream signed envelope events for a Node over SSE.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the SSE stream scope.
	lastEventID := "lastEventID_example" // string | SSE replay cursor. When present and parseable as a non-negative integer, the server resumes streaming from the envelope whose JetStream sequence is strictly greater than the supplied value. When absent or empty the stream tails from now.  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.GetNodeEvents(context.Background(), id).LastEventID(lastEventID).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.GetNodeEvents``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetNodeEvents`: string
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.GetNodeEvents`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the SSE stream scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetNodeEventsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **lastEventID** | **string** | SSE replay cursor. When present and parseable as a non-negative integer, the server resumes streaming from the envelope whose JetStream sequence is strictly greater than the supplied value. When absent or empty the stream tails from now.  | 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: text/event-stream, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetNodeKeysRotatePreview

> RotationImpactPreview GetNodeKeysRotatePreview(ctx, id).Execute()

Preview the fleet impact of rotating a Node's mesh key.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the rotation scope.

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.GetNodeKeysRotatePreview(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.GetNodeKeysRotatePreview``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetNodeKeysRotatePreview`: RotationImpactPreview
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.GetNodeKeysRotatePreview`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the rotation scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetNodeKeysRotatePreviewRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**RotationImpactPreview**](RotationImpactPreview.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetNodeReachability

> Reachability GetNodeReachability(ctx, id).Execute()

Read the reachability projection for a Node.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the reachability scope.

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.GetNodeReachability(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.GetNodeReachability``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetNodeReachability`: Reachability
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.GetNodeReachability`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the reachability scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetNodeReachabilityRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**Reachability**](Reachability.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetNodeState

> NodeStateSnapshot GetNodeState(ctx, id).Execute()

Reconciliation pull for a Node — return the canonical NodeStateSnapshot.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the snapshot scope.

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.GetNodeState(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.GetNodeState``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetNodeState`: NodeStateSnapshot
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.GetNodeState`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the snapshot scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetNodeStateRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**NodeStateSnapshot**](NodeStateSnapshot.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostKeysRotate

> KeysRotateResponse PostKeysRotate(ctx).KeysRotateRequest(keysRotateRequest).Execute()

Submit a freshly-generated Curve25519 key to complete a rotation.



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
	keysRotateRequest := *openapiclient.NewKeysRotateRequest(string(123)) // KeysRotateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.PostKeysRotate(context.Background()).KeysRotateRequest(keysRotateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.PostKeysRotate``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostKeysRotate`: KeysRotateResponse
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.PostKeysRotate`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiPostKeysRotateRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **keysRotateRequest** | [**KeysRotateRequest**](KeysRotateRequest.md) |  | 

### Return type

[**KeysRotateResponse**](KeysRotateResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostNodeAudit

> IngestReceipt PostNodeAudit(ctx, id).Authorization(authorization).AuditEvent(auditEvent).XPlexsphereSentAt(xPlexsphereSentAt).Execute()

Ingest a batch of normalised audit events for a Node.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the ingest scope.
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path `id`; a credential belonging to a different Node surfaces as 403 `node_id_mismatch`. 
	auditEvent := []openapiclient.AuditEvent{*openapiclient.NewAuditEvent(openapiclient.AuditEvent_source("auditd"), "Action_example", "Outcome_example", time.Now())} // []AuditEvent | 
	xPlexsphereSentAt := time.Now() // time.Time | RFC 3339 timestamp at which plexd dispatched the batch. The handler requires it and refuses a missing or unparseable value with 400 `ingest_sent_at_invalid`; it drives the ingest-lag metric the platform records on acceptance.  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.PostNodeAudit(context.Background(), id).Authorization(authorization).AuditEvent(auditEvent).XPlexsphereSentAt(xPlexsphereSentAt).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.PostNodeAudit``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostNodeAudit`: IngestReceipt
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.PostNodeAudit`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the ingest scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostNodeAuditRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path &#x60;id&#x60;; a credential belonging to a different Node surfaces as 403 &#x60;node_id_mismatch&#x60;.  | 
 **auditEvent** | [**[]AuditEvent**](AuditEvent.md) |  | 
 **xPlexsphereSentAt** | **time.Time** | RFC 3339 timestamp at which plexd dispatched the batch. The handler requires it and refuses a missing or unparseable value with 400 &#x60;ingest_sent_at_invalid&#x60;; it drives the ingest-lag metric the platform records on acceptance.  | 

### Return type

[**IngestReceipt**](IngestReceipt.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/x-ndjson
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostNodeHeartbeat

> HeartbeatResponse PostNodeHeartbeat(ctx, id).Authorization(authorization).HeartbeatRequest(heartbeatRequest).Execute()

Record a Node liveness heartbeat and return reconcile/rotate hints.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the heartbeat scope.
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path `id`; a credential belonging to a different Node surfaces as 403 `node_id_mismatch` . 
	heartbeatRequest := *openapiclient.NewHeartbeatRequest(time.Now(), string(123), "BinaryVersion_example", map[string]interface{}{"key": interface{}(123)}) // HeartbeatRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.PostNodeHeartbeat(context.Background(), id).Authorization(authorization).HeartbeatRequest(heartbeatRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.PostNodeHeartbeat``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostNodeHeartbeat`: HeartbeatResponse
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.PostNodeHeartbeat`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the heartbeat scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostNodeHeartbeatRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path &#x60;id&#x60;; a credential belonging to a different Node surfaces as 403 &#x60;node_id_mismatch&#x60; .  | 
 **heartbeatRequest** | [**HeartbeatRequest**](HeartbeatRequest.md) |  | 

### Return type

[**HeartbeatResponse**](HeartbeatResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostNodeIntegrityViolations

> IntegrityViolationsResponse PostNodeIntegrityViolations(ctx, id).Authorization(authorization).IntegrityViolationsRequest(integrityViolationsRequest).Execute()

Ingest a batch of integrity-violation reports for a Node.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the reporting Node.
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path `id`; a credential belonging to a different Node surfaces as 403 `node_id_mismatch`. 
	integrityViolationsRequest := *openapiclient.NewIntegrityViolationsRequest([]openapiclient.IntegrityViolationRequest{*openapiclient.NewIntegrityViolationRequest(openapiclient.IntegrityViolationRequest_kind("binary_checksum"), openapiclient.IntegrityViolationRequest_detected_by("startup_scan"), "ArtifactId_example")}) // IntegrityViolationsRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.PostNodeIntegrityViolations(context.Background(), id).Authorization(authorization).IntegrityViolationsRequest(integrityViolationsRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.PostNodeIntegrityViolations``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostNodeIntegrityViolations`: IntegrityViolationsResponse
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.PostNodeIntegrityViolations`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the reporting Node. | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostNodeIntegrityViolationsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path &#x60;id&#x60;; a credential belonging to a different Node surfaces as 403 &#x60;node_id_mismatch&#x60;.  | 
 **integrityViolationsRequest** | [**IntegrityViolationsRequest**](IntegrityViolationsRequest.md) |  | 

### Return type

[**IntegrityViolationsResponse**](IntegrityViolationsResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostNodeKeysRotate

> RotationTriggerResponse PostNodeKeysRotate(ctx, id).Execute()

Trigger a mesh-key rotation for a Node.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the rotation scope.

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.PostNodeKeysRotate(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.PostNodeKeysRotate``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostNodeKeysRotate`: RotationTriggerResponse
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.PostNodeKeysRotate`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the rotation scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostNodeKeysRotateRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**RotationTriggerResponse**](RotationTriggerResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostNodeLogs

> IngestReceipt PostNodeLogs(ctx, id).Authorization(authorization).LogLine(logLine).XPlexsphereSentAt(xPlexsphereSentAt).Execute()

Ingest a batch of structured log lines for a Node.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the ingest scope.
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path `id`; a credential belonging to a different Node surfaces as 403 `node_id_mismatch`. 
	logLine := []openapiclient.LogLine{*openapiclient.NewLogLine(openapiclient.LogLine_severity("emerg"), "Message_example", time.Now())} // []LogLine | 
	xPlexsphereSentAt := time.Now() // time.Time | RFC 3339 timestamp at which plexd dispatched the batch. The handler requires it and refuses a missing or unparseable value with 400 `ingest_sent_at_invalid`; it drives the ingest-lag metric the platform records on acceptance.  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.PostNodeLogs(context.Background(), id).Authorization(authorization).LogLine(logLine).XPlexsphereSentAt(xPlexsphereSentAt).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.PostNodeLogs``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostNodeLogs`: IngestReceipt
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.PostNodeLogs`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the ingest scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostNodeLogsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path &#x60;id&#x60;; a credential belonging to a different Node surfaces as 403 &#x60;node_id_mismatch&#x60;.  | 
 **logLine** | [**[]LogLine**](LogLine.md) |  | 
 **xPlexsphereSentAt** | **time.Time** | RFC 3339 timestamp at which plexd dispatched the batch. The handler requires it and refuses a missing or unparseable value with 400 &#x60;ingest_sent_at_invalid&#x60;; it drives the ingest-lag metric the platform records on acceptance.  | 

### Return type

[**IngestReceipt**](IngestReceipt.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/x-ndjson
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostNodeMetrics

> IngestReceipt PostNodeMetrics(ctx, id).Authorization(authorization).MetricSample(metricSample).XPlexsphereSentAt(xPlexsphereSentAt).Execute()

Ingest a batch of metric samples for a Node.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the ingest scope.
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path `id`; a credential belonging to a different Node surfaces as 403 `node_id_mismatch`. 
	metricSample := []openapiclient.MetricSample{*openapiclient.NewMetricSample(openapiclient.MetricSample_group("node_resources"), "Name_example", float32(123), time.Now())} // []MetricSample | 
	xPlexsphereSentAt := time.Now() // time.Time | RFC 3339 timestamp at which plexd dispatched the batch. The handler requires it and refuses a missing or unparseable value with 400 `ingest_sent_at_invalid`; it drives the ingest-lag metric the platform records on acceptance.  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.PostNodeMetrics(context.Background(), id).Authorization(authorization).MetricSample(metricSample).XPlexsphereSentAt(xPlexsphereSentAt).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.PostNodeMetrics``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostNodeMetrics`: IngestReceipt
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.PostNodeMetrics`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the ingest scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostNodeMetricsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path &#x60;id&#x60;; a credential belonging to a different Node surfaces as 403 &#x60;node_id_mismatch&#x60;.  | 
 **metricSample** | [**[]MetricSample**](MetricSample.md) |  | 
 **xPlexsphereSentAt** | **time.Time** | RFC 3339 timestamp at which plexd dispatched the batch. The handler requires it and refuses a missing or unparseable value with 400 &#x60;ingest_sent_at_invalid&#x60;; it drives the ingest-lag metric the platform records on acceptance.  | 

### Return type

[**IngestReceipt**](IngestReceipt.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PutNodeCapabilities

> CapabilityManifestResponse PutNodeCapabilities(ctx, id).Authorization(authorization).CapabilityManifestRequest(capabilityManifestRequest).Execute()

Record the per-Node capability manifest snapshot.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the capability manifest scope.
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path `id`; a credential belonging to a different Node surfaces as 403 `node_id_mismatch`. 
	capabilityManifestRequest := *openapiclient.NewCapabilityManifestRequest("BinaryVersion_example", string(123)) // CapabilityManifestRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.PutNodeCapabilities(context.Background(), id).Authorization(authorization).CapabilityManifestRequest(capabilityManifestRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.PutNodeCapabilities``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PutNodeCapabilities`: CapabilityManifestResponse
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.PutNodeCapabilities`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the capability manifest scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiPutNodeCapabilitiesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path &#x60;id&#x60;; a credential belonging to a different Node surfaces as 403 &#x60;node_id_mismatch&#x60;.  | 
 **capabilityManifestRequest** | [**CapabilityManifestRequest**](CapabilityManifestRequest.md) |  | 

### Return type

[**CapabilityManifestResponse**](CapabilityManifestResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PutNodeEndpoint

> EndpointResponse PutNodeEndpoint(ctx, id).Authorization(authorization).EndpointRequest(endpointRequest).Execute()

Record a NAT-observed Peer endpoint observation.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the endpoint scope.
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path `id`; a credential belonging to a different Node surfaces as 403 `node_id_mismatch`. 
	endpointRequest := *openapiclient.NewEndpointRequest("Endpoint_example", openapiclient.EndpointRequest_nat_type("full_cone"), time.Now()) // EndpointRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.PutNodeEndpoint(context.Background(), id).Authorization(authorization).EndpointRequest(endpointRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.PutNodeEndpoint``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PutNodeEndpoint`: EndpointResponse
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.PutNodeEndpoint`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the endpoint scope. | 

### Other Parameters

Other parameters are passed through a pointer to a apiPutNodeEndpointRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path &#x60;id&#x60;; a credential belonging to a different Node surfaces as 403 &#x60;node_id_mismatch&#x60;.  | 
 **endpointRequest** | [**EndpointRequest**](EndpointRequest.md) |  | 

### Return type

[**EndpointResponse**](EndpointResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PutNodeStateReport

> NodeStateReportResponse PutNodeStateReport(ctx, id, key).Authorization(authorization).NodeStateReportRequest(nodeStateReportRequest).Execute()

Record an upstream node-state report entry for a Node.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Node identifier (UUIDv7) — the report-write scope.
	key := "key_example" // string | Report entry key. Lower-case, starts with a letter, and is limited to letters, digits, dot, hyphen, and underscore (1 to 128 characters). 
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. Only a Node proving possession of its NSK may write a report; a missing, malformed, or revoked credential surfaces as 401. 
	nodeStateReportRequest := *openapiclient.NewNodeStateReportRequest("Value_example") // NodeStateReportRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.MeshAPI.PutNodeStateReport(context.Background(), id, key).Authorization(authorization).NodeStateReportRequest(nodeStateReportRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `MeshAPI.PutNodeStateReport``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PutNodeStateReport`: NodeStateReportResponse
	fmt.Fprintf(os.Stdout, "Response from `MeshAPI.PutNodeStateReport`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the report-write scope. | 
**key** | **string** | Report entry key. Lower-case, starts with a letter, and is limited to letters, digits, dot, hyphen, and underscore (1 to 128 characters).  | 

### Other Parameters

Other parameters are passed through a pointer to a apiPutNodeStateReportRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. Only a Node proving possession of its NSK may write a report; a missing, malformed, or revoked credential surfaces as 401.  | 
 **nodeStateReportRequest** | [**NodeStateReportRequest**](NodeStateReportRequest.md) |  | 

### Return type

[**NodeStateReportResponse**](NodeStateReportResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

