# DeviceCodeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DomainId** | **string** | Domain the caller is authenticating against. | 
**IdpBindingId** | **string** | IdP binding within the Domain. | 
**ClientId** | Pointer to **string** | Optional OIDC client identifier override. | [optional] 

## Methods

### NewDeviceCodeRequest

`func NewDeviceCodeRequest(domainId string, idpBindingId string, ) *DeviceCodeRequest`

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


