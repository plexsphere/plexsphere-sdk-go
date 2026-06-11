# \ActionsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DispatchExecution**](ActionsAPI.md#DispatchExecution) | **Post** /v1/projects/{project_id}/executions:dispatch | Dispatch an action to a single Node or a label-selected cohort.
[**GetExecution**](ActionsAPI.md#GetExecution) | **Get** /v1/projects/{project_id}/executions/{execution_id} | Inspect a single action Execution.
[**ListExecutions**](ActionsAPI.md#ListExecutions) | **Get** /v1/projects/{project_id}/executions | List action Executions for a Project.
[**PostNodeExecutionCallback**](ActionsAPI.md#PostNodeExecutionCallback) | **Post** /v1/nodes/{id}/executions/{exec_id} | Report an action-execution status advance from a Node.



## DispatchExecution

> Execution DispatchExecution(ctx, projectId).DispatchExecutionRequest(dispatchExecutionRequest).Execute()

Dispatch an action to a single Node or a label-selected cohort.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The Action Orchestrator dispatch and read operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path. 
	dispatchExecutionRequest := *openapiclient.NewDispatchExecutionRequest("Action_example") // DispatchExecutionRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ActionsAPI.DispatchExecution(context.Background(), projectId).DispatchExecutionRequest(dispatchExecutionRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ActionsAPI.DispatchExecution``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DispatchExecution`: Execution
	fmt.Fprintf(os.Stdout, "Response from `ActionsAPI.DispatchExecution`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The Action Orchestrator dispatch and read operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDispatchExecutionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **dispatchExecutionRequest** | [**DispatchExecutionRequest**](DispatchExecutionRequest.md) |  | 

### Return type

[**Execution**](Execution.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetExecution

> Execution GetExecution(ctx, projectId, executionId).Execute()

Inspect a single action Execution.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The Action Orchestrator dispatch and read operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path. 
	executionId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Execution identifier (UUIDv7). Bound on `/v1/projects/{project_id}/executions/{execution_id}` for the single-Execution read. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ActionsAPI.GetExecution(context.Background(), projectId, executionId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ActionsAPI.GetExecution``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetExecution`: Execution
	fmt.Fprintf(os.Stdout, "Response from `ActionsAPI.GetExecution`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The Action Orchestrator dispatch and read operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path.  | 
**executionId** | **string** | Execution identifier (UUIDv7). Bound on &#x60;/v1/projects/{project_id}/executions/{execution_id}&#x60; for the single-Execution read.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetExecutionRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**Execution**](Execution.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListExecutions

> ExecutionList ListExecutions(ctx, projectId).Status(status).ActionName(actionName).Cursor(cursor).Limit(limit).Execute()

List action Executions for a Project.



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
	projectId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Project. The Action Orchestrator dispatch and read operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path. 
	status := openapiclient.ExecutionStatus("pending") // ExecutionStatus | Optional aggregate-status filter. When present, only Executions whose aggregate status equals the named value are returned.  (optional)
	actionName := "actionName_example" // string | Optional action-name filter. When present, only Executions for the named action are returned.  (optional)
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ActionsAPI.ListExecutions(context.Background(), projectId).Status(status).ActionName(actionName).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ActionsAPI.ListExecutions``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListExecutions`: ExecutionList
	fmt.Fprintf(os.Stdout, "Response from `ActionsAPI.ListExecutions`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**projectId** | **string** | Owning Project. The Action Orchestrator dispatch and read operations are scoped per Project, so every operator-facing endpoint requires the Project identifier in the path.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListExecutionsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **status** | [**ExecutionStatus**](ExecutionStatus.md) | Optional aggregate-status filter. When present, only Executions whose aggregate status equals the named value are returned.  | 
 **actionName** | **string** | Optional action-name filter. When present, only Executions for the named action are returned.  | 
 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. The handler clamps the value to [1, 200] before forwarding it to the read service.  | [default to 50]

### Return type

[**ExecutionList**](ExecutionList.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## PostNodeExecutionCallback

> ExecutionCallbackResponse PostNodeExecutionCallback(ctx, id, execId).Authorization(authorization).ExecutionCallbackRequest(executionCallbackRequest).Execute()

Report an action-execution status advance from a Node.



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
	execId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Execution identifier (UUIDv7) the callback settles.
	authorization := "authorization_example" // string | `Bearer <NSK plaintext>` — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path `id`; a credential belonging to a different Node surfaces as 403 `nsk_node_mismatch`. 
	executionCallbackRequest := *openapiclient.NewExecutionCallbackRequest(openapiclient.ExecutionStatus("pending")) // ExecutionCallbackRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ActionsAPI.PostNodeExecutionCallback(context.Background(), id, execId).Authorization(authorization).ExecutionCallbackRequest(executionCallbackRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ActionsAPI.PostNodeExecutionCallback``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `PostNodeExecutionCallback`: ExecutionCallbackResponse
	fmt.Fprintf(os.Stdout, "Response from `ActionsAPI.PostNodeExecutionCallback`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**id** | **string** | Node identifier (UUIDv7) — the callback scope. | 
**execId** | **string** | Execution identifier (UUIDv7) the callback settles. | 

### Other Parameters

Other parameters are passed through a pointer to a apiPostNodeExecutionCallbackRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **authorization** | **string** | &#x60;Bearer &lt;NSK plaintext&gt;&#x60; — the per-Node Node Secret Key issued at registration time. The NSK is bound to the Node addressed by the path &#x60;id&#x60;; a credential belonging to a different Node surfaces as 403 &#x60;nsk_node_mismatch&#x60;.  | 
 **executionCallbackRequest** | [**ExecutionCallbackRequest**](ExecutionCallbackRequest.md) |  | 

### Return type

[**ExecutionCallbackResponse**](ExecutionCallbackResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

