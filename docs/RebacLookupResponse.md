# RebacLookupResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | **[]string** | Full materialised set of object references the lookup resolved (&#x60;&lt;type&gt;:&lt;id&gt;&#x60;). Ordering is the authorizer&#39;s insertion order; callers that need a stable order MUST sort client-side.  | 
**CorrelationId** | **string** | Correlation id that pairs this lookup with the matching audit entry emitted by &#x60;internal/audit&#x60;.  | 

## Methods

### NewRebacLookupResponse

`func NewRebacLookupResponse(items []string, correlationId string, ) *RebacLookupResponse`

NewRebacLookupResponse instantiates a new RebacLookupResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRebacLookupResponseWithDefaults

`func NewRebacLookupResponseWithDefaults() *RebacLookupResponse`

NewRebacLookupResponseWithDefaults instantiates a new RebacLookupResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *RebacLookupResponse) GetItems() []string`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *RebacLookupResponse) GetItemsOk() (*[]string, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *RebacLookupResponse) SetItems(v []string)`

SetItems sets Items field to given value.


### GetCorrelationId

`func (o *RebacLookupResponse) GetCorrelationId() string`

GetCorrelationId returns the CorrelationId field if non-nil, zero value otherwise.

### GetCorrelationIdOk

`func (o *RebacLookupResponse) GetCorrelationIdOk() (*string, bool)`

GetCorrelationIdOk returns a tuple with the CorrelationId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCorrelationId

`func (o *RebacLookupResponse) SetCorrelationId(v string)`

SetCorrelationId sets CorrelationId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


