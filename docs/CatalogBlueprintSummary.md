# CatalogBlueprintSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Slug** | **string** | Kebab-case URL handle the Blueprint imports under. | 
**DisplayName** | **string** | Human-readable Blueprint name from the bundle metadata. | 
**Description** | Pointer to **string** | Optional free-form description from the bundle metadata. | [optional] 
**Version** | **string** | The version label the bundle offers for this Blueprint. | 
**ProviderKinds** | **[]string** | Infrastructure substrates the offered version targets, as declared in the bundle metadata.  | 
**InjectionStrategy** | **string** | How the offered version threads request parameters into the rendered Composite Resource, as declared in the bundle metadata.  | 

## Methods

### NewCatalogBlueprintSummary

`func NewCatalogBlueprintSummary(slug string, displayName string, version string, providerKinds []string, injectionStrategy string, ) *CatalogBlueprintSummary`

NewCatalogBlueprintSummary instantiates a new CatalogBlueprintSummary object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCatalogBlueprintSummaryWithDefaults

`func NewCatalogBlueprintSummaryWithDefaults() *CatalogBlueprintSummary`

NewCatalogBlueprintSummaryWithDefaults instantiates a new CatalogBlueprintSummary object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSlug

`func (o *CatalogBlueprintSummary) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *CatalogBlueprintSummary) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *CatalogBlueprintSummary) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *CatalogBlueprintSummary) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *CatalogBlueprintSummary) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *CatalogBlueprintSummary) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetDescription

`func (o *CatalogBlueprintSummary) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *CatalogBlueprintSummary) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *CatalogBlueprintSummary) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *CatalogBlueprintSummary) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetVersion

`func (o *CatalogBlueprintSummary) GetVersion() string`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *CatalogBlueprintSummary) GetVersionOk() (*string, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *CatalogBlueprintSummary) SetVersion(v string)`

SetVersion sets Version field to given value.


### GetProviderKinds

`func (o *CatalogBlueprintSummary) GetProviderKinds() []string`

GetProviderKinds returns the ProviderKinds field if non-nil, zero value otherwise.

### GetProviderKindsOk

`func (o *CatalogBlueprintSummary) GetProviderKindsOk() (*[]string, bool)`

GetProviderKindsOk returns a tuple with the ProviderKinds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderKinds

`func (o *CatalogBlueprintSummary) SetProviderKinds(v []string)`

SetProviderKinds sets ProviderKinds field to given value.


### GetInjectionStrategy

`func (o *CatalogBlueprintSummary) GetInjectionStrategy() string`

GetInjectionStrategy returns the InjectionStrategy field if non-nil, zero value otherwise.

### GetInjectionStrategyOk

`func (o *CatalogBlueprintSummary) GetInjectionStrategyOk() (*string, bool)`

GetInjectionStrategyOk returns a tuple with the InjectionStrategy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInjectionStrategy

`func (o *CatalogBlueprintSummary) SetInjectionStrategy(v string)`

SetInjectionStrategy sets InjectionStrategy field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


