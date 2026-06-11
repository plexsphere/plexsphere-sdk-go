# BlueprintList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]BlueprintResponse**](BlueprintResponse.md) | Blueprints in the current page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. &#x60;null&#x60; or omitted when the iteration has reached end-of-stream. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60; on the next call.  | [optional] 

## Methods

### NewBlueprintList

`func NewBlueprintList(items []BlueprintResponse, ) *BlueprintList`

NewBlueprintList instantiates a new BlueprintList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBlueprintListWithDefaults

`func NewBlueprintListWithDefaults() *BlueprintList`

NewBlueprintListWithDefaults instantiates a new BlueprintList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *BlueprintList) GetItems() []BlueprintResponse`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *BlueprintList) GetItemsOk() (*[]BlueprintResponse, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *BlueprintList) SetItems(v []BlueprintResponse)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *BlueprintList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *BlueprintList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *BlueprintList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *BlueprintList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


