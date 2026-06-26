# \BackupAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetBackupCatalog**](BackupAPI.md#GetBackupCatalog) | **Get** /v1/platform/backup/catalog | Return the backup coverage catalog.
[**GetBackupRestorePlan**](BackupAPI.md#GetBackupRestorePlan) | **Get** /v1/platform/backup/restore-plan | Return the ordered disaster-recovery restore plan.



## GetBackupCatalog

> BackupCatalog GetBackupCatalog(ctx).Execute()

Return the backup coverage catalog.



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
	resp, r, err := apiClient.BackupAPI.GetBackupCatalog(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BackupAPI.GetBackupCatalog``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBackupCatalog`: BackupCatalog
	fmt.Fprintf(os.Stdout, "Response from `BackupAPI.GetBackupCatalog`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiGetBackupCatalogRequest struct via the builder pattern


### Return type

[**BackupCatalog**](BackupCatalog.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetBackupRestorePlan

> RestorePlan GetBackupRestorePlan(ctx).Execute()

Return the ordered disaster-recovery restore plan.



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
	resp, r, err := apiClient.BackupAPI.GetBackupRestorePlan(context.Background()).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `BackupAPI.GetBackupRestorePlan``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetBackupRestorePlan`: RestorePlan
	fmt.Fprintf(os.Stdout, "Response from `BackupAPI.GetBackupRestorePlan`: %v\n", resp)
}
```

### Path Parameters

This endpoint does not need any parameter.

### Other Parameters

Other parameters are passed through a pointer to a apiGetBackupRestorePlanRequest struct via the builder pattern


### Return type

[**RestorePlan**](RestorePlan.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

