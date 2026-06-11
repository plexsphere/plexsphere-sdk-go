# \ManagementFleetAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetManagementCluster**](ManagementFleetAPI.md#GetManagementCluster) | **Get** /v1/management-clusters/{id} | Fetch one management cluster.
[**GetProjectManagementClusterAssignment**](ManagementFleetAPI.md#GetProjectManagementClusterAssignment) | **Get** /v1/projects/{project_id}/management-cluster-assignment | Look up a Project&#39;s management-cluster assignment.
[**ListManagementClusterAssignments**](ManagementFleetAPI.md#ListManagementClusterAssignments) | **Get** /v1/management-clusters/{id}/assignments | List the Project assignments placed on a cluster.
[**ListManagementClusters**](ManagementFleetAPI.md#ListManagementClusters) | **Get** /v1/management-clusters | List the registered management clusters.
[**RegisterManagementCluster**](ManagementFleetAPI.md#RegisterManagementCluster) | **Post** /v1/management-clusters | Register a management cluster into the fleet.
[**TerminateProjectManagementClusterAssignment**](ManagementFleetAPI.md#TerminateProjectManagementClusterAssignment) | **Post** /v1/projects/{project_id}/management-cluster-assignment/terminate | Request teardown of a Project&#39;s namespace.



## GetManagementCluster

> ManagementClusterResponse GetManagementCluster(ctx, id).Execute()

Fetch one management cluster.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Management cluster identifier (UUIDv7). Bound on `/v1/management-clusters/{id}` and `/v1/management-clusters/{id}/assignments` for the operator-facing Management Fleet surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ManagementFleetAPI.GetManagementCluster(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagementFleetAPI.GetManagementCluster``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetManagementCluster`: ManagementClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ManagementFleetAPI.GetManagementCluster`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Management cluster identifier (UUIDv7). Bound on &#x60;/v1/management-clusters/{id}&#x60; and &#x60;/v1/management-clusters/{id}/assignments&#x60; for the operator-facing Management Fleet surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetManagementClusterRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**ManagementClusterResponse**](ManagementClusterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetProjectManagementClusterAssignment

> ProjectClusterAssignmentResponse GetProjectManagementClusterAssignment(ctx, projectId).Execute()

Look up a Project's management-cluster assignment.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/management-cluster-assignment` and its `/terminate` sub-resource — the Management Fleet assignment is keyed by the Project it places. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ManagementFleetAPI.GetProjectManagementClusterAssignment(context.Background(), projectId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagementFleetAPI.GetProjectManagementClusterAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetProjectManagementClusterAssignment`: ProjectClusterAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `ManagementFleetAPI.GetProjectManagementClusterAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/management-cluster-assignment&#x60; and its &#x60;/terminate&#x60; sub-resource — the Management Fleet assignment is keyed by the Project it places.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetProjectManagementClusterAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**ProjectClusterAssignmentResponse**](ProjectClusterAssignmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListManagementClusterAssignments

> ProjectClusterAssignmentList ListManagementClusterAssignments(ctx, id).Execute()

List the Project assignments placed on a cluster.



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
	id := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Management cluster identifier (UUIDv7). Bound on `/v1/management-clusters/{id}` and `/v1/management-clusters/{id}/assignments` for the operator-facing Management Fleet surface. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ManagementFleetAPI.ListManagementClusterAssignments(context.Background(), id).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagementFleetAPI.ListManagementClusterAssignments``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListManagementClusterAssignments`: ProjectClusterAssignmentList
	fmt.Fprintf(os.Stdout, "Response from `ManagementFleetAPI.ListManagementClusterAssignments`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Management cluster identifier (UUIDv7). Bound on &#x60;/v1/management-clusters/{id}&#x60; and &#x60;/v1/management-clusters/{id}/assignments&#x60; for the operator-facing Management Fleet surface.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListManagementClusterAssignmentsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**ProjectClusterAssignmentList**](ProjectClusterAssignmentList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListManagementClusters

> ManagementClusterList ListManagementClusters(ctx).Execute()

List the registered management clusters.



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
	resp, r, err := apiClient.ManagementFleetAPI.ListManagementClusters(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagementFleetAPI.ListManagementClusters``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListManagementClusters`: ManagementClusterList
	fmt.Fprintf(os.Stdout, "Response from `ManagementFleetAPI.ListManagementClusters`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiListManagementClustersRequest struct via the builder pattern


### Return type

[**ManagementClusterList**](ManagementClusterList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## RegisterManagementCluster

> ManagementClusterResponse RegisterManagementCluster(ctx).RegisterManagementClusterRequest(registerManagementClusterRequest).Execute()

Register a management cluster into the fleet.



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
	registerManagementClusterRequest := *openapiclient.NewRegisterManagementClusterRequest("Name_example", "Slug_example", "KubeconfigSecretRef_example") // RegisterManagementClusterRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ManagementFleetAPI.RegisterManagementCluster(context.Background()).RegisterManagementClusterRequest(registerManagementClusterRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagementFleetAPI.RegisterManagementCluster``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `RegisterManagementCluster`: ManagementClusterResponse
	fmt.Fprintf(os.Stdout, "Response from `ManagementFleetAPI.RegisterManagementCluster`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiRegisterManagementClusterRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **registerManagementClusterRequest** | [**RegisterManagementClusterRequest**](RegisterManagementClusterRequest.md) |  | 

### Return type

[**ManagementClusterResponse**](ManagementClusterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## TerminateProjectManagementClusterAssignment

> ProjectClusterAssignmentResponse TerminateProjectManagementClusterAssignment(ctx, projectId).Execute()

Request teardown of a Project's namespace.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project (UUIDv7). Bound on `/v1/projects/{project_id}/management-cluster-assignment` and its `/terminate` sub-resource — the Management Fleet assignment is keyed by the Project it places. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ManagementFleetAPI.TerminateProjectManagementClusterAssignment(context.Background(), projectId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ManagementFleetAPI.TerminateProjectManagementClusterAssignment``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `TerminateProjectManagementClusterAssignment`: ProjectClusterAssignmentResponse
	fmt.Fprintf(os.Stdout, "Response from `ManagementFleetAPI.TerminateProjectManagementClusterAssignment`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/management-cluster-assignment&#x60; and its &#x60;/terminate&#x60; sub-resource — the Management Fleet assignment is keyed by the Project it places.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiTerminateProjectManagementClusterAssignmentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


### Return type

[**ProjectClusterAssignmentResponse**](ProjectClusterAssignmentResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

