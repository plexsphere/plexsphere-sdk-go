# VerificationPolicy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Mode** | [**VerificationPolicyMode**](VerificationPolicyMode.md) |  | 
**IdentitySan** | Pointer to **string** | Regexp matched against the signing certificate&#39;s SAN. Required for &#x60;pinned&#x60;; must be absent for &#x60;unsigned&#x60;.  | [optional] 
**Issuer** | Pointer to **string** | Expected OIDC issuer. Required for &#x60;pinned&#x60;; must be absent for &#x60;unsigned&#x60;.  | [optional] 

## Methods

### NewVerificationPolicy

`func NewVerificationPolicy(mode VerificationPolicyMode, ) *VerificationPolicy`

NewVerificationPolicy instantiates a new VerificationPolicy object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewVerificationPolicyWithDefaults

`func NewVerificationPolicyWithDefaults() *VerificationPolicy`

NewVerificationPolicyWithDefaults instantiates a new VerificationPolicy object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMode

`func (o *VerificationPolicy) GetMode() VerificationPolicyMode`

GetMode returns the Mode field if non-nil, zero value otherwise.

### GetModeOk

`func (o *VerificationPolicy) GetModeOk() (*VerificationPolicyMode, bool)`

GetModeOk returns a tuple with the Mode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMode

`func (o *VerificationPolicy) SetMode(v VerificationPolicyMode)`

SetMode sets Mode field to given value.


### GetIdentitySan

`func (o *VerificationPolicy) GetIdentitySan() string`

GetIdentitySan returns the IdentitySan field if non-nil, zero value otherwise.

### GetIdentitySanOk

`func (o *VerificationPolicy) GetIdentitySanOk() (*string, bool)`

GetIdentitySanOk returns a tuple with the IdentitySan field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdentitySan

`func (o *VerificationPolicy) SetIdentitySan(v string)`

SetIdentitySan sets IdentitySan field to given value.

### HasIdentitySan

`func (o *VerificationPolicy) HasIdentitySan() bool`

HasIdentitySan returns a boolean if a field has been set.

### GetIssuer

`func (o *VerificationPolicy) GetIssuer() string`

GetIssuer returns the Issuer field if non-nil, zero value otherwise.

### GetIssuerOk

`func (o *VerificationPolicy) GetIssuerOk() (*string, bool)`

GetIssuerOk returns a tuple with the Issuer field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIssuer

`func (o *VerificationPolicy) SetIssuer(v string)`

SetIssuer sets Issuer field to given value.

### HasIssuer

`func (o *VerificationPolicy) HasIssuer() bool`

HasIssuer returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


