# \AuditAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**EraseIdentityFromAudit**](AuditAPI.md#EraseIdentityFromAudit) | **Post** /v1/domains/{domainId}/audit/erase-identity | Erase an identity&#39;s PII mapping from the per-Domain audit log.
[**EraseIdentityFromPlatformAudit**](AuditAPI.md#EraseIdentityFromPlatformAudit) | **Post** /v1/platform/audit/erase-identity | Erase an identity&#39;s PII mapping from the platform audit log.
[**GetAuditEntry**](AuditAPI.md#GetAuditEntry) | **Get** /v1/domains/{domainId}/audit/entries/{seq} | Read a single audit entry with its hash-chain proof.
[**GetPlatformAuditEntry**](AuditAPI.md#GetPlatformAuditEntry) | **Get** /v1/platform/audit/entries/{seq} | Read a single platform audit entry with its hash-chain proof.
[**ListAuditEntries**](AuditAPI.md#ListAuditEntries) | **Get** /v1/domains/{domainId}/audit/entries | List entries on the per-Domain audit chain.
[**ListPlatformAuditEntries**](AuditAPI.md#ListPlatformAuditEntries) | **Get** /v1/platform/audit/entries | List entries on the platform-residency audit chain.
[**VerifyAuditChain**](AuditAPI.md#VerifyAuditChain) | **Post** /v1/domains/{domainId}/audit/verify | Verify the per-Domain hash chain or a segment of it.
[**VerifyPlatformAuditChain**](AuditAPI.md#VerifyPlatformAuditChain) | **Post** /v1/platform/audit/verify | Verify the platform-residency hash chain or a segment of it.



## EraseIdentityFromAudit

> AuditEraseIdentityResponse EraseIdentityFromAudit(ctx, domainId).AuditEraseIdentityRequest(auditEraseIdentityRequest).Execute()

Erase an identity's PII mapping from the per-Domain audit log.



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
	auditEraseIdentityRequest := *openapiclient.NewAuditEraseIdentityRequest("IdentityId_example") // AuditEraseIdentityRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuditAPI.EraseIdentityFromAudit(context.Background(), domainId).AuditEraseIdentityRequest(auditEraseIdentityRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuditAPI.EraseIdentityFromAudit``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `EraseIdentityFromAudit`: AuditEraseIdentityResponse
	fmt.Fprintf(os.Stdout, "Response from `AuditAPI.EraseIdentityFromAudit`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiEraseIdentityFromAuditRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **auditEraseIdentityRequest** | [**AuditEraseIdentityRequest**](AuditEraseIdentityRequest.md) |  | 

### Return type

[**AuditEraseIdentityResponse**](AuditEraseIdentityResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## EraseIdentityFromPlatformAudit

> AuditEraseIdentityResponse EraseIdentityFromPlatformAudit(ctx).AuditEraseIdentityRequest(auditEraseIdentityRequest).Execute()

Erase an identity's PII mapping from the platform audit log.



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
	auditEraseIdentityRequest := *openapiclient.NewAuditEraseIdentityRequest("IdentityId_example") // AuditEraseIdentityRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuditAPI.EraseIdentityFromPlatformAudit(context.Background()).AuditEraseIdentityRequest(auditEraseIdentityRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuditAPI.EraseIdentityFromPlatformAudit``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `EraseIdentityFromPlatformAudit`: AuditEraseIdentityResponse
	fmt.Fprintf(os.Stdout, "Response from `AuditAPI.EraseIdentityFromPlatformAudit`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiEraseIdentityFromPlatformAuditRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auditEraseIdentityRequest** | [**AuditEraseIdentityRequest**](AuditEraseIdentityRequest.md) |  | 

### Return type

[**AuditEraseIdentityResponse**](AuditEraseIdentityResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAuditEntry

> AuditEntryProof GetAuditEntry(ctx, domainId, seq).Execute()

Read a single audit entry with its hash-chain proof.



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
	seq := int64(789) // int64 | Per-Domain monotonic sequence number assigned at append time. Sequences start at 1 (the genesis row) and never reset. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuditAPI.GetAuditEntry(context.Background(), domainId, seq).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuditAPI.GetAuditEntry``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAuditEntry`: AuditEntryProof
	fmt.Fprintf(os.Stdout, "Response from `AuditAPI.GetAuditEntry`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 
**seq** | **int64** | Per-Domain monotonic sequence number assigned at append time. Sequences start at 1 (the genesis row) and never reset.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetAuditEntryRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**AuditEntryProof**](AuditEntryProof.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetPlatformAuditEntry

> AuditEntryProof GetPlatformAuditEntry(ctx, seq).Execute()

Read a single platform audit entry with its hash-chain proof.



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
	seq := int64(789) // int64 | Monotonic sequence number assigned at append time. Sequences start at 1 (the genesis row) and never reset. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuditAPI.GetPlatformAuditEntry(context.Background(), seq).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuditAPI.GetPlatformAuditEntry``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetPlatformAuditEntry`: AuditEntryProof
	fmt.Fprintf(os.Stdout, "Response from `AuditAPI.GetPlatformAuditEntry`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**seq** | **int64** | Monotonic sequence number assigned at append time. Sequences start at 1 (the genesis row) and never reset.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetPlatformAuditEntryRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**AuditEntryProof**](AuditEntryProof.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListAuditEntries

> AuditEntryList ListAuditEntries(ctx, domainId).Cursor(cursor).Limit(limit).Subject(subject).Relation(relation).ObjectType(objectType).ObjectId(objectId).Reason(reason).From(from).To(to).CorrelationId(correlationId).Execute()

List entries on the per-Domain audit chain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain's chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path. 
	cursor := "cursor_example" // string | Opaque pagination cursor — value of `next_cursor` from the previous page, or unset to start at the head of the chain .  (optional)
	limit := int32(56) // int32 | Maximum number of entries to return on this page. Clamped server-side at 200 to protect the read replica from a single auditor issuing an unbounded LIMIT.  (optional) (default to 50)
	subject := "subject_example" // string | Filter by subject pseudonym (64 lowercase hex characters). The query service never accepts plaintext subject ids; pseudonymisation is the caller's responsibility and happens at the sink boundary.  (optional)
	relation := "relation_example" // string | SpiceDB relation label to filter on. (optional)
	objectType := "objectType_example" // string | SpiceDB object type to filter on (e.g. `domain`, `node`). (optional)
	objectId := "objectId_example" // string | Opaque object identifier within `object_type`. (optional)
	reason := openapiclient.AuditReason("granted") // AuditReason | Filter by ReBAC decision reason.  (optional)
	from := time.Now() // time.Time | Inclusive lower bound on `occurred_at` (RFC 3339). (optional)
	to := time.Now() // time.Time | Inclusive upper bound on `occurred_at` (RFC 3339). (optional)
	correlationId := "correlationId_example" // string | Filter by inbound request correlation id. (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuditAPI.ListAuditEntries(context.Background(), domainId).Cursor(cursor).Limit(limit).Subject(subject).Relation(relation).ObjectType(objectType).ObjectId(objectId).Reason(reason).From(from).To(to).CorrelationId(correlationId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuditAPI.ListAuditEntries``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListAuditEntries`: AuditEntryList
	fmt.Fprintf(os.Stdout, "Response from `AuditAPI.ListAuditEntries`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListAuditEntriesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque pagination cursor — value of &#x60;next_cursor&#x60; from the previous page, or unset to start at the head of the chain .  | 
 **limit** | **int32** | Maximum number of entries to return on this page. Clamped server-side at 200 to protect the read replica from a single auditor issuing an unbounded LIMIT.  | [default to 50]
 **subject** | **string** | Filter by subject pseudonym (64 lowercase hex characters). The query service never accepts plaintext subject ids; pseudonymisation is the caller&#39;s responsibility and happens at the sink boundary.  | 
 **relation** | **string** | SpiceDB relation label to filter on. | 
 **objectType** | **string** | SpiceDB object type to filter on (e.g. &#x60;domain&#x60;, &#x60;node&#x60;). | 
 **objectId** | **string** | Opaque object identifier within &#x60;object_type&#x60;. | 
 **reason** | [**AuditReason**](AuditReason.md) | Filter by ReBAC decision reason.  | 
 **from** | **time.Time** | Inclusive lower bound on &#x60;occurred_at&#x60; (RFC 3339). | 
 **to** | **time.Time** | Inclusive upper bound on &#x60;occurred_at&#x60; (RFC 3339). | 
 **correlationId** | **string** | Filter by inbound request correlation id. | 

### Return type

[**AuditEntryList**](AuditEntryList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListPlatformAuditEntries

> AuditEntryList ListPlatformAuditEntries(ctx).Cursor(cursor).Limit(limit).Subject(subject).Relation(relation).ObjectType(objectType).ObjectId(objectId).Reason(reason).From(from).To(to).CorrelationId(correlationId).Execute()

List entries on the platform-residency audit chain.



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
	cursor := "cursor_example" // string | Opaque pagination cursor — value of `next_cursor` from the previous page, or unset to start at the head of the chain .  (optional)
	limit := int32(56) // int32 | Maximum number of entries to return on this page. Clamped server-side at 200 to protect the read replica from a single auditor issuing an unbounded LIMIT.  (optional) (default to 50)
	subject := "subject_example" // string | Filter by subject pseudonym (64 lowercase hex characters). The query service never accepts plaintext subject ids; pseudonymisation is the caller's responsibility and happens at the sink boundary.  (optional)
	relation := "relation_example" // string | SpiceDB relation label to filter on. (optional)
	objectType := "objectType_example" // string | SpiceDB object type to filter on (e.g. `cloud`, `platform`). (optional)
	objectId := "objectId_example" // string | Opaque object identifier within `object_type`. (optional)
	reason := openapiclient.AuditReason("granted") // AuditReason | Filter by ReBAC decision reason.  (optional)
	from := time.Now() // time.Time | Inclusive lower bound on `occurred_at` (RFC 3339). (optional)
	to := time.Now() // time.Time | Inclusive upper bound on `occurred_at` (RFC 3339). (optional)
	correlationId := "correlationId_example" // string | Filter by inbound request correlation id. (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuditAPI.ListPlatformAuditEntries(context.Background()).Cursor(cursor).Limit(limit).Subject(subject).Relation(relation).ObjectType(objectType).ObjectId(objectId).Reason(reason).From(from).To(to).CorrelationId(correlationId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuditAPI.ListPlatformAuditEntries``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListPlatformAuditEntries`: AuditEntryList
	fmt.Fprintf(os.Stdout, "Response from `AuditAPI.ListPlatformAuditEntries`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListPlatformAuditEntriesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cursor** | **string** | Opaque pagination cursor — value of &#x60;next_cursor&#x60; from the previous page, or unset to start at the head of the chain .  | 
 **limit** | **int32** | Maximum number of entries to return on this page. Clamped server-side at 200 to protect the read replica from a single auditor issuing an unbounded LIMIT.  | [default to 50]
 **subject** | **string** | Filter by subject pseudonym (64 lowercase hex characters). The query service never accepts plaintext subject ids; pseudonymisation is the caller&#39;s responsibility and happens at the sink boundary.  | 
 **relation** | **string** | SpiceDB relation label to filter on. | 
 **objectType** | **string** | SpiceDB object type to filter on (e.g. &#x60;cloud&#x60;, &#x60;platform&#x60;). | 
 **objectId** | **string** | Opaque object identifier within &#x60;object_type&#x60;. | 
 **reason** | [**AuditReason**](AuditReason.md) | Filter by ReBAC decision reason.  | 
 **from** | **time.Time** | Inclusive lower bound on &#x60;occurred_at&#x60; (RFC 3339). | 
 **to** | **time.Time** | Inclusive upper bound on &#x60;occurred_at&#x60; (RFC 3339). | 
 **correlationId** | **string** | Filter by inbound request correlation id. | 

### Return type

[**AuditEntryList**](AuditEntryList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## VerifyAuditChain

> AuditChainVerifyResult VerifyAuditChain(ctx, domainId).AuditChainVerifyRequest(auditChainVerifyRequest).Execute()

Verify the per-Domain hash chain or a segment of it.



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
	auditChainVerifyRequest := *openapiclient.NewAuditChainVerifyRequest() // AuditChainVerifyRequest |  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuditAPI.VerifyAuditChain(context.Background(), domainId).AuditChainVerifyRequest(auditChainVerifyRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuditAPI.VerifyAuditChain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `VerifyAuditChain`: AuditChainVerifyResult
	fmt.Fprintf(os.Stdout, "Response from `AuditAPI.VerifyAuditChain`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain. The Platform Audit Log is per-Domain by residency contract — cross-Domain decisions land in EACH affected Domain&#39;s chain, never on a shared system chain . Every audit endpoint requires the Domain identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiVerifyAuditChainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **auditChainVerifyRequest** | [**AuditChainVerifyRequest**](AuditChainVerifyRequest.md) |  | 

### Return type

[**AuditChainVerifyResult**](AuditChainVerifyResult.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## VerifyPlatformAuditChain

> AuditChainVerifyResult VerifyPlatformAuditChain(ctx).AuditChainVerifyRequest(auditChainVerifyRequest).Execute()

Verify the platform-residency hash chain or a segment of it.



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
	auditChainVerifyRequest := *openapiclient.NewAuditChainVerifyRequest() // AuditChainVerifyRequest |  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.AuditAPI.VerifyPlatformAuditChain(context.Background()).AuditChainVerifyRequest(auditChainVerifyRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `AuditAPI.VerifyPlatformAuditChain``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `VerifyPlatformAuditChain`: AuditChainVerifyResult
	fmt.Fprintf(os.Stdout, "Response from `AuditAPI.VerifyPlatformAuditChain`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiVerifyPlatformAuditChainRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auditChainVerifyRequest** | [**AuditChainVerifyRequest**](AuditChainVerifyRequest.md) |  | 

### Return type

[**AuditChainVerifyResult**](AuditChainVerifyResult.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

