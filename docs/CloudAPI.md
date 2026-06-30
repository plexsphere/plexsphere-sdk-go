# \CloudAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ApproveCloudAssignment**](CloudAPI.md#ApproveCloudAssignment) | **Post** /v1/cloud-assignments/{id}/approve | Approve a Cloud Assignment request.
[**ApproveCredentialAssignment**](CloudAPI.md#ApproveCredentialAssignment) | **Post** /v1/credential-assignments/{id}/approve | Approve a Credential Assignment.
[**AttachCloudCredentialCloud**](CloudAPI.md#AttachCloudCredentialCloud) | **Post** /v1/cloud-credentials/{id}/clouds | Attach a usage Cloud to a Cloud Credential.
[**CreateCloud**](CloudAPI.md#CreateCloud) | **Post** /v1/clouds | Create a Cloud Inventory entry.
[**DeleteCloud**](CloudAPI.md#DeleteCloud) | **Delete** /v1/clouds/{id} | Delete a Cloud.
[**DetachCloudCredentialCloud**](CloudAPI.md#DetachCloudCredentialCloud) | **Delete** /v1/cloud-credentials/{id}/clouds/{cloudId} | Detach a usage Cloud from a Cloud Credential.
[**GetCloud**](CloudAPI.md#GetCloud) | **Get** /v1/clouds/{id} | Fetch a Cloud by identifier.
[**GetCloudCredential**](CloudAPI.md#GetCloudCredential) | **Get** /v1/cloud-credentials/{id} | Fetch a Cloud Credential&#39;s lifecycle metadata.
[**GrantCloudAssignment**](CloudAPI.md#GrantCloudAssignment) | **Post** /v1/clouds/{id}/cloud-assignments | Grant a Cloud to a Project (operator push).
[**IssueCloudCredential**](CloudAPI.md#IssueCloudCredential) | **Post** /v1/clouds/{id}/cloud-credentials | Issue a new Cloud Credential under a Cloud.
[**ListCloudAssignments**](CloudAPI.md#ListCloudAssignments) | **Get** /v1/projects/{id}/cloud-assignments | List the Cloud Assignments owned by a Project.
[**ListCloudCredentialClouds**](CloudAPI.md#ListCloudCredentialClouds) | **Get** /v1/cloud-credentials/{id}/clouds | List the Clouds a Cloud Credential serves.
[**ListCloudCredentials**](CloudAPI.md#ListCloudCredentials) | **Get** /v1/clouds/{id}/cloud-credentials | List Cloud Credentials owned by a Cloud.
[**ListClouds**](CloudAPI.md#ListClouds) | **Get** /v1/clouds | List Cloud Inventory entries.
[**ListCredentialAssignments**](CloudAPI.md#ListCredentialAssignments) | **Get** /v1/projects/{id}/credential-assignments | List the Credential Assignments owned by a Project.
[**PatchCloud**](CloudAPI.md#PatchCloud) | **Patch** /v1/clouds/{id} | Patch mutable fields on a Cloud.
[**RejectCloudAssignment**](CloudAPI.md#RejectCloudAssignment) | **Post** /v1/cloud-assignments/{id}/reject | Reject a Cloud Assignment request.
[**RejectCredentialAssignment**](CloudAPI.md#RejectCredentialAssignment) | **Post** /v1/credential-assignments/{id}/reject | Reject a Credential Assignment.
[**RequestCloudAssignment**](CloudAPI.md#RequestCloudAssignment) | **Post** /v1/projects/{id}/cloud-assignments | Request usage of a Cloud for a Project.
[**RequestCredentialAssignment**](CloudAPI.md#RequestCredentialAssignment) | **Post** /v1/projects/{id}/credential-assignments | Request a Credential Assignment for a Project.
[**RevokeCloudAssignment**](CloudAPI.md#RevokeCloudAssignment) | **Post** /v1/cloud-assignments/{id}/revoke | Revoke a Cloud Assignment.
[**RevokeCloudCredential**](CloudAPI.md#RevokeCloudCredential) | **Post** /v1/cloud-credentials/{id}/revoke | Revoke a Cloud Credential.
[**RevokeCredentialAssignment**](CloudAPI.md#RevokeCredentialAssignment) | **Post** /v1/credential-assignments/{id}/revoke | Revoke a Credential Assignment.



## ApproveCloudAssignment

> CloudAssignmentResponse ApproveCloudAssignment(ctx, id).Execute()

Approve a Cloud Assignment request.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Cloud Assignment identifier (UUIDv7). Bound on `/v1/cloud-assignments/{id}/approve`, `/v1/cloud-assignments/{id}/reject`, and `/v1/cloud-assignments/{id}/revoke` for the Cloud Assignment decision surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.ApproveCloudAssignment(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.ApproveCloudAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ApproveCloudAssignment`: CloudAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.ApproveCloudAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud Assignment identifier (UUIDv7). Bound on &#x60;/v1/cloud-assignments/{id}/approve&#x60;, &#x60;/v1/cloud-assignments/{id}/reject&#x60;, and &#x60;/v1/cloud-assignments/{id}/revoke&#x60; for the Cloud Assignment decision surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiApproveCloudAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**CloudAssignmentResponse**](CloudAssignmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


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


## AttachCloudCredentialCloud

> CloudUsageRef AttachCloudCredentialCloud(ctx, id).CloudCredentialAttachRequest(cloudCredentialAttachRequest).Execute()

Attach a usage Cloud to a Cloud Credential.



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
	cloudCredentialAttachRequest := *openapiclient.NewCloudCredentialAttachRequest("CloudId_example") // CloudCredentialAttachRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.AttachCloudCredentialCloud(context.Background(), id).CloudCredentialAttachRequest(cloudCredentialAttachRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.AttachCloudCredentialCloud``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AttachCloudCredentialCloud`: CloudUsageRef
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.AttachCloudCredentialCloud`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud Credential identifier (UUIDv7). Bound on &#x60;/v1/cloud-credentials/{id}&#x60; and &#x60;/v1/cloud-credentials/{id}/revoke&#x60; for the operator-facing Cloud Credentials read + revoke surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiAttachCloudCredentialCloudRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cloudCredentialAttachRequest** | [**CloudCredentialAttachRequest**](CloudCredentialAttachRequest.md) |  | 

### Return type

[**CloudUsageRef**](CloudUsageRef.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
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


## DetachCloudCredentialCloud

> DetachCloudCredentialCloud(ctx, id, cloudId).Execute()

Detach a usage Cloud from a Cloud Credential.



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
	cloudId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Identifier of the usage Cloud to detach (UUIDv7). Must be a non-zero UUID — a malformed value is rejected with `400 invalid_cloud_id`. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.CloudAPI.DetachCloudCredentialCloud(context.Background(), id, cloudId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.DetachCloudCredentialCloud``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud Credential identifier (UUIDv7). Bound on &#x60;/v1/cloud-credentials/{id}&#x60; and &#x60;/v1/cloud-credentials/{id}/revoke&#x60; for the operator-facing Cloud Credentials read + revoke surface.  | 
**cloudId** | **string** | Identifier of the usage Cloud to detach (UUIDv7). Must be a non-zero UUID — a malformed value is rejected with &#x60;400 invalid_cloud_id&#x60;.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDetachCloudCredentialCloudRequest struct via the builder pattern


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


## GrantCloudAssignment

> CloudAssignmentResponse GrantCloudAssignment(ctx, id).CloudAssignmentGrantRequest(cloudAssignmentGrantRequest).Execute()

Grant a Cloud to a Project (operator push).



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
	cloudAssignmentGrantRequest := *openapiclient.NewCloudAssignmentGrantRequest("ProjectId_example") // CloudAssignmentGrantRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.GrantCloudAssignment(context.Background(), id).CloudAssignmentGrantRequest(cloudAssignmentGrantRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.GrantCloudAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GrantCloudAssignment`: CloudAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.GrantCloudAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud identifier (UUIDv7). Bound on &#x60;/v1/clouds/{id}&#x60; for the Cloud Inventory CRUD surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGrantCloudAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cloudAssignmentGrantRequest** | [**CloudAssignmentGrantRequest**](CloudAssignmentGrantRequest.md) |  | 

### Return type

[**CloudAssignmentResponse**](CloudAssignmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
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


## ListCloudAssignments

> CloudAssignmentList ListCloudAssignments(ctx, id).Cursor(cursor).Limit(limit).Execute()

List the Cloud Assignments owned by a Project.



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
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the application service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.ListCloudAssignments(context.Background(), id).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.ListCloudAssignments``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCloudAssignments`: CloudAssignmentList
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.ListCloudAssignments`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface and on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListCloudAssignmentsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the application service.  | [default to 50]

### Return type

[**CloudAssignmentList**](CloudAssignmentList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListCloudCredentialClouds

> CloudCredentialCloudList ListCloudCredentialClouds(ctx, id).Cursor(cursor).Limit(limit).Execute()

List the Clouds a Cloud Credential serves.



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
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.ListCloudCredentialClouds(context.Background(), id).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.ListCloudCredentialClouds``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListCloudCredentialClouds`: CloudCredentialCloudList
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.ListCloudCredentialClouds`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud Credential identifier (UUIDv7). Bound on &#x60;/v1/cloud-credentials/{id}&#x60; and &#x60;/v1/cloud-credentials/{id}/revoke&#x60; for the operator-facing Cloud Credentials read + revoke surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListCloudCredentialCloudsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**CloudCredentialCloudList**](CloudCredentialCloudList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
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


## RejectCloudAssignment

> CloudAssignmentResponse RejectCloudAssignment(ctx, id).CloudAssignmentDecisionRequest(cloudAssignmentDecisionRequest).Execute()

Reject a Cloud Assignment request.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Cloud Assignment identifier (UUIDv7). Bound on `/v1/cloud-assignments/{id}/approve`, `/v1/cloud-assignments/{id}/reject`, and `/v1/cloud-assignments/{id}/revoke` for the Cloud Assignment decision surface. 
	cloudAssignmentDecisionRequest := *openapiclient.NewCloudAssignmentDecisionRequest("Reason_example") // CloudAssignmentDecisionRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.RejectCloudAssignment(context.Background(), id).CloudAssignmentDecisionRequest(cloudAssignmentDecisionRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.RejectCloudAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RejectCloudAssignment`: CloudAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.RejectCloudAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud Assignment identifier (UUIDv7). Bound on &#x60;/v1/cloud-assignments/{id}/approve&#x60;, &#x60;/v1/cloud-assignments/{id}/reject&#x60;, and &#x60;/v1/cloud-assignments/{id}/revoke&#x60; for the Cloud Assignment decision surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRejectCloudAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cloudAssignmentDecisionRequest** | [**CloudAssignmentDecisionRequest**](CloudAssignmentDecisionRequest.md) |  | 

### Return type

[**CloudAssignmentResponse**](CloudAssignmentResponse.md)

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


## RequestCloudAssignment

> CloudAssignmentResponse RequestCloudAssignment(ctx, id).CloudAssignmentRequestBody(cloudAssignmentRequestBody).Execute()

Request usage of a Cloud for a Project.



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
	cloudAssignmentRequestBody := *openapiclient.NewCloudAssignmentRequestBody("CloudId_example") // CloudAssignmentRequestBody | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.RequestCloudAssignment(context.Background(), id).CloudAssignmentRequestBody(cloudAssignmentRequestBody).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.RequestCloudAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RequestCloudAssignment`: CloudAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.RequestCloudAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Project identifier (UUIDv7). Bound on &#x60;/v1/projects/{id}&#x60; for the tenancy CRUD surface and on &#x60;/v1/projects/{id}/credentials&#x60; for the operator-facing OpenBao Credential Broker inventory list.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRequestCloudAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cloudAssignmentRequestBody** | [**CloudAssignmentRequestBody**](CloudAssignmentRequestBody.md) |  | 

### Return type

[**CloudAssignmentResponse**](CloudAssignmentResponse.md)

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
	credentialAssignmentRequest := *openapiclient.NewCredentialAssignmentRequest() // CredentialAssignmentRequest | 

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


## RevokeCloudAssignment

> CloudAssignmentResponse RevokeCloudAssignment(ctx, id).CloudAssignmentDecisionRequest(cloudAssignmentDecisionRequest).Execute()

Revoke a Cloud Assignment.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Cloud Assignment identifier (UUIDv7). Bound on `/v1/cloud-assignments/{id}/approve`, `/v1/cloud-assignments/{id}/reject`, and `/v1/cloud-assignments/{id}/revoke` for the Cloud Assignment decision surface. 
	cloudAssignmentDecisionRequest := *openapiclient.NewCloudAssignmentDecisionRequest("Reason_example") // CloudAssignmentDecisionRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.CloudAPI.RevokeCloudAssignment(context.Background(), id).CloudAssignmentDecisionRequest(cloudAssignmentDecisionRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `CloudAPI.RevokeCloudAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RevokeCloudAssignment`: CloudAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `CloudAPI.RevokeCloudAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Cloud Assignment identifier (UUIDv7). Bound on &#x60;/v1/cloud-assignments/{id}/approve&#x60;, &#x60;/v1/cloud-assignments/{id}/reject&#x60;, and &#x60;/v1/cloud-assignments/{id}/revoke&#x60; for the Cloud Assignment decision surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiRevokeCloudAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cloudAssignmentDecisionRequest** | [**CloudAssignmentDecisionRequest**](CloudAssignmentDecisionRequest.md) |  | 

### Return type

[**CloudAssignmentResponse**](CloudAssignmentResponse.md)

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

