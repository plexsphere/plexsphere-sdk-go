# \CloudAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ApproveCredentialAssignment**](CloudAPI.md#ApproveCredentialAssignment) | **Post** /v1/credential-assignments/{id}/approve | Approve a Credential Assignment.
[**CreateCloud**](CloudAPI.md#CreateCloud) | **Post** /v1/clouds | Create a Cloud Inventory entry.
[**DeleteCloud**](CloudAPI.md#DeleteCloud) | **Delete** /v1/clouds/{id} | Delete a Cloud.
[**GetCloud**](CloudAPI.md#GetCloud) | **Get** /v1/clouds/{id} | Fetch a Cloud by identifier.
[**GetCloudCredential**](CloudAPI.md#GetCloudCredential) | **Get** /v1/cloud-credentials/{id} | Fetch a Cloud Credential&#39;s lifecycle metadata.
[**IssueCloudCredential**](CloudAPI.md#IssueCloudCredential) | **Post** /v1/clouds/{id}/cloud-credentials | Issue a new Cloud Credential under a Cloud.
[**ListCloudCredentials**](CloudAPI.md#ListCloudCredentials) | **Get** /v1/clouds/{id}/cloud-credentials | List Cloud Credentials owned by a Cloud.
[**ListClouds**](CloudAPI.md#ListClouds) | **Get** /v1/clouds | List Cloud Inventory entries.
[**ListCredentialAssignments**](CloudAPI.md#ListCredentialAssignments) | **Get** /v1/projects/{id}/credential-assignments | List the Credential Assignments owned by a Project.
[**PatchCloud**](CloudAPI.md#PatchCloud) | **Patch** /v1/clouds/{id} | Patch mutable fields on a Cloud.
[**RejectCredentialAssignment**](CloudAPI.md#RejectCredentialAssignment) | **Post** /v1/credential-assignments/{id}/reject | Reject a Credential Assignment.
[**RequestCredentialAssignment**](CloudAPI.md#RequestCredentialAssignment) | **Post** /v1/projects/{id}/credential-assignments | Request a Credential Assignment for a Project.
[**RevokeCloudCredential**](CloudAPI.md#RevokeCloudCredential) | **Post** /v1/cloud-credentials/{id}/revoke | Revoke a Cloud Credential.
[**RevokeCredentialAssignment**](CloudAPI.md#RevokeCredentialAssignment) | **Post** /v1/credential-assignments/{id}/revoke | Revoke a Credential Assignment.



## ApproveCredentialAssignment

> CredentialAssignmentResponse ApproveCredentialAssignment(ctx, id).Execute()

Approve a Credential Assignment.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Credential Assignment identifier (UUIDv7). Bound on `/v1/credential-assignments/{id}/approve`, `/v1/credential-assignments/{id}/reject`, and `/v1/credential-assignments/{id}/revoke` for the Credential Assignment decision surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.ApproveCredentialAssignment(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.ApproveCredentialAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ApproveCredentialAssignment`: CredentialAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.ApproveCredentialAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Credential Assignment identifier (UUIDv7). Bound on &#x60;/v1/credential-assignments/{id}/approve&#x60;, &#x60;/v1/credential-assignments/{id}/reject&#x60;, and &#x60;/v1/credential-assignments/{id}/revoke&#x60; for the Credential Assignment decision surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiApproveCredentialAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**CredentialAssignmentResponse**](CredentialAssignmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateCloud

> CloudResponse CreateCloud(ctx).CloudCreateRequest(cloudCreateRequest).Execute()

Create a Cloud Inventory entry.



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
	cloudCreateRequest := *openapiclient.NewCloudCreateRequest("DisplayName_example", "Slug_example", openapiclient.CloudProvider("aws"), map[string]interface{}{"key": interface{}(123)}, map[string]interface{}{"key": interface{}(123)}, "ExternalId_example") // CloudCreateRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.CreateCloud(context.Background()).CloudCreateRequest(cloudCreateRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.CreateCloud``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateCloud`: CloudResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.CreateCloud`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiCreateCloudRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cloudCreateRequest** | [**CloudCreateRequest**](CloudCreateRequest.md) |  | 

### Return type

[**CloudResponse**](CloudResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteCloud

> DeleteCloud(ctx, id).Execute()

Delete a Cloud.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Cloud identifier (UUIDv7). Bound on `/v1/clouds/{id}` for the Cloud Inventory CRUD surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.CloudAPI.DeleteCloud(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.DeleteCloud``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud identifier (UUIDv7). Bound on &#x60;/v1/clouds/{id}&#x60; for the Cloud Inventory CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteCloudRequest struct via the builder pattern


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


## GetCloud

> CloudResponse GetCloud(ctx, id).Execute()

Fetch a Cloud by identifier.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Cloud identifier (UUIDv7). Bound on `/v1/clouds/{id}` for the Cloud Inventory CRUD surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.GetCloud(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.GetCloud``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetCloud`: CloudResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.GetCloud`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud identifier (UUIDv7). Bound on &#x60;/v1/clouds/{id}&#x60; for the Cloud Inventory CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetCloudRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**CloudResponse**](CloudResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetCloudCredential

> CloudCredentialResponse GetCloudCredential(ctx, id).Execute()

Fetch a Cloud Credential's lifecycle metadata.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Cloud Credential identifier (UUIDv7). Bound on `/v1/cloud-credentials/{id}` and `/v1/cloud-credentials/{id}/revoke` for the operator-facing Cloud Credentials read + revoke surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.GetCloudCredential(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.GetCloudCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetCloudCredential`: CloudCredentialResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.GetCloudCredential`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud Credential identifier (UUIDv7). Bound on &#x60;/v1/cloud-credentials/{id}&#x60; and &#x60;/v1/cloud-credentials/{id}/revoke&#x60; for the operator-facing Cloud Credentials read + revoke surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetCloudCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**CloudCredentialResponse**](CloudCredentialResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## IssueCloudCredential

> CloudCredentialResponse IssueCloudCredential(ctx, id).CloudCredentialIssueRequest(cloudCredentialIssueRequest).Execute()

Issue a new Cloud Credential under a Cloud.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Cloud identifier (UUIDv7). Bound on `/v1/clouds/{id}` for the Cloud Inventory CRUD surface. 
	cloudCredentialIssueRequest := *openapiclient.NewCloudCredentialIssueRequest("DisplayName_example", string(123)) // CloudCredentialIssueRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.IssueCloudCredential(context.Background(), id).CloudCredentialIssueRequest(cloudCredentialIssueRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.IssueCloudCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `IssueCloudCredential`: CloudCredentialResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.IssueCloudCredential`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud identifier (UUIDv7). Bound on &#x60;/v1/clouds/{id}&#x60; for the Cloud Inventory CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiIssueCloudCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cloudCredentialIssueRequest** | [**CloudCredentialIssueRequest**](CloudCredentialIssueRequest.md) |  | 

### Return type

[**CloudCredentialResponse**](CloudCredentialResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCloudCredentials

> CloudCredentialList ListCloudCredentials(ctx, id).Cursor(cursor).Limit(limit).Execute()

List Cloud Credentials owned by a Cloud.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Cloud identifier (UUIDv7). Bound on `/v1/clouds/{id}` for the Cloud Inventory CRUD surface. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.ListCloudCredentials(context.Background(), id).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.ListCloudCredentials``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCloudCredentials`: CloudCredentialList
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.ListCloudCredentials`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud identifier (UUIDv7). Bound on &#x60;/v1/clouds/{id}&#x60; for the Cloud Inventory CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListCloudCredentialsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**CloudCredentialList**](CloudCredentialList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListClouds

> CloudList ListClouds(ctx).Cursor(cursor).Limit(limit).Execute()

List Cloud Inventory entries.



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
	resp, r, err := apiClient.CloudAPI.ListClouds(context.Background()).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.ListClouds``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListClouds`: CloudList
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.ListClouds`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiListCloudsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the service.  | [default to 50]

### Return type

[**CloudList**](CloudList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCredentialAssignments

> CredentialAssignmentList ListCredentialAssignments(ctx, id).Cursor(cursor).Limit(limit).Execute()

List the Credential Assignments owned by a Project.



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
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.ListCredentialAssignments(context.Background(), id).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.ListCredentialAssignments``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCredentialAssignments`: CredentialAssignmentList
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.ListCredentialAssignments`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface and on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListCredentialAssignmentsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**CredentialAssignmentList**](CredentialAssignmentList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PatchCloud

> CloudResponse PatchCloud(ctx, id).CloudPatchRequest(cloudPatchRequest).Execute()

Patch mutable fields on a Cloud.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Cloud identifier (UUIDv7). Bound on `/v1/clouds/{id}` for the Cloud Inventory CRUD surface. 
	cloudPatchRequest := *openapiclient.NewCloudPatchRequest() // CloudPatchRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.PatchCloud(context.Background(), id).CloudPatchRequest(cloudPatchRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.PatchCloud``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PatchCloud`: CloudResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.PatchCloud`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud identifier (UUIDv7). Bound on &#x60;/v1/clouds/{id}&#x60; for the Cloud Inventory CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiPatchCloudRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cloudPatchRequest** | [**CloudPatchRequest**](CloudPatchRequest.md) |  | 

### Return type

[**CloudResponse**](CloudResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RejectCredentialAssignment

> CredentialAssignmentResponse RejectCredentialAssignment(ctx, id).CredentialAssignmentDecisionRequest(credentialAssignmentDecisionRequest).Execute()

Reject a Credential Assignment.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Credential Assignment identifier (UUIDv7). Bound on `/v1/credential-assignments/{id}/approve`, `/v1/credential-assignments/{id}/reject`, and `/v1/credential-assignments/{id}/revoke` for the Credential Assignment decision surface. 
	credentialAssignmentDecisionRequest := *openapiclient.NewCredentialAssignmentDecisionRequest("Reason_example") // CredentialAssignmentDecisionRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.RejectCredentialAssignment(context.Background(), id).CredentialAssignmentDecisionRequest(credentialAssignmentDecisionRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.RejectCredentialAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RejectCredentialAssignment`: CredentialAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.RejectCredentialAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Credential Assignment identifier (UUIDv7). Bound on &#x60;/v1/credential-assignments/{id}/approve&#x60;, &#x60;/v1/credential-assignments/{id}/reject&#x60;, and &#x60;/v1/credential-assignments/{id}/revoke&#x60; for the Credential Assignment decision surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRejectCredentialAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **credentialAssignmentDecisionRequest** | [**CredentialAssignmentDecisionRequest**](CredentialAssignmentDecisionRequest.md) |  | 

### Return type

[**CredentialAssignmentResponse**](CredentialAssignmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RequestCredentialAssignment

> CredentialAssignmentResponse RequestCredentialAssignment(ctx, id).CredentialAssignmentRequest(credentialAssignmentRequest).Execute()

Request a Credential Assignment for a Project.



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
	credentialAssignmentRequest := *openapiclient.NewCredentialAssignmentRequest("CloudCredentialId_example") // CredentialAssignmentRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.RequestCredentialAssignment(context.Background(), id).CredentialAssignmentRequest(credentialAssignmentRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.RequestCredentialAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RequestCredentialAssignment`: CredentialAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.RequestCredentialAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface and on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRequestCredentialAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **credentialAssignmentRequest** | [**CredentialAssignmentRequest**](CredentialAssignmentRequest.md) |  | 

### Return type

[**CredentialAssignmentResponse**](CredentialAssignmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RevokeCloudCredential

> CloudCredentialResponse RevokeCloudCredential(ctx, id).CloudCredentialRevokeRequest(cloudCredentialRevokeRequest).Execute()

Revoke a Cloud Credential.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Cloud Credential identifier (UUIDv7). Bound on `/v1/cloud-credentials/{id}` and `/v1/cloud-credentials/{id}/revoke` for the operator-facing Cloud Credentials read + revoke surface. 
	cloudCredentialRevokeRequest := *openapiclient.NewCloudCredentialRevokeRequest("Reason_example") // CloudCredentialRevokeRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.RevokeCloudCredential(context.Background(), id).CloudCredentialRevokeRequest(cloudCredentialRevokeRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.RevokeCloudCredential``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RevokeCloudCredential`: CloudCredentialResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.RevokeCloudCredential`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud Credential identifier (UUIDv7). Bound on &#x60;/v1/cloud-credentials/{id}&#x60; and &#x60;/v1/cloud-credentials/{id}/revoke&#x60; for the operator-facing Cloud Credentials read + revoke surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRevokeCloudCredentialRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cloudCredentialRevokeRequest** | [**CloudCredentialRevokeRequest**](CloudCredentialRevokeRequest.md) |  | 

### Return type

[**CloudCredentialResponse**](CloudCredentialResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RevokeCredentialAssignment

> CredentialAssignmentResponse RevokeCredentialAssignment(ctx, id).CredentialAssignmentDecisionRequest(credentialAssignmentDecisionRequest).Execute()

Revoke a Credential Assignment.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Credential Assignment identifier (UUIDv7). Bound on `/v1/credential-assignments/{id}/approve`, `/v1/credential-assignments/{id}/reject`, and `/v1/credential-assignments/{id}/revoke` for the Credential Assignment decision surface. 
	credentialAssignmentDecisionRequest := *openapiclient.NewCredentialAssignmentDecisionRequest("Reason_example") // CredentialAssignmentDecisionRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.RevokeCredentialAssignment(context.Background(), id).CredentialAssignmentDecisionRequest(credentialAssignmentDecisionRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.RevokeCredentialAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RevokeCredentialAssignment`: CredentialAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.RevokeCredentialAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Credential Assignment identifier (UUIDv7). Bound on &#x60;/v1/credential-assignments/{id}/approve&#x60;, &#x60;/v1/credential-assignments/{id}/reject&#x60;, and &#x60;/v1/credential-assignments/{id}/revoke&#x60; for the Credential Assignment decision surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRevokeCredentialAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **credentialAssignmentDecisionRequest** | [**CredentialAssignmentDecisionRequest**](CredentialAssignmentDecisionRequest.md) |  | 

### Return type

[**CredentialAssignmentResponse**](CredentialAssignmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

