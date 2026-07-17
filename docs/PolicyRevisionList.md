# PolicyRevisionList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]PolicyRevision**](PolicyRevision.md) |  | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. Absent when the iteration has reached end-of-stream.  | [optional] 

## Methods

### NewPolicyRevisionList

`func NewPolicyRevisionList(items []PolicyRevision, ) *PolicyRevisionList`

NewPolicyRevisionList instantiates a new PolicyRevisionList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyRevisionListWithDefaults

`func NewPolicyRevisionListWithDefaults() *PolicyRevisionList`

NewPolicyRevisionListWithDefaults instantiates a new PolicyRevisionList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *PolicyRevisionList) GetItems() []PolicyRevision`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *PolicyRevisionList) GetItemsOk() (*[]PolicyRevision, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *PolicyRevisionList) SetItems(v []PolicyRevision)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *PolicyRevisionList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *PolicyRevisionList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *PolicyRevisionList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *PolicyRevisionList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


