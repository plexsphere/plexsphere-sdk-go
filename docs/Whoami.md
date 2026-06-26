# Whoami

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PrincipalType** | [**WhoamiPrincipalType**](WhoamiPrincipalType.md) |  | 
**Subject** | **string** | Principal identifier (UUIDv7 serialised as a string). | 
**DomainId** | Pointer to **string** | Domain the principal belongs to. | [optional] 
**Email** | Pointer to **string** | Primary email of the principal as projected by the upstream IdP at sign-in. Omitted when the IdP did not supply an &#x60;email&#x60; claim or the principal is a ServiceIdentity. A browser client renders it as the human-readable identity label.  | [optional] 
**Acr** | Pointer to **string** | Authentication Context Class Reference, if available. | [optional] 
**Amr** | Pointer to **[]string** | Authentication Methods References (e.g. \&quot;pwd\&quot;, \&quot;mfa\&quot;). | [optional] 

## Methods

### NewWhoami

`func NewWhoami(principalType WhoamiPrincipalType, subject string, ) *Whoami`

NewWhoami instantiates a new Whoami object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewWhoamiWithDefaults

`func NewWhoamiWithDefaults() *Whoami`

NewWhoamiWithDefaults instantiates a new Whoami object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPrincipalType

`func (o *Whoami) GetPrincipalType() WhoamiPrincipalType`

GetPrincipalType returns the PrincipalType field if non-nil, zero value otherwise.

### GetPrincipalTypeOk

`func (o *Whoami) GetPrincipalTypeOk() (*WhoamiPrincipalType, bool)`

GetPrincipalTypeOk returns a tuple with the PrincipalType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrincipalType

`func (o *Whoami) SetPrincipalType(v WhoamiPrincipalType)`

SetPrincipalType sets PrincipalType field to given value.


### GetSubject

`func (o *Whoami) GetSubject() string`

GetSubject returns the Subject field if non-nil, zero value otherwise.

### GetSubjectOk

`func (o *Whoami) GetSubjectOk() (*string, bool)`

GetSubjectOk returns a tuple with the Subject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubject

`func (o *Whoami) SetSubject(v string)`

SetSubject sets Subject field to given value.


### GetDomainId

`func (o *Whoami) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *Whoami) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *Whoami) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.

### HasDomainId

`func (o *Whoami) HasDomainId() bool`

HasDomainId returns a boolean if a field has been set.

### GetEmail

`func (o *Whoami) GetEmail() string`

GetEmail returns the Email field if non-nil, zero value otherwise.

### GetEmailOk

`func (o *Whoami) GetEmailOk() (*string, bool)`

GetEmailOk returns a tuple with the Email field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEmail

`func (o *Whoami) SetEmail(v string)`

SetEmail sets Email field to given value.

### HasEmail

`func (o *Whoami) HasEmail() bool`

HasEmail returns a boolean if a field has been set.

### GetAcr

`func (o *Whoami) GetAcr() string`

GetAcr returns the Acr field if non-nil, zero value otherwise.

### GetAcrOk

`func (o *Whoami) GetAcrOk() (*string, bool)`

GetAcrOk returns a tuple with the Acr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcr

`func (o *Whoami) SetAcr(v string)`

SetAcr sets Acr field to given value.

### HasAcr

`func (o *Whoami) HasAcr() bool`

HasAcr returns a boolean if a field has been set.

### GetAmr

`func (o *Whoami) GetAmr() []string`

GetAmr returns the Amr field if non-nil, zero value otherwise.

### GetAmrOk

`func (o *Whoami) GetAmrOk() (*[]string, bool)`

GetAmrOk returns a tuple with the Amr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAmr

`func (o *Whoami) SetAmr(v []string)`

SetAmr sets Amr field to given value.

### HasAmr

`func (o *Whoami) HasAmr() bool`

HasAmr returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


