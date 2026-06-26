# DomainIdPBinding

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Binding id to pin on POST /v1/auth/sign-in. | 
**Alias** | Pointer to **string** | Operator-assigned alias, when the binding carries one. | [optional] 
**Label** | **string** | Human-friendly button label — the alias when set, otherwise the issuer host.  | 
**IssuerHost** | **string** | Host component of the binding&#39;s OIDC issuer URL. | 
**Primary** | **bool** | Whether the binding is the Domain&#39;s default. | 
**PlatformScoped** | **bool** | Whether the binding is a shared platform binding. | 

## Methods

### NewDomainIdPBinding

`func NewDomainIdPBinding(id string, label string, issuerHost string, primary bool, platformScoped bool, ) *DomainIdPBinding`

NewDomainIdPBinding instantiates a new DomainIdPBinding object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDomainIdPBindingWithDefaults

`func NewDomainIdPBindingWithDefaults() *DomainIdPBinding`

NewDomainIdPBindingWithDefaults instantiates a new DomainIdPBinding object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *DomainIdPBinding) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *DomainIdPBinding) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *DomainIdPBinding) SetId(v string)`

SetId sets Id field to given value.


### GetAlias

`func (o *DomainIdPBinding) GetAlias() string`

GetAlias returns the Alias field if non-nil, zero value otherwise.

### GetAliasOk

`func (o *DomainIdPBinding) GetAliasOk() (*string, bool)`

GetAliasOk returns a tuple with the Alias field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAlias

`func (o *DomainIdPBinding) SetAlias(v string)`

SetAlias sets Alias field to given value.

### HasAlias

`func (o *DomainIdPBinding) HasAlias() bool`

HasAlias returns a boolean if a field has been set.

### GetLabel

`func (o *DomainIdPBinding) GetLabel() string`

GetLabel returns the Label field if non-nil, zero value otherwise.

### GetLabelOk

`func (o *DomainIdPBinding) GetLabelOk() (*string, bool)`

GetLabelOk returns a tuple with the Label field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLabel

`func (o *DomainIdPBinding) SetLabel(v string)`

SetLabel sets Label field to given value.


### GetIssuerHost

`func (o *DomainIdPBinding) GetIssuerHost() string`

GetIssuerHost returns the IssuerHost field if non-nil, zero value otherwise.

### GetIssuerHostOk

`func (o *DomainIdPBinding) GetIssuerHostOk() (*string, bool)`

GetIssuerHostOk returns a tuple with the IssuerHost field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIssuerHost

`func (o *DomainIdPBinding) SetIssuerHost(v string)`

SetIssuerHost sets IssuerHost field to given value.


### GetPrimary

`func (o *DomainIdPBinding) GetPrimary() bool`

GetPrimary returns the Primary field if non-nil, zero value otherwise.

### GetPrimaryOk

`func (o *DomainIdPBinding) GetPrimaryOk() (*bool, bool)`

GetPrimaryOk returns a tuple with the Primary field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrimary

`func (o *DomainIdPBinding) SetPrimary(v bool)`

SetPrimary sets Primary field to given value.


### GetPlatformScoped

`func (o *DomainIdPBinding) GetPlatformScoped() bool`

GetPlatformScoped returns the PlatformScoped field if non-nil, zero value otherwise.

### GetPlatformScopedOk

`func (o *DomainIdPBinding) GetPlatformScopedOk() (*bool, bool)`

GetPlatformScopedOk returns a tuple with the PlatformScoped field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPlatformScoped

`func (o *DomainIdPBinding) SetPlatformScoped(v bool)`

SetPlatformScoped sets PlatformScoped field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


