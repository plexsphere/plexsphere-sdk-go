# ProjectSecretList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]ProjectSecretRef**](ProjectSecretRef.md) | Secret inventory entries in the current page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. &#x60;null&#x60; or omitted when the iteration has reached end-of-stream. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60; on the next call.  | [optional] 

## Methods

### NewProjectSecretList

`func NewProjectSecretList(items []ProjectSecretRef, ) *ProjectSecretList`

NewProjectSecretList instantiates a new ProjectSecretList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProjectSecretListWithDefaults

`func NewProjectSecretListWithDefaults() *ProjectSecretList`

NewProjectSecretListWithDefaults instantiates a new ProjectSecretList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *ProjectSecretList) GetItems() []ProjectSecretRef`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *ProjectSecretList) GetItemsOk() (*[]ProjectSecretRef, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *ProjectSecretList) SetItems(v []ProjectSecretRef)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *ProjectSecretList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *ProjectSecretList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *ProjectSecretList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *ProjectSecretList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


