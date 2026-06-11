# BlueprintResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Blueprint identifier (UUIDv7). | 
**Slug** | **string** | Kebab-case URL handle, unique across the catalogue. | 
**DomainId** | Pointer to **string** | Owning Domain when the Blueprint is scoped to a single Domain. &#x60;null&#x60; when the entry is catalogue-wide.  | [optional] 
**DisplayName** | **string** | Human-readable Blueprint name. | 
**Description** | Pointer to **string** | Optional free-form Blueprint description. Empty when the catalogue entry declares none.  | [optional] 
**Status** | [**BlueprintResponseStatus**](BlueprintResponseStatus.md) |  | 
**CreatedAt** | **time.Time** | Blueprint creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). | 
**Versions** | [**[]BlueprintVersionResponse**](BlueprintVersionResponse.md) | Ordered Blueprint versions. Empty on the &#x60;ListBlueprints&#x60; projection; populated on &#x60;GetBlueprint&#x60;.  | 

## Methods

### NewBlueprintResponse

`func NewBlueprintResponse(id string, slug string, displayName string, status BlueprintResponseStatus, createdAt time.Time, updatedAt time.Time, versions []BlueprintVersionResponse, ) *BlueprintResponse`

NewBlueprintResponse instantiates a new BlueprintResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBlueprintResponseWithDefaults

`func NewBlueprintResponseWithDefaults() *BlueprintResponse`

NewBlueprintResponseWithDefaults instantiates a new BlueprintResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *BlueprintResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *BlueprintResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *BlueprintResponse) SetId(v string)`

SetId sets Id field to given value.


### GetSlug

`func (o *BlueprintResponse) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *BlueprintResponse) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *BlueprintResponse) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDomainId

`func (o *BlueprintResponse) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *BlueprintResponse) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *BlueprintResponse) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.

### HasDomainId

`func (o *BlueprintResponse) HasDomainId() bool`

HasDomainId returns a boolean if a field has been set.

### GetDisplayName

`func (o *BlueprintResponse) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *BlueprintResponse) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *BlueprintResponse) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetDescription

`func (o *BlueprintResponse) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *BlueprintResponse) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *BlueprintResponse) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *BlueprintResponse) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetStatus

`func (o *BlueprintResponse) GetStatus() BlueprintResponseStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *BlueprintResponse) GetStatusOk() (*BlueprintResponseStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *BlueprintResponse) SetStatus(v BlueprintResponseStatus)`

SetStatus sets Status field to given value.


### GetCreatedAt

`func (o *BlueprintResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *BlueprintResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *BlueprintResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *BlueprintResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *BlueprintResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *BlueprintResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.


### GetVersions

`func (o *BlueprintResponse) GetVersions() []BlueprintVersionResponse`

GetVersions returns the Versions field if non-nil, zero value otherwise.

### GetVersionsOk

`func (o *BlueprintResponse) GetVersionsOk() (*[]BlueprintVersionResponse, bool)`

GetVersionsOk returns a tuple with the Versions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersions

`func (o *BlueprintResponse) SetVersions(v []BlueprintVersionResponse)`

SetVersions sets Versions field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


