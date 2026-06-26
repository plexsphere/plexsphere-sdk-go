# CatalogBrowseResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]CatalogBlueprintSummary**](CatalogBlueprintSummary.md) | Blueprints the bundle offers, in slug order. | 

## Methods

### NewCatalogBrowseResponse

`func NewCatalogBrowseResponse(items []CatalogBlueprintSummary, ) *CatalogBrowseResponse`

NewCatalogBrowseResponse instantiates a new CatalogBrowseResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCatalogBrowseResponseWithDefaults

`func NewCatalogBrowseResponseWithDefaults() *CatalogBrowseResponse`

NewCatalogBrowseResponseWithDefaults instantiates a new CatalogBrowseResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *CatalogBrowseResponse) GetItems() []CatalogBlueprintSummary`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *CatalogBrowseResponse) GetItemsOk() (*[]CatalogBlueprintSummary, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *CatalogBrowseResponse) SetItems(v []CatalogBlueprintSummary)`

SetItems sets Items field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


