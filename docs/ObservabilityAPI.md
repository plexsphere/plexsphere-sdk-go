# \ObservabilityAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AppendIncidentEvent**](ObservabilityAPI.md#AppendIncidentEvent) | **Post** /v1/domains/{domain_id}/incidents/{incident_id}/events | Append an event to an incident&#39;s timeline.
[**CreateAlertRule**](ObservabilityAPI.md#CreateAlertRule) | **Post** /v1/domains/{domain_id}/alert-rules | Store a new alert rule for a Domain.
[**DeleteAlertRule**](ObservabilityAPI.md#DeleteAlertRule) | **Delete** /v1/domains/{domain_id}/alert-rules/{alert_rule_id} | Delete a stored alert rule.
[**GetAlertRule**](ObservabilityAPI.md#GetAlertRule) | **Get** /v1/domains/{domain_id}/alert-rules/{alert_rule_id} | Read a single stored alert rule.
[**GetIncident**](ObservabilityAPI.md#GetIncident) | **Get** /v1/domains/{domain_id}/incidents/{incident_id} | Read a single incident with its ordered timeline.
[**ListAlertRules**](ObservabilityAPI.md#ListAlertRules) | **Get** /v1/domains/{domain_id}/alert-rules | List the stored alert rules for a Domain.
[**ListIncidents**](ObservabilityAPI.md#ListIncidents) | **Get** /v1/domains/{domain_id}/incidents | List the incidents for a Domain.
[**OpenIncident**](ObservabilityAPI.md#OpenIncident) | **Post** /v1/domains/{domain_id}/incidents | Open a new incident for a Domain.
[**QueryDomainLogs**](ObservabilityAPI.md#QueryDomainLogs) | **Get** /v1/domains/{domain_id}/logs/query | Run a read-only LogQL logs query for a Domain.
[**QueryDomainMetrics**](ObservabilityAPI.md#QueryDomainMetrics) | **Get** /v1/domains/{domain_id}/metrics/query | Run a read-only PromQL metrics query for a Domain.
[**ResolveIncident**](ObservabilityAPI.md#ResolveIncident) | **Post** /v1/domains/{domain_id}/incidents/{incident_id}/resolve | Resolve an open incident.
[**UpdateAlertRule**](ObservabilityAPI.md#UpdateAlertRule) | **Patch** /v1/domains/{domain_id}/alert-rules/{alert_rule_id} | Update mutable fields on a stored alert rule.



## AppendIncidentEvent

> TimelineEvent AppendIncidentEvent(ctx, domainId, incidentId).TimelineEventAppend(timelineEventAppend).Execute()

Append an event to an incident's timeline.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	incidentId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Incident identifier (UUIDv7). Bound on `/v1/domains/{domain_id}/incidents/{incident_id}`, its `/events` sub-resource, and its `:resolve` sub-resource. 
	timelineEventAppend := *openapiclient.NewTimelineEventAppend(openapiclient.TimelineEventKind("note"), "Message_example") // TimelineEventAppend | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.AppendIncidentEvent(context.Background(), domainId, incidentId).TimelineEventAppend(timelineEventAppend).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.AppendIncidentEvent``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `AppendIncidentEvent`: TimelineEvent
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.AppendIncidentEvent`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 
**incidentId** | **string** | Incident identifier (UUIDv7). Bound on &#x60;/v1/domains/{domain_id}/incidents/{incident_id}&#x60;, its &#x60;/events&#x60; sub-resource, and its &#x60;:resolve&#x60; sub-resource.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiAppendIncidentEventRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **timelineEventAppend** | [**TimelineEventAppend**](TimelineEventAppend.md) |  | 

### Return type

[**TimelineEvent**](TimelineEvent.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## CreateAlertRule

> AlertRule CreateAlertRule(ctx, domainId).AlertRuleCreate(alertRuleCreate).Execute()

Store a new alert rule for a Domain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	alertRuleCreate := *openapiclient.NewAlertRuleCreate("Name_example", "Signal_example", openapiclient.AlertComparator("gt"), float64(123), openapiclient.AlertSeverity("info")) // AlertRuleCreate | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.CreateAlertRule(context.Background(), domainId).AlertRuleCreate(alertRuleCreate).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.CreateAlertRule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `CreateAlertRule`: AlertRule
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.CreateAlertRule`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiCreateAlertRuleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **alertRuleCreate** | [**AlertRuleCreate**](AlertRuleCreate.md) |  | 

### Return type

[**AlertRule**](AlertRule.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## DeleteAlertRule

> DeleteAlertRule(ctx, domainId, alertRuleId).Execute()

Delete a stored alert rule.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	alertRuleId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Alert rule identifier (UUIDv7). Bound on `/v1/domains/{domain_id}/alert-rules/{alert_rule_id}` for the single-rule read, update, and delete. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	r, err := apiClient.ObservabilityAPI.DeleteAlertRule(context.Background(), domainId, alertRuleId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.DeleteAlertRule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 
**alertRuleId** | **string** | Alert rule identifier (UUIDv7). Bound on &#x60;/v1/domains/{domain_id}/alert-rules/{alert_rule_id}&#x60; for the single-rule read, update, and delete.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiDeleteAlertRuleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

 (empty response body)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetAlertRule

> AlertRule GetAlertRule(ctx, domainId, alertRuleId).Execute()

Read a single stored alert rule.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	alertRuleId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Alert rule identifier (UUIDv7). Bound on `/v1/domains/{domain_id}/alert-rules/{alert_rule_id}` for the single-rule read, update, and delete. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.GetAlertRule(context.Background(), domainId, alertRuleId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.GetAlertRule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetAlertRule`: AlertRule
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.GetAlertRule`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 
**alertRuleId** | **string** | Alert rule identifier (UUIDv7). Bound on &#x60;/v1/domains/{domain_id}/alert-rules/{alert_rule_id}&#x60; for the single-rule read, update, and delete.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetAlertRuleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**AlertRule**](AlertRule.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetIncident

> Incident GetIncident(ctx, domainId, incidentId).Execute()

Read a single incident with its ordered timeline.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	incidentId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Incident identifier (UUIDv7). Bound on `/v1/domains/{domain_id}/incidents/{incident_id}`, its `/events` sub-resource, and its `:resolve` sub-resource. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.GetIncident(context.Background(), domainId, incidentId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.GetIncident``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetIncident`: Incident
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.GetIncident`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 
**incidentId** | **string** | Incident identifier (UUIDv7). Bound on &#x60;/v1/domains/{domain_id}/incidents/{incident_id}&#x60;, its &#x60;/events&#x60; sub-resource, and its &#x60;:resolve&#x60; sub-resource.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiGetIncidentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**Incident**](Incident.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListAlertRules

> AlertRuleList ListAlertRules(ctx, domainId).Cursor(cursor).Limit(limit).Execute()

List the stored alert rules for a Domain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. A value outside [1, 200] is rejected with a `400` Problem rather than silently clamped.  (optional) (default to 50)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.ListAlertRules(context.Background(), domainId).Cursor(cursor).Limit(limit).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.ListAlertRules``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListAlertRules`: AlertRuleList
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.ListAlertRules`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListAlertRulesRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. A value outside [1, 200] is rejected with a &#x60;400&#x60; Problem rather than silently clamped.  | [default to 50]

### Return type

[**AlertRuleList**](AlertRuleList.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListIncidents

> IncidentList ListIncidents(ctx, domainId).Cursor(cursor).Limit(limit).Status(status).Execute()

List the incidents for a Domain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	cursor := "cursor_example" // string | Opaque continuation token returned by a previous call's `next_cursor`. The encoding is HMAC-signed by the server so a tampered cursor surfaces as `400`.  (optional)
	limit := int32(56) // int32 | Maximum number of items to return in a single page. A value outside [1, 200] is rejected with a `400` Problem rather than silently clamped.  (optional) (default to 50)
	status := openapiclient.IncidentStatus("open") // IncidentStatus | Optional status filter so the Dashboard can show only open or only resolved incidents.  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.ListIncidents(context.Background(), domainId).Cursor(cursor).Limit(limit).Status(status).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.ListIncidents``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ListIncidents`: IncidentList
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.ListIncidents`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiListIncidentsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **cursor** | **string** | Opaque continuation token returned by a previous call&#39;s &#x60;next_cursor&#x60;. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60;.  | 
 **limit** | **int32** | Maximum number of items to return in a single page. A value outside [1, 200] is rejected with a &#x60;400&#x60; Problem rather than silently clamped.  | [default to 50]
 **status** | [**IncidentStatus**](IncidentStatus.md) | Optional status filter so the Dashboard can show only open or only resolved incidents.  | 

### Return type

[**IncidentList**](IncidentList.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## OpenIncident

> Incident OpenIncident(ctx, domainId).IncidentOpenRequest(incidentOpenRequest).Execute()

Open a new incident for a Domain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	incidentOpenRequest := *openapiclient.NewIncidentOpenRequest("Title_example", openapiclient.IncidentSeverity("info")) // IncidentOpenRequest | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.OpenIncident(context.Background(), domainId).IncidentOpenRequest(incidentOpenRequest).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.OpenIncident``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `OpenIncident`: Incident
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.OpenIncident`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiOpenIncidentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **incidentOpenRequest** | [**IncidentOpenRequest**](IncidentOpenRequest.md) |  | 

### Return type

[**Incident**](Incident.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## QueryDomainLogs

> LogsQueryResult QueryDomainLogs(ctx, domainId).Query(query).Start(start).End(end).Limit(limit).Direction(direction).NodeId(nodeId).Execute()

Run a read-only LogQL logs query for a Domain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	query := "query_example" // string | The LogQL expression to evaluate. Capped at 4096 characters; an empty or oversized expression is rejected with 400. 
	start := time.Now() // time.Time | Inclusive lower bound of the query window (RFC 3339). `end` must be after `start` and the window may span at most 31 days. 
	end := time.Now() // time.Time | Inclusive upper bound of the query window (RFC 3339), strictly after `start`. 
	limit := int32(56) // int32 | Maximum number of log lines to return. Clamped server-side to protect the logs store from an unbounded read.  (optional) (default to 100)
	direction := openapiclient.QueryDomainLogs_direction_parameter("forward") // QueryDomainLogsDirectionParameter | Scan order: `backward` returns the newest lines first, `forward` the oldest first.  (optional) (default to "backward")
	nodeId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional Node hint for a single-Node drill-down. NOTE: this filter is accepted but NOT yet applied — splicing a per-Node label selector into an arbitrary caller-supplied LogQL expression safely requires parsing the query AST, which is a deferred enhancement. The Domain tenant boundary IS enforced regardless; until Node scoping lands, a present `nodeId` does not narrow the result to that Node.  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.QueryDomainLogs(context.Background(), domainId).Query(query).Start(start).End(end).Limit(limit).Direction(direction).NodeId(nodeId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.QueryDomainLogs``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `QueryDomainLogs`: LogsQueryResult
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.QueryDomainLogs`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiQueryDomainLogsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **query** | **string** | The LogQL expression to evaluate. Capped at 4096 characters; an empty or oversized expression is rejected with 400.  | 
 **start** | **time.Time** | Inclusive lower bound of the query window (RFC 3339). &#x60;end&#x60; must be after &#x60;start&#x60; and the window may span at most 31 days.  | 
 **end** | **time.Time** | Inclusive upper bound of the query window (RFC 3339), strictly after &#x60;start&#x60;.  | 
 **limit** | **int32** | Maximum number of log lines to return. Clamped server-side to protect the logs store from an unbounded read.  | [default to 100]
 **direction** | [**QueryDomainLogsDirectionParameter**](QueryDomainLogsDirectionParameter.md) | Scan order: &#x60;backward&#x60; returns the newest lines first, &#x60;forward&#x60; the oldest first.  | [default to &quot;backward&quot;]
 **nodeId** | **string** | Optional Node hint for a single-Node drill-down. NOTE: this filter is accepted but NOT yet applied — splicing a per-Node label selector into an arbitrary caller-supplied LogQL expression safely requires parsing the query AST, which is a deferred enhancement. The Domain tenant boundary IS enforced regardless; until Node scoping lands, a present &#x60;nodeId&#x60; does not narrow the result to that Node.  | 

### Return type

[**LogsQueryResult**](LogsQueryResult.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## QueryDomainMetrics

> MetricsQueryResult QueryDomainMetrics(ctx, domainId).Query(query).Time(time).Start(start).End(end).Step(step).NodeId(nodeId).Execute()

Run a read-only PromQL metrics query for a Domain.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	query := "query_example" // string | The PromQL expression to evaluate. Capped at 4096 characters; an empty or oversized expression is rejected with 400. 
	time := time.Now() // time.Time | Evaluation instant for an instant query (RFC 3339). When present the handler runs an instant query and ignores `start` / `end` / `step`; when absent the handler runs a range query and requires `start`, `end`, and `step`.  (optional)
	start := time.Now() // time.Time | Inclusive lower bound of the range-query window (RFC 3339). Required for a range query; `end` must be after `start` and the window may span at most 31 days.  (optional)
	end := time.Now() // time.Time | Inclusive upper bound of the range-query window (RFC 3339). Required for a range query and must be after `start`.  (optional)
	step := "step_example" // string | Range-query resolution step expressed as a duration (for example `30s`, `5m`). Required for a range query and ignored for an instant query.  (optional)
	nodeId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Optional Node hint for a single-Node drill-down. NOTE: this filter is accepted but NOT yet applied — splicing a per-Node label selector into an arbitrary caller-supplied PromQL expression safely requires parsing the query AST, which is a deferred enhancement. The Domain tenant boundary IS enforced regardless (see the operation description); until Node scoping lands, a present `nodeId` does not narrow the result to that Node.  (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.QueryDomainMetrics(context.Background(), domainId).Query(query).Time(time).Start(start).End(end).Step(step).NodeId(nodeId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.QueryDomainMetrics``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `QueryDomainMetrics`: MetricsQueryResult
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.QueryDomainMetrics`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiQueryDomainMetricsRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **query** | **string** | The PromQL expression to evaluate. Capped at 4096 characters; an empty or oversized expression is rejected with 400.  | 
 **time** | **time.Time** | Evaluation instant for an instant query (RFC 3339). When present the handler runs an instant query and ignores &#x60;start&#x60; / &#x60;end&#x60; / &#x60;step&#x60;; when absent the handler runs a range query and requires &#x60;start&#x60;, &#x60;end&#x60;, and &#x60;step&#x60;.  | 
 **start** | **time.Time** | Inclusive lower bound of the range-query window (RFC 3339). Required for a range query; &#x60;end&#x60; must be after &#x60;start&#x60; and the window may span at most 31 days.  | 
 **end** | **time.Time** | Inclusive upper bound of the range-query window (RFC 3339). Required for a range query and must be after &#x60;start&#x60;.  | 
 **step** | **string** | Range-query resolution step expressed as a duration (for example &#x60;30s&#x60;, &#x60;5m&#x60;). Required for a range query and ignored for an instant query.  | 
 **nodeId** | **string** | Optional Node hint for a single-Node drill-down. NOTE: this filter is accepted but NOT yet applied — splicing a per-Node label selector into an arbitrary caller-supplied PromQL expression safely requires parsing the query AST, which is a deferred enhancement. The Domain tenant boundary IS enforced regardless (see the operation description); until Node scoping lands, a present &#x60;nodeId&#x60; does not narrow the result to that Node.  | 

### Return type

[**MetricsQueryResult**](MetricsQueryResult.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ResolveIncident

> Incident ResolveIncident(ctx, domainId, incidentId).Execute()

Resolve an open incident.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	incidentId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Incident identifier (UUIDv7). Bound on `/v1/domains/{domain_id}/incidents/{incident_id}`, its `/events` sub-resource, and its `:resolve` sub-resource. 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.ResolveIncident(context.Background(), domainId, incidentId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.ResolveIncident``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `ResolveIncident`: Incident
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.ResolveIncident`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 
**incidentId** | **string** | Incident identifier (UUIDv7). Bound on &#x60;/v1/domains/{domain_id}/incidents/{incident_id}&#x60;, its &#x60;/events&#x60; sub-resource, and its &#x60;:resolve&#x60; sub-resource.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiResolveIncidentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------



### Return type

[**Incident**](Incident.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## UpdateAlertRule

> AlertRule UpdateAlertRule(ctx, domainId, alertRuleId).AlertRuleUpdate(alertRuleUpdate).Execute()

Update mutable fields on a stored alert rule.



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
	domainId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents. 
	alertRuleId := "38400000-8cf0-11bd-b23e-10b96e4ef00d" // string | Alert rule identifier (UUIDv7). Bound on `/v1/domains/{domain_id}/alert-rules/{alert_rule_id}` for the single-rule read, update, and delete. 
	alertRuleUpdate := *openapiclient.NewAlertRuleUpdate() // AlertRuleUpdate | 

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.ObservabilityAPI.UpdateAlertRule(context.Background(), domainId, alertRuleId).AlertRuleUpdate(alertRuleUpdate).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `ObservabilityAPI.UpdateAlertRule``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `UpdateAlertRule`: AlertRule
	fmt.Fprintf(os.Stdout, "Response from `ObservabilityAPI.UpdateAlertRule`: %v\n", resp)
}
```

### Path Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**domainId** | **string** | Owning Domain identifier (UUIDv7). Bound on the Domain-scoped operator surfaces — capacity, mesh topology, managed-push, observability queries, alert rules, and incidents.  | 
**alertRuleId** | **string** | Alert rule identifier (UUIDv7). Bound on &#x60;/v1/domains/{domain_id}/alert-rules/{alert_rule_id}&#x60; for the single-rule read, update, and delete.  | 

### Other Parameters

Other parameters are passed through a pointer to a apiUpdateAlertRuleRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------


 **alertRuleUpdate** | [**AlertRuleUpdate**](AlertRuleUpdate.md) |  | 

### Return type

[**AlertRule**](AlertRule.md)

### Authorization

[operatorBearer](../README.md#operatorBearer), [sessionCookie](../README.md#sessionCookie)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

