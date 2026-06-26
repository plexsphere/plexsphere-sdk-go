# PlatformIdPBindingRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Issuer** | **string** | OIDC issuer URL (absolute http/https). | 
**ClientId** | **string** | OIDC client identifier. | 
**ClientSecretRef** | **string** | Opaque reference to the client secret held in the secret store — never the secret value itself.  | 
**DiscoveryUrl** | **string** | OIDC discovery document URL (absolute http/https). | 
**ClaimMappings** | Pointer to **map[string]string** | Mapping of plexsphere claim name → IdP claim name. An empty map is permitted. The mappings apply uniformly to every Domain that resolves through this shared binding.  | [optional] 
**RequiredAcr** | Pointer to **[]string** | Required OIDC ACR values. | [optional] 
**RequiredAmr** | Pointer to **[]string** | Required OIDC AMR values. | [optional] 
**JitPolicy** | **string** | Just-in-time user-provisioning policy. One of &#x60;allow&#x60; or &#x60;deny&#x60;; the server rejects any other value with 400 &#x60;invalid-jit-policy&#x60;. Declared as a plain string rather than an inline enum so it shares the IdPBinding jit-policy vocabulary without minting a fourth generated enum type.  | 
**Alias** | Pointer to **string** | Optional human-friendly handle for the binding, unique among active platform bindings (e.g. &#x60;github&#x60;). Normalised to lowercase kebab-case, so an operator may submit mixed case.  | [optional] 

## Methods

### NewPlatformIdPBindingRequest

`func NewPlatformIdPBindingRequest(issuer string, clientId string, clientSecretRef string, discoveryUrl string, jitPolicy string, ) *PlatformIdPBindingRequest`

NewPlatformIdPBindingRequest instantiates a new PlatformIdPBindingRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPlatformIdPBindingRequestWithDefaults

`func NewPlatformIdPBindingRequestWithDefaults() *PlatformIdPBindingRequest`

NewPlatformIdPBindingRequestWithDefaults instantiates a new PlatformIdPBindingRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetIssuer

`func (o *PlatformIdPBindingRequest) GetIssuer() string`

GetIssuer returns the Issuer field if non-nil, zero value otherwise.

### GetIssuerOk

`func (o *PlatformIdPBindingRequest) GetIssuerOk() (*string, bool)`

GetIssuerOk returns a tuple with the Issuer field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIssuer

`func (o *PlatformIdPBindingRequest) SetIssuer(v string)`

SetIssuer sets Issuer field to given value.


### GetClientId

`func (o *PlatformIdPBindingRequest) GetClientId() string`

GetClientId returns the ClientId field if non-nil, zero value otherwise.

### GetClientIdOk

`func (o *PlatformIdPBindingRequest) GetClientIdOk() (*string, bool)`

GetClientIdOk returns a tuple with the ClientId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientId

`func (o *PlatformIdPBindingRequest) SetClientId(v string)`

SetClientId sets ClientId field to given value.


### GetClientSecretRef

`func (o *PlatformIdPBindingRequest) GetClientSecretRef() string`

GetClientSecretRef returns the ClientSecretRef field if non-nil, zero value otherwise.

### GetClientSecretRefOk

`func (o *PlatformIdPBindingRequest) GetClientSecretRefOk() (*string, bool)`

GetClientSecretRefOk returns a tuple with the ClientSecretRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientSecretRef

`func (o *PlatformIdPBindingRequest) SetClientSecretRef(v string)`

SetClientSecretRef sets ClientSecretRef field to given value.


### GetDiscoveryUrl

`func (o *PlatformIdPBindingRequest) GetDiscoveryUrl() string`

GetDiscoveryUrl returns the DiscoveryUrl field if non-nil, zero value otherwise.

### GetDiscoveryUrlOk

`func (o *PlatformIdPBindingRequest) GetDiscoveryUrlOk() (*string, bool)`

GetDiscoveryUrlOk returns a tuple with the DiscoveryUrl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDiscoveryUrl

`func (o *PlatformIdPBindingRequest) SetDiscoveryUrl(v string)`

SetDiscoveryUrl sets DiscoveryUrl field to given value.


### GetClaimMappings

`func (o *PlatformIdPBindingRequest) GetClaimMappings() map[string]string`

GetClaimMappings returns the ClaimMappings field if non-nil, zero value otherwise.

### GetClaimMappingsOk

`func (o *PlatformIdPBindingRequest) GetClaimMappingsOk() (*map[string]string, bool)`

GetClaimMappingsOk returns a tuple with the ClaimMappings field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClaimMappings

`func (o *PlatformIdPBindingRequest) SetClaimMappings(v map[string]string)`

SetClaimMappings sets ClaimMappings field to given value.

### HasClaimMappings

`func (o *PlatformIdPBindingRequest) HasClaimMappings() bool`

HasClaimMappings returns a boolean if a field has been set.

### GetRequiredAcr

`func (o *PlatformIdPBindingRequest) GetRequiredAcr() []string`

GetRequiredAcr returns the RequiredAcr field if non-nil, zero value otherwise.

### GetRequiredAcrOk

`func (o *PlatformIdPBindingRequest) GetRequiredAcrOk() (*[]string, bool)`

GetRequiredAcrOk returns a tuple with the RequiredAcr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequiredAcr

`func (o *PlatformIdPBindingRequest) SetRequiredAcr(v []string)`

SetRequiredAcr sets RequiredAcr field to given value.

### HasRequiredAcr

`func (o *PlatformIdPBindingRequest) HasRequiredAcr() bool`

HasRequiredAcr returns a boolean if a field has been set.

### GetRequiredAmr

`func (o *PlatformIdPBindingRequest) GetRequiredAmr() []string`

GetRequiredAmr returns the RequiredAmr field if non-nil, zero value otherwise.

### GetRequiredAmrOk

`func (o *PlatformIdPBindingRequest) GetRequiredAmrOk() (*[]string, bool)`

GetRequiredAmrOk returns a tuple with the RequiredAmr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequiredAmr

`func (o *PlatformIdPBindingRequest) SetRequiredAmr(v []string)`

SetRequiredAmr sets RequiredAmr field to given value.

### HasRequiredAmr

`func (o *PlatformIdPBindingRequest) HasRequiredAmr() bool`

HasRequiredAmr returns a boolean if a field has been set.

### GetJitPolicy

`func (o *PlatformIdPBindingRequest) GetJitPolicy() string`

GetJitPolicy returns the JitPolicy field if non-nil, zero value otherwise.

### GetJitPolicyOk

`func (o *PlatformIdPBindingRequest) GetJitPolicyOk() (*string, bool)`

GetJitPolicyOk returns a tuple with the JitPolicy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetJitPolicy

`func (o *PlatformIdPBindingRequest) SetJitPolicy(v string)`

SetJitPolicy sets JitPolicy field to given value.


### GetAlias

`func (o *PlatformIdPBindingRequest) GetAlias() string`

GetAlias returns the Alias field if non-nil, zero value otherwise.

### GetAliasOk

`func (o *PlatformIdPBindingRequest) GetAliasOk() (*string, bool)`

GetAliasOk returns a tuple with the Alias field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAlias

`func (o *PlatformIdPBindingRequest) SetAlias(v string)`

SetAlias sets Alias field to given value.

### HasAlias

`func (o *PlatformIdPBindingRequest) HasAlias() bool`

HasAlias returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


