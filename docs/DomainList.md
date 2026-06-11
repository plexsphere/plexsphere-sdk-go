# DomainList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]DomainResponse**](DomainResponse.md) | Domains in the current page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. &#x60;null&#x60; or omitted when the iteration has reached end-of-stream. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60; on the next call.  | [optional] 
**EmptyReason** | Pointer to [**DomainListEmptyReason**](DomainListEmptyReason.md) |  | [optional] 

## Methods

### NewDomainList

`func NewDomainList(items []DomainResponse, ) *DomainList`

NewDomainList instantiates a new DomainList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDomainListWithDefaults

`func NewDomainListWithDefaults() *DomainList`

NewDomainListWithDefaults instantiates a new DomainList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *DomainList) GetItems() []DomainResponse`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *DomainList) GetItemsOk() (*[]DomainResponse, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *DomainList) SetItems(v []DomainResponse)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *DomainList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *DomainList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *DomainList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *DomainList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.

### GetEmptyReason

`func (o *DomainList) GetEmptyReason() DomainListEmptyReason`

GetEmptyReason returns the EmptyReason field if non-nil, zero value otherwise.

### GetEmptyReasonOk

`func (o *DomainList) GetEmptyReasonOk() (*DomainListEmptyReason, bool)`

GetEmptyReasonOk returns a tuple with the EmptyReason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEmptyReason

`func (o *DomainList) SetEmptyReason(v DomainListEmptyReason)`

SetEmptyReason sets EmptyReason field to given value.

### HasEmptyReason

`func (o *DomainList) HasEmptyReason() bool`

HasEmptyReason returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


