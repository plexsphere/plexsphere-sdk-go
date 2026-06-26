# DeviceCodeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DomainId** | **string** | Domain the caller is authenticating against. | 
**IdpBindingId** | Pointer to **string** | Explicit IdP binding within the Domain. Optional: when omitted, the binding is resolved by alias, then the Domain&#39;s primary binding, then its single active binding. A Domain with two or more active bindings and no primary requires this field (or idp_binding_alias) to disambiguate.  | [optional] 
**IdpBindingAlias** | Pointer to **string** | Human-friendly alias of an IdP binding within the Domain (e.g. &#x60;github&#x60;). Optional. Resolution precedence is explicit id, then alias, then the Domain&#39;s primary binding, then its single active binding. Mutually exclusive with idp_binding_id.  | [optional] 
**ClientId** | Pointer to **string** | Optional OIDC client identifier override. | [optional] 

## Methods

### NewDeviceCodeRequest

`func NewDeviceCodeRequest(domainId string, ) *DeviceCodeRequest`

NewDeviceCodeRequest instantiates a new DeviceCodeRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDeviceCodeRequestWithDefaults

`func NewDeviceCodeRequestWithDefaults() *DeviceCodeRequest`

NewDeviceCodeRequestWithDefaults instantiates a new DeviceCodeRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDomainId

`func (o *DeviceCodeRequest) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *DeviceCodeRequest) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *DeviceCodeRequest) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetIdpBindingId

`func (o *DeviceCodeRequest) GetIdpBindingId() string`

GetIdpBindingId returns the IdpBindingId field if non-nil, zero value otherwise.

### GetIdpBindingIdOk

`func (o *DeviceCodeRequest) GetIdpBindingIdOk() (*string, bool)`

GetIdpBindingIdOk returns a tuple with the IdpBindingId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdpBindingId

`func (o *DeviceCodeRequest) SetIdpBindingId(v string)`

SetIdpBindingId sets IdpBindingId field to given value.

### HasIdpBindingId

`func (o *DeviceCodeRequest) HasIdpBindingId() bool`

HasIdpBindingId returns a boolean if a field has been set.

### GetIdpBindingAlias

`func (o *DeviceCodeRequest) GetIdpBindingAlias() string`

GetIdpBindingAlias returns the IdpBindingAlias field if non-nil, zero value otherwise.

### GetIdpBindingAliasOk

`func (o *DeviceCodeRequest) GetIdpBindingAliasOk() (*string, bool)`

GetIdpBindingAliasOk returns a tuple with the IdpBindingAlias field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdpBindingAlias

`func (o *DeviceCodeRequest) SetIdpBindingAlias(v string)`

SetIdpBindingAlias sets IdpBindingAlias field to given value.

### HasIdpBindingAlias

`func (o *DeviceCodeRequest) HasIdpBindingAlias() bool`

HasIdpBindingAlias returns a boolean if a field has been set.

### GetClientId

`func (o *DeviceCodeRequest) GetClientId() string`

GetClientId returns the ClientId field if non-nil, zero value otherwise.

### GetClientIdOk

`func (o *DeviceCodeRequest) GetClientIdOk() (*string, bool)`

GetClientIdOk returns a tuple with the ClientId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientId

`func (o *DeviceCodeRequest) SetClientId(v string)`

SetClientId sets ClientId field to given value.

### HasClientId

`func (o *DeviceCodeRequest) HasClientId() bool`

HasClientId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


