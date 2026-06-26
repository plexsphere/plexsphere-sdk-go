# BlueprintCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Slug** | **string** | Kebab-case URL handle, unique across the catalogue. The aggregate&#39;s &#x60;ParseSlug&#x60; enforces the same regex; surfacing the pattern here lets the generated client validate before the round-trip.  | 
**DisplayName** | **string** | Human-readable Blueprint name. Whitespace-only is rejected. | 
**Description** | Pointer to **string** | Optional free-form Blueprint description. | [optional] 
**DomainId** | Pointer to **string** | Owning Domain when the Blueprint is scoped to a single Domain. Omit or &#x60;null&#x60; for a catalogue-wide entry.  | [optional] 

## Methods

### NewBlueprintCreateRequest

`func NewBlueprintCreateRequest(slug string, displayName string, ) *BlueprintCreateRequest`

NewBlueprintCreateRequest instantiates a new BlueprintCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBlueprintCreateRequestWithDefaults

`func NewBlueprintCreateRequestWithDefaults() *BlueprintCreateRequest`

NewBlueprintCreateRequestWithDefaults instantiates a new BlueprintCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSlug

`func (o *BlueprintCreateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *BlueprintCreateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *BlueprintCreateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *BlueprintCreateRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *BlueprintCreateRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *BlueprintCreateRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetDescription

`func (o *BlueprintCreateRequest) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *BlueprintCreateRequest) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *BlueprintCreateRequest) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *BlueprintCreateRequest) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetDomainId

`func (o *BlueprintCreateRequest) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *BlueprintCreateRequest) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *BlueprintCreateRequest) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.

### HasDomainId

`func (o *BlueprintCreateRequest) HasDomainId() bool`

HasDomainId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


