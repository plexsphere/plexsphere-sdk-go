# ProjectBlueprintOffer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Blueprint identifier (UUIDv7). | 
**Slug** | **string** | Kebab-case URL handle, unique across the catalogue. | 
**DisplayName** | **string** | Human-readable Blueprint name. | 
**Description** | Pointer to **string** | Optional free-form Blueprint description. Absent when the catalogue entry declares none.  | [optional] 
**Status** | [**BlueprintResponseStatus**](BlueprintResponseStatus.md) |  | 
**ProviderKinds** | [**[]BlueprintVersionCreateRequestProviderKindsInner**](BlueprintVersionCreateRequestProviderKindsInner.md) | Union of the substrates the Blueprint&#39;s published versions accept, deduplicated and sorted ascending. Empty when the Blueprint has no published version, which also makes &#x60;provisionable&#x60; false.  | 
**Provisionable** | **bool** | True when &#x60;provider_kinds&#x60; intersects the Project&#39;s &#x60;reachable_provider_kinds&#x60;. The verdict is assignment-level: it does not promise an assigned credential for the matching Cloud.  | 
**CreatedAt** | **time.Time** | Blueprint creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). | 

## Methods

### NewProjectBlueprintOffer

`func NewProjectBlueprintOffer(id string, slug string, displayName string, status BlueprintResponseStatus, providerKinds []BlueprintVersionCreateRequestProviderKindsInner, provisionable bool, createdAt time.Time, updatedAt time.Time, ) *ProjectBlueprintOffer`

NewProjectBlueprintOffer instantiates a new ProjectBlueprintOffer object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProjectBlueprintOfferWithDefaults

`func NewProjectBlueprintOfferWithDefaults() *ProjectBlueprintOffer`

NewProjectBlueprintOfferWithDefaults instantiates a new ProjectBlueprintOffer object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *ProjectBlueprintOffer) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *ProjectBlueprintOffer) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *ProjectBlueprintOffer) SetId(v string)`

SetId sets Id field to given value.


### GetSlug

`func (o *ProjectBlueprintOffer) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *ProjectBlueprintOffer) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *ProjectBlueprintOffer) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *ProjectBlueprintOffer) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *ProjectBlueprintOffer) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *ProjectBlueprintOffer) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetDescription

`func (o *ProjectBlueprintOffer) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *ProjectBlueprintOffer) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *ProjectBlueprintOffer) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *ProjectBlueprintOffer) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetStatus

`func (o *ProjectBlueprintOffer) GetStatus() BlueprintResponseStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *ProjectBlueprintOffer) GetStatusOk() (*BlueprintResponseStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *ProjectBlueprintOffer) SetStatus(v BlueprintResponseStatus)`

SetStatus sets Status field to given value.


### GetProviderKinds

`func (o *ProjectBlueprintOffer) GetProviderKinds() []BlueprintVersionCreateRequestProviderKindsInner`

GetProviderKinds returns the ProviderKinds field if non-nil, zero value otherwise.

### GetProviderKindsOk

`func (o *ProjectBlueprintOffer) GetProviderKindsOk() (*[]BlueprintVersionCreateRequestProviderKindsInner, bool)`

GetProviderKindsOk returns a tuple with the ProviderKinds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderKinds

`func (o *ProjectBlueprintOffer) SetProviderKinds(v []BlueprintVersionCreateRequestProviderKindsInner)`

SetProviderKinds sets ProviderKinds field to given value.


### GetProvisionable

`func (o *ProjectBlueprintOffer) GetProvisionable() bool`

GetProvisionable returns the Provisionable field if non-nil, zero value otherwise.

### GetProvisionableOk

`func (o *ProjectBlueprintOffer) GetProvisionableOk() (*bool, bool)`

GetProvisionableOk returns a tuple with the Provisionable field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProvisionable

`func (o *ProjectBlueprintOffer) SetProvisionable(v bool)`

SetProvisionable sets Provisionable field to given value.


### GetCreatedAt

`func (o *ProjectBlueprintOffer) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *ProjectBlueprintOffer) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *ProjectBlueprintOffer) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *ProjectBlueprintOffer) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *ProjectBlueprintOffer) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *ProjectBlueprintOffer) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


