# GroupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DomainId** | **string** | Owning Domain. | 
**Slug** | **string** | URL-safe identifier unique within &#x60;domain_id&#x60;. Lowercase ASCII letters, digits, and internal dashes only; cannot start or end with a dash.  | 
**DisplayName** | **string** | Human-friendly Group name. | 
**Source** | [**GroupRequestSource**](GroupRequestSource.md) |  | 
**IdpBindingId** | Pointer to **string** | IdP binding the Group is reconciled from. Required when &#x60;source&#x3D;idp&#x60;; must be omitted when &#x60;source&#x3D;manual&#x60; .  | [optional] 
**IdpClaimValue** | Pointer to **string** | Verbatim IdP claim value the Group reconciles to. Required when &#x60;source&#x3D;idp&#x60;; must be omitted when &#x60;source&#x3D;manual&#x60; .  | [optional] 

## Methods

### NewGroupRequest

`func NewGroupRequest(domainId string, slug string, displayName string, source GroupRequestSource, ) *GroupRequest`

NewGroupRequest instantiates a new GroupRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupRequestWithDefaults

`func NewGroupRequestWithDefaults() *GroupRequest`

NewGroupRequestWithDefaults instantiates a new GroupRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDomainId

`func (o *GroupRequest) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *GroupRequest) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *GroupRequest) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetSlug

`func (o *GroupRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *GroupRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *GroupRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *GroupRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *GroupRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *GroupRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetSource

`func (o *GroupRequest) GetSource() GroupRequestSource`

GetSource returns the Source field if non-nil, zero value otherwise.

### GetSourceOk

`func (o *GroupRequest) GetSourceOk() (*GroupRequestSource, bool)`

GetSourceOk returns a tuple with the Source field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSource

`func (o *GroupRequest) SetSource(v GroupRequestSource)`

SetSource sets Source field to given value.


### GetIdpBindingId

`func (o *GroupRequest) GetIdpBindingId() string`

GetIdpBindingId returns the IdpBindingId field if non-nil, zero value otherwise.

### GetIdpBindingIdOk

`func (o *GroupRequest) GetIdpBindingIdOk() (*string, bool)`

GetIdpBindingIdOk returns a tuple with the IdpBindingId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdpBindingId

`func (o *GroupRequest) SetIdpBindingId(v string)`

SetIdpBindingId sets IdpBindingId field to given value.

### HasIdpBindingId

`func (o *GroupRequest) HasIdpBindingId() bool`

HasIdpBindingId returns a boolean if a field has been set.

### GetIdpClaimValue

`func (o *GroupRequest) GetIdpClaimValue() string`

GetIdpClaimValue returns the IdpClaimValue field if non-nil, zero value otherwise.

### GetIdpClaimValueOk

`func (o *GroupRequest) GetIdpClaimValueOk() (*string, bool)`

GetIdpClaimValueOk returns a tuple with the IdpClaimValue field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdpClaimValue

`func (o *GroupRequest) SetIdpClaimValue(v string)`

SetIdpClaimValue sets IdpClaimValue field to given value.

### HasIdpClaimValue

`func (o *GroupRequest) HasIdpClaimValue() bool`

HasIdpClaimValue returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


