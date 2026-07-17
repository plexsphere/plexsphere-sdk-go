# GroupList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]GroupResponse**](GroupResponse.md) | Groups in the current page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. Omitted or empty when the iteration has reached end-of-stream.  | [optional] 

## Methods

### NewGroupList

`func NewGroupList(items []GroupResponse, ) *GroupList`

NewGroupList instantiates a new GroupList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupListWithDefaults

`func NewGroupListWithDefaults() *GroupList`

NewGroupListWithDefaults instantiates a new GroupList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *GroupList) GetItems() []GroupResponse`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *GroupList) GetItemsOk() (*[]GroupResponse, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *GroupList) SetItems(v []GroupResponse)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *GroupList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *GroupList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *GroupList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *GroupList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


