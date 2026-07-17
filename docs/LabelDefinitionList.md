# LabelDefinitionList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]LabelDefinition**](LabelDefinition.md) |  | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. Omitted or empty when the iteration has reached end-of-stream.  | [optional] 

## Methods

### NewLabelDefinitionList

`func NewLabelDefinitionList(items []LabelDefinition, ) *LabelDefinitionList`

NewLabelDefinitionList instantiates a new LabelDefinitionList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelDefinitionListWithDefaults

`func NewLabelDefinitionListWithDefaults() *LabelDefinitionList`

NewLabelDefinitionListWithDefaults instantiates a new LabelDefinitionList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *LabelDefinitionList) GetItems() []LabelDefinition`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *LabelDefinitionList) GetItemsOk() (*[]LabelDefinition, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *LabelDefinitionList) SetItems(v []LabelDefinition)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *LabelDefinitionList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *LabelDefinitionList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *LabelDefinitionList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *LabelDefinitionList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


