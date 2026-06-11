# ServiceTokenRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GrantType** | [**ServiceTokenRequestGrantType**](ServiceTokenRequestGrantType.md) |  | 
**ClientId** | Pointer to **string** | ServiceIdentity client identifier. | [optional] 
**ClientSecret** | Pointer to **string** | Client secret for the &#x60;client_credentials&#x60; grant. Rejected for the JWT-bearer grant.  | [optional] 
**ClientAssertion** | Pointer to **string** | Signed JWT assertion for the JWT-bearer grant. Rejected for the &#x60;client_credentials&#x60; grant.  | [optional] 
**Scope** | Pointer to **string** | Optional space-delimited OAuth2 scope list. | [optional] 

## Methods

### NewServiceTokenRequest

`func NewServiceTokenRequest(grantType ServiceTokenRequestGrantType, ) *ServiceTokenRequest`

NewServiceTokenRequest instantiates a new ServiceTokenRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewServiceTokenRequestWithDefaults

`func NewServiceTokenRequestWithDefaults() *ServiceTokenRequest`

NewServiceTokenRequestWithDefaults instantiates a new ServiceTokenRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetGrantType

`func (o *ServiceTokenRequest) GetGrantType() ServiceTokenRequestGrantType`

GetGrantType returns the GrantType field if non-nil, zero value otherwise.

### GetGrantTypeOk

`func (o *ServiceTokenRequest) GetGrantTypeOk() (*ServiceTokenRequestGrantType, bool)`

GetGrantTypeOk returns a tuple with the GrantType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGrantType

`func (o *ServiceTokenRequest) SetGrantType(v ServiceTokenRequestGrantType)`

SetGrantType sets GrantType field to given value.


### GetClientId

`func (o *ServiceTokenRequest) GetClientId() string`

GetClientId returns the ClientId field if non-nil, zero value otherwise.

### GetClientIdOk

`func (o *ServiceTokenRequest) GetClientIdOk() (*string, bool)`

GetClientIdOk returns a tuple with the ClientId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientId

`func (o *ServiceTokenRequest) SetClientId(v string)`

SetClientId sets ClientId field to given value.

### HasClientId

`func (o *ServiceTokenRequest) HasClientId() bool`

HasClientId returns a boolean if a field has been set.

### GetClientSecret

`func (o *ServiceTokenRequest) GetClientSecret() string`

GetClientSecret returns the ClientSecret field if non-nil, zero value otherwise.

### GetClientSecretOk

`func (o *ServiceTokenRequest) GetClientSecretOk() (*string, bool)`

GetClientSecretOk returns a tuple with the ClientSecret field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientSecret

`func (o *ServiceTokenRequest) SetClientSecret(v string)`

SetClientSecret sets ClientSecret field to given value.

### HasClientSecret

`func (o *ServiceTokenRequest) HasClientSecret() bool`

HasClientSecret returns a boolean if a field has been set.

### GetClientAssertion

`func (o *ServiceTokenRequest) GetClientAssertion() string`

GetClientAssertion returns the ClientAssertion field if non-nil, zero value otherwise.

### GetClientAssertionOk

`func (o *ServiceTokenRequest) GetClientAssertionOk() (*string, bool)`

GetClientAssertionOk returns a tuple with the ClientAssertion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientAssertion

`func (o *ServiceTokenRequest) SetClientAssertion(v string)`

SetClientAssertion sets ClientAssertion field to given value.

### HasClientAssertion

`func (o *ServiceTokenRequest) HasClientAssertion() bool`

HasClientAssertion returns a boolean if a field has been set.

### GetScope

`func (o *ServiceTokenRequest) GetScope() string`

GetScope returns the Scope field if non-nil, zero value otherwise.

### GetScopeOk

`func (o *ServiceTokenRequest) GetScopeOk() (*string, bool)`

GetScopeOk returns a tuple with the Scope field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScope

`func (o *ServiceTokenRequest) SetScope(v string)`

SetScope sets Scope field to given value.

### HasScope

`func (o *ServiceTokenRequest) HasScope() bool`

HasScope returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


