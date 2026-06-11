# GroupResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Group identifier (UUIDv7). | 
**DomainId** | **string** | Owning Domain. | 
**Slug** | **string** | URL-safe identifier unique within &#x60;domain_id&#x60; .  | 
**DisplayName** | **string** | Human-friendly Group name. | 
**Source** | [**GroupResponseSource**](GroupResponseSource.md) |  | 
**IdpBindingId** | Pointer to **string** | IdP binding the Group is reconciled from. Present only when &#x60;source&#x3D;idp&#x60;.  | [optional] 
**IdpClaimValue** | Pointer to **string** | Verbatim IdP claim value. Present only when &#x60;source&#x3D;idp&#x60; .  | [optional] 
**CreatedAt** | **time.Time** |  | 
**UpdatedAt** | **time.Time** |  | 

## Methods

### NewGroupResponse

`func NewGroupResponse(id string, domainId string, slug string, displayName string, source GroupResponseSource, createdAt time.Time, updatedAt time.Time, ) *GroupResponse`

NewGroupResponse instantiates a new GroupResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupResponseWithDefaults

`func NewGroupResponseWithDefaults() *GroupResponse`

NewGroupResponseWithDefaults instantiates a new GroupResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *GroupResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *GroupResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *GroupResponse) SetId(v string)`

SetId sets Id field to given value.


### GetDomainId

`func (o *GroupResponse) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *GroupResponse) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *GroupResponse) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetSlug

`func (o *GroupResponse) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *GroupResponse) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *GroupResponse) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *GroupResponse) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *GroupResponse) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *GroupResponse) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetSource

`func (o *GroupResponse) GetSource() GroupResponseSource`

GetSource returns the Source field if non-nil, zero value otherwise.

### GetSourceOk

`func (o *GroupResponse) GetSourceOk() (*GroupResponseSource, bool)`

GetSourceOk returns a tuple with the Source field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSource

`func (o *GroupResponse) SetSource(v GroupResponseSource)`

SetSource sets Source field to given value.


### GetIdpBindingId

`func (o *GroupResponse) GetIdpBindingId() string`

GetIdpBindingId returns the IdpBindingId field if non-nil, zero value otherwise.

### GetIdpBindingIdOk

`func (o *GroupResponse) GetIdpBindingIdOk() (*string, bool)`

GetIdpBindingIdOk returns a tuple with the IdpBindingId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdpBindingId

`func (o *GroupResponse) SetIdpBindingId(v string)`

SetIdpBindingId sets IdpBindingId field to given value.

### HasIdpBindingId

`func (o *GroupResponse) HasIdpBindingId() bool`

HasIdpBindingId returns a boolean if a field has been set.

### GetIdpClaimValue

`func (o *GroupResponse) GetIdpClaimValue() string`

GetIdpClaimValue returns the IdpClaimValue field if non-nil, zero value otherwise.

### GetIdpClaimValueOk

`func (o *GroupResponse) GetIdpClaimValueOk() (*string, bool)`

GetIdpClaimValueOk returns a tuple with the IdpClaimValue field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdpClaimValue

`func (o *GroupResponse) SetIdpClaimValue(v string)`

SetIdpClaimValue sets IdpClaimValue field to given value.

### HasIdpClaimValue

`func (o *GroupResponse) HasIdpClaimValue() bool`

HasIdpClaimValue returns a boolean if a field has been set.

### GetCreatedAt

`func (o *GroupResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *GroupResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *GroupResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *GroupResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *GroupResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *GroupResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


