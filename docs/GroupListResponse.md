# GroupListResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]GroupResponse**](GroupResponse.md) | Groups in the current page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. Omitted or empty when the iteration has reached end-of-stream .  | [optional] 

## Methods

### NewGroupListResponse

`func NewGroupListResponse(items []GroupResponse, ) *GroupListResponse`

NewGroupListResponse instantiates a new GroupListResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupListResponseWithDefaults

`func NewGroupListResponseWithDefaults() *GroupListResponse`

NewGroupListResponseWithDefaults instantiates a new GroupListResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *GroupListResponse) GetItems() []GroupResponse`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *GroupListResponse) GetItemsOk() (*[]GroupResponse, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *GroupListResponse) SetItems(v []GroupResponse)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *GroupListResponse) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *GroupListResponse) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *GroupListResponse) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *GroupListResponse) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


