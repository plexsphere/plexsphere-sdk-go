# PolicyRevisionListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]PolicyRevision**](PolicyRevision.md) |  | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. &#x60;null&#x60; or omitted when the iteration has reached end-of-stream.  | [optional] 

## Methods

### NewPolicyRevisionListResponse

`func NewPolicyRevisionListResponse(items []PolicyRevision, ) *PolicyRevisionListResponse`

NewPolicyRevisionListResponse instantiates a new PolicyRevisionListResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyRevisionListResponseWithDefaults

`func NewPolicyRevisionListResponseWithDefaults() *PolicyRevisionListResponse`

NewPolicyRevisionListResponseWithDefaults instantiates a new PolicyRevisionListResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *PolicyRevisionListResponse) GetItems() []PolicyRevision`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *PolicyRevisionListResponse) GetItemsOk() (*[]PolicyRevision, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *PolicyRevisionListResponse) SetItems(v []PolicyRevision)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *PolicyRevisionListResponse) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *PolicyRevisionListResponse) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *PolicyRevisionListResponse) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *PolicyRevisionListResponse) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


