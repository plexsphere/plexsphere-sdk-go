# ProjectList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]ProjectResponse**](ProjectResponse.md) | Projects in the current page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. &#x60;null&#x60; or omitted when the iteration has reached end-of-stream. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60; on the next call.  | [optional] 
**EmptyReason** | Pointer to [**ProjectListEmptyReason**](ProjectListEmptyReason.md) |  | [optional] 

## Methods

### NewProjectList

`func NewProjectList(items []ProjectResponse, ) *ProjectList`

NewProjectList instantiates a new ProjectList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProjectListWithDefaults

`func NewProjectListWithDefaults() *ProjectList`

NewProjectListWithDefaults instantiates a new ProjectList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *ProjectList) GetItems() []ProjectResponse`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *ProjectList) GetItemsOk() (*[]ProjectResponse, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *ProjectList) SetItems(v []ProjectResponse)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *ProjectList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *ProjectList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *ProjectList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *ProjectList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.

### GetEmptyReason

`func (o *ProjectList) GetEmptyReason() ProjectListEmptyReason`

GetEmptyReason returns the EmptyReason field if non-nil, zero value otherwise.

### GetEmptyReasonOk

`func (o *ProjectList) GetEmptyReasonOk() (*ProjectListEmptyReason, bool)`

GetEmptyReasonOk returns a tuple with the EmptyReason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEmptyReason

`func (o *ProjectList) SetEmptyReason(v ProjectListEmptyReason)`

SetEmptyReason sets EmptyReason field to given value.

### HasEmptyReason

`func (o *ProjectList) HasEmptyReason() bool`

HasEmptyReason returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


