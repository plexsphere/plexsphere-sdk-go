# IdPBindingRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DomainId** | **string** | Owning Domain. | 
**Issuer** | **string** | OIDC issuer URL (absolute http/https). | 
**ClientId** | **string** | OIDC client identifier. | 
**ClientSecretRef** | **string** | Opaque reference to the client secret held in the secret store — never the secret value itself.  | 
**DiscoveryUrl** | **string** | OIDC discovery document URL (absolute http/https). | 
**ClaimMappings** | Pointer to **map[string]string** | Mapping of plexsphere claim name → IdP claim name. An empty map is permitted.  | [optional] 
**RequiredAcr** | Pointer to **[]string** | Required OIDC ACR values. | [optional] 
**RequiredAmr** | Pointer to **[]string** | Required OIDC AMR values. | [optional] 
**JitPolicy** | [**IdPBindingRequestJitPolicy**](IdPBindingRequestJitPolicy.md) |  | 
**Alias** | Pointer to **string** | Optional human-friendly handle for the binding, unique per Domain among active bindings (e.g. &#x60;github&#x60;). Normalised to lowercase kebab-case, so an operator may submit mixed case.  | [optional] 
**Primary** | Pointer to **bool** | Mark this binding as the Domain default a Domain-only login resolves to. At most one active primary per Domain; a second primary is rejected with 409 primary-conflict.  | [optional] 

## Methods

### NewIdPBindingRequest

`func NewIdPBindingRequest(domainId string, issuer string, clientId string, clientSecretRef string, discoveryUrl string, jitPolicy IdPBindingRequestJitPolicy, ) *IdPBindingRequest`

NewIdPBindingRequest instantiates a new IdPBindingRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIdPBindingRequestWithDefaults

`func NewIdPBindingRequestWithDefaults() *IdPBindingRequest`

NewIdPBindingRequestWithDefaults instantiates a new IdPBindingRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDomainId

`func (o *IdPBindingRequest) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *IdPBindingRequest) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *IdPBindingRequest) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetIssuer

`func (o *IdPBindingRequest) GetIssuer() string`

GetIssuer returns the Issuer field if non-nil, zero value otherwise.

### GetIssuerOk

`func (o *IdPBindingRequest) GetIssuerOk() (*string, bool)`

GetIssuerOk returns a tuple with the Issuer field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIssuer

`func (o *IdPBindingRequest) SetIssuer(v string)`

SetIssuer sets Issuer field to given value.


### GetClientId

`func (o *IdPBindingRequest) GetClientId() string`

GetClientId returns the ClientId field if non-nil, zero value otherwise.

### GetClientIdOk

`func (o *IdPBindingRequest) GetClientIdOk() (*string, bool)`

GetClientIdOk returns a tuple with the ClientId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientId

`func (o *IdPBindingRequest) SetClientId(v string)`

SetClientId sets ClientId field to given value.


### GetClientSecretRef

`func (o *IdPBindingRequest) GetClientSecretRef() string`

GetClientSecretRef returns the ClientSecretRef field if non-nil, zero value otherwise.

### GetClientSecretRefOk

`func (o *IdPBindingRequest) GetClientSecretRefOk() (*string, bool)`

GetClientSecretRefOk returns a tuple with the ClientSecretRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientSecretRef

`func (o *IdPBindingRequest) SetClientSecretRef(v string)`

SetClientSecretRef sets ClientSecretRef field to given value.


### GetDiscoveryUrl

`func (o *IdPBindingRequest) GetDiscoveryUrl() string`

GetDiscoveryUrl returns the DiscoveryUrl field if non-nil, zero value otherwise.

### GetDiscoveryUrlOk

`func (o *IdPBindingRequest) GetDiscoveryUrlOk() (*string, bool)`

GetDiscoveryUrlOk returns a tuple with the DiscoveryUrl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDiscoveryUrl

`func (o *IdPBindingRequest) SetDiscoveryUrl(v string)`

SetDiscoveryUrl sets DiscoveryUrl field to given value.


### GetClaimMappings

`func (o *IdPBindingRequest) GetClaimMappings() map[string]string`

GetClaimMappings returns the ClaimMappings field if non-nil, zero value otherwise.

### GetClaimMappingsOk

`func (o *IdPBindingRequest) GetClaimMappingsOk() (*map[string]string, bool)`

GetClaimMappingsOk returns a tuple with the ClaimMappings field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClaimMappings

`func (o *IdPBindingRequest) SetClaimMappings(v map[string]string)`

SetClaimMappings sets ClaimMappings field to given value.

### HasClaimMappings

`func (o *IdPBindingRequest) HasClaimMappings() bool`

HasClaimMappings returns a boolean if a field has been set.

### GetRequiredAcr

`func (o *IdPBindingRequest) GetRequiredAcr() []string`

GetRequiredAcr returns the RequiredAcr field if non-nil, zero value otherwise.

### GetRequiredAcrOk

`func (o *IdPBindingRequest) GetRequiredAcrOk() (*[]string, bool)`

GetRequiredAcrOk returns a tuple with the RequiredAcr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequiredAcr

`func (o *IdPBindingRequest) SetRequiredAcr(v []string)`

SetRequiredAcr sets RequiredAcr field to given value.

### HasRequiredAcr

`func (o *IdPBindingRequest) HasRequiredAcr() bool`

HasRequiredAcr returns a boolean if a field has been set.

### GetRequiredAmr

`func (o *IdPBindingRequest) GetRequiredAmr() []string`

GetRequiredAmr returns the RequiredAmr field if non-nil, zero value otherwise.

### GetRequiredAmrOk

`func (o *IdPBindingRequest) GetRequiredAmrOk() (*[]string, bool)`

GetRequiredAmrOk returns a tuple with the RequiredAmr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequiredAmr

`func (o *IdPBindingRequest) SetRequiredAmr(v []string)`

SetRequiredAmr sets RequiredAmr field to given value.

### HasRequiredAmr

`func (o *IdPBindingRequest) HasRequiredAmr() bool`

HasRequiredAmr returns a boolean if a field has been set.

### GetJitPolicy

`func (o *IdPBindingRequest) GetJitPolicy() IdPBindingRequestJitPolicy`

GetJitPolicy returns the JitPolicy field if non-nil, zero value otherwise.

### GetJitPolicyOk

`func (o *IdPBindingRequest) GetJitPolicyOk() (*IdPBindingRequestJitPolicy, bool)`

GetJitPolicyOk returns a tuple with the JitPolicy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetJitPolicy

`func (o *IdPBindingRequest) SetJitPolicy(v IdPBindingRequestJitPolicy)`

SetJitPolicy sets JitPolicy field to given value.


### GetAlias

`func (o *IdPBindingRequest) GetAlias() string`

GetAlias returns the Alias field if non-nil, zero value otherwise.

### GetAliasOk

`func (o *IdPBindingRequest) GetAliasOk() (*string, bool)`

GetAliasOk returns a tuple with the Alias field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAlias

`func (o *IdPBindingRequest) SetAlias(v string)`

SetAlias sets Alias field to given value.

### HasAlias

`func (o *IdPBindingRequest) HasAlias() bool`

HasAlias returns a boolean if a field has been set.

### GetPrimary

`func (o *IdPBindingRequest) GetPrimary() bool`

GetPrimary returns the Primary field if non-nil, zero value otherwise.

### GetPrimaryOk

`func (o *IdPBindingRequest) GetPrimaryOk() (*bool, bool)`

GetPrimaryOk returns a tuple with the Primary field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrimary

`func (o *IdPBindingRequest) SetPrimary(v bool)`

SetPrimary sets Primary field to given value.

### HasPrimary

`func (o *IdPBindingRequest) HasPrimary() bool`

HasPrimary returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


