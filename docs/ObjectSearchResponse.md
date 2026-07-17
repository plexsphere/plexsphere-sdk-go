# ObjectSearchResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]ObjectSearchResultItem**](ObjectSearchResultItem.md) | Page of matched, access-checked object references. May be shorter than the requested &#x60;limit&#x60; because the ReBAC filter runs after pagination.  | 
**NextCursor** | Pointer to **string** | Opaque cursor for the next page, or empty when this is the last page.  | [optional] 
**CorrelationId** | **string** | Correlation id pairing this search with the matching audit entry emitted by &#x60;internal/audit&#x60;.  | 

## Methods

### NewObjectSearchResponse

`func NewObjectSearchResponse(items []ObjectSearchResultItem, correlationId string, ) *ObjectSearchResponse`

NewObjectSearchResponse instantiates a new ObjectSearchResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewObjectSearchResponseWithDefaults

`func NewObjectSearchResponseWithDefaults() *ObjectSearchResponse`

NewObjectSearchResponseWithDefaults instantiates a new ObjectSearchResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *ObjectSearchResponse) GetItems() []ObjectSearchResultItem`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *ObjectSearchResponse) GetItemsOk() (*[]ObjectSearchResultItem, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *ObjectSearchResponse) SetItems(v []ObjectSearchResultItem)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *ObjectSearchResponse) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *ObjectSearchResponse) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *ObjectSearchResponse) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *ObjectSearchResponse) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.

### GetCorrelationId

`func (o *ObjectSearchResponse) GetCorrelationId() string`

GetCorrelationId returns the CorrelationId field if non-nil, zero value otherwise.

### GetCorrelationIdOk

`func (o *ObjectSearchResponse) GetCorrelationIdOk() (*string, bool)`

GetCorrelationIdOk returns a tuple with the CorrelationId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCorrelationId

`func (o *ObjectSearchResponse) SetCorrelationId(v string)`

SetCorrelationId sets CorrelationId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


