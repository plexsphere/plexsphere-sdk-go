# SinkEnablementPage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]SinkEnablement**](SinkEnablement.md) | The sink enablements on this page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page, absent when the page is the last. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60; on the next call.  | [optional] 

## Methods

### NewSinkEnablementPage

`func NewSinkEnablementPage(items []SinkEnablement, ) *SinkEnablementPage`

NewSinkEnablementPage instantiates a new SinkEnablementPage object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkEnablementPageWithDefaults

`func NewSinkEnablementPageWithDefaults() *SinkEnablementPage`

NewSinkEnablementPageWithDefaults instantiates a new SinkEnablementPage object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *SinkEnablementPage) GetItems() []SinkEnablement`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *SinkEnablementPage) GetItemsOk() (*[]SinkEnablement, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *SinkEnablementPage) SetItems(v []SinkEnablement)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *SinkEnablementPage) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *SinkEnablementPage) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *SinkEnablementPage) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *SinkEnablementPage) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


