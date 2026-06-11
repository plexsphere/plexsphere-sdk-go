# BootstrapTokenList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]BootstrapTokenMetadata**](BootstrapTokenMetadata.md) | BootstrapToken metadata in the current page. | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. Null or omitted when the iteration has reached end-of-stream.  | [optional] 

## Methods

### NewBootstrapTokenList

`func NewBootstrapTokenList(items []BootstrapTokenMetadata, ) *BootstrapTokenList`

NewBootstrapTokenList instantiates a new BootstrapTokenList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBootstrapTokenListWithDefaults

`func NewBootstrapTokenListWithDefaults() *BootstrapTokenList`

NewBootstrapTokenListWithDefaults instantiates a new BootstrapTokenList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *BootstrapTokenList) GetItems() []BootstrapTokenMetadata`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *BootstrapTokenList) GetItemsOk() (*[]BootstrapTokenMetadata, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *BootstrapTokenList) SetItems(v []BootstrapTokenMetadata)`

SetItems sets Items field to given value.


### GetNextCursor

`func (o *BootstrapTokenList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *BootstrapTokenList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *BootstrapTokenList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *BootstrapTokenList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


