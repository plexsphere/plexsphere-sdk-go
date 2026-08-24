# ProjectBlueprintList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]ProjectBlueprintOffer**](ProjectBlueprintOffer.md) | Blueprint offers in the current page. | 
**ReachableProviderKinds** | [**[]BlueprintVersionCreateRequestProviderKindsInner**](BlueprintVersionCreateRequestProviderKindsInner.md) | The substrates the Project reaches through its &#x60;approved&#x60; Cloud Assignments, deduplicated and sorted ascending. An empty array means the Project holds no approved assignment whose Cloud provider the correspondence knows, so every item is &#x60;provisionable: false&#x60;.  | 
**NextCursor** | Pointer to **string** | Continuation token for the next page. Absent when the iteration has reached end-of-stream. The encoding is HMAC-signed by the server so a tampered cursor surfaces as &#x60;400&#x60; on the next call.  | [optional] 

## Methods

### NewProjectBlueprintList

`func NewProjectBlueprintList(items []ProjectBlueprintOffer, reachableProviderKinds []BlueprintVersionCreateRequestProviderKindsInner, ) *ProjectBlueprintList`

NewProjectBlueprintList instantiates a new ProjectBlueprintList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProjectBlueprintListWithDefaults

`func NewProjectBlueprintListWithDefaults() *ProjectBlueprintList`

NewProjectBlueprintListWithDefaults instantiates a new ProjectBlueprintList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *ProjectBlueprintList) GetItems() []ProjectBlueprintOffer`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *ProjectBlueprintList) GetItemsOk() (*[]ProjectBlueprintOffer, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *ProjectBlueprintList) SetItems(v []ProjectBlueprintOffer)`

SetItems sets Items field to given value.


### GetReachableProviderKinds

`func (o *ProjectBlueprintList) GetReachableProviderKinds() []BlueprintVersionCreateRequestProviderKindsInner`

GetReachableProviderKinds returns the ReachableProviderKinds field if non-nil, zero value otherwise.

### GetReachableProviderKindsOk

`func (o *ProjectBlueprintList) GetReachableProviderKindsOk() (*[]BlueprintVersionCreateRequestProviderKindsInner, bool)`

GetReachableProviderKindsOk returns a tuple with the ReachableProviderKinds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReachableProviderKinds

`func (o *ProjectBlueprintList) SetReachableProviderKinds(v []BlueprintVersionCreateRequestProviderKindsInner)`

SetReachableProviderKinds sets ReachableProviderKinds field to given value.


### GetNextCursor

`func (o *ProjectBlueprintList) GetNextCursor() string`

GetNextCursor returns the NextCursor field if non-nil, zero value otherwise.

### GetNextCursorOk

`func (o *ProjectBlueprintList) GetNextCursorOk() (*string, bool)`

GetNextCursorOk returns a tuple with the NextCursor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNextCursor

`func (o *ProjectBlueprintList) SetNextCursor(v string)`

SetNextCursor sets NextCursor field to given value.

### HasNextCursor

`func (o *ProjectBlueprintList) HasNextCursor() bool`

HasNextCursor returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


