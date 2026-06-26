# IdPBindingResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Binding identifier (UUIDv7). | 
**DomainId** | Pointer to **string** | Owning Domain, or null for a platform-scoped (shared) binding usable by any Domain.  | [optional] 
**Issuer** | **string** | OIDC issuer URL. | 
**ClientId** | **string** | OIDC client identifier. | 
**ClientSecretRef** | **string** | Opaque reference to the client secret. | 
**DiscoveryUrl** | **string** | OIDC discovery document URL. | 
**ClaimMappings** | Pointer to **map[string]string** | Plexsphere claim → IdP claim mapping. | [optional] 
**RequiredAcr** | Pointer to **[]string** |  | [optional] 
**RequiredAmr** | Pointer to **[]string** |  | [optional] 
**JitPolicy** | [**IdPBindingResponseJitPolicy**](IdPBindingResponseJitPolicy.md) |  | 
**Status** | [**IdPBindingResponseStatus**](IdPBindingResponseStatus.md) |  | 
**Alias** | Pointer to **string** | Human-friendly handle, unique per Domain among active bindings. Absent when the binding has no alias.  | [optional] 
**Primary** | **bool** | Whether this binding is the Domain default a Domain-only login resolves to.  | 
**CreatedAt** | **time.Time** |  | 
**UpdatedAt** | **time.Time** |  | 

## Methods

### NewIdPBindingResponse

`func NewIdPBindingResponse(id string, issuer string, clientId string, clientSecretRef string, discoveryUrl string, jitPolicy IdPBindingResponseJitPolicy, status IdPBindingResponseStatus, primary bool, createdAt time.Time, updatedAt time.Time, ) *IdPBindingResponse`

NewIdPBindingResponse instantiates a new IdPBindingResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIdPBindingResponseWithDefaults

`func NewIdPBindingResponseWithDefaults() *IdPBindingResponse`

NewIdPBindingResponseWithDefaults instantiates a new IdPBindingResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *IdPBindingResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *IdPBindingResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *IdPBindingResponse) SetId(v string)`

SetId sets Id field to given value.


### GetDomainId

`func (o *IdPBindingResponse) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *IdPBindingResponse) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *IdPBindingResponse) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.

### HasDomainId

`func (o *IdPBindingResponse) HasDomainId() bool`

HasDomainId returns a boolean if a field has been set.

### GetIssuer

`func (o *IdPBindingResponse) GetIssuer() string`

GetIssuer returns the Issuer field if non-nil, zero value otherwise.

### GetIssuerOk

`func (o *IdPBindingResponse) GetIssuerOk() (*string, bool)`

GetIssuerOk returns a tuple with the Issuer field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIssuer

`func (o *IdPBindingResponse) SetIssuer(v string)`

SetIssuer sets Issuer field to given value.


### GetClientId

`func (o *IdPBindingResponse) GetClientId() string`

GetClientId returns the ClientId field if non-nil, zero value otherwise.

### GetClientIdOk

`func (o *IdPBindingResponse) GetClientIdOk() (*string, bool)`

GetClientIdOk returns a tuple with the ClientId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientId

`func (o *IdPBindingResponse) SetClientId(v string)`

SetClientId sets ClientId field to given value.


### GetClientSecretRef

`func (o *IdPBindingResponse) GetClientSecretRef() string`

GetClientSecretRef returns the ClientSecretRef field if non-nil, zero value otherwise.

### GetClientSecretRefOk

`func (o *IdPBindingResponse) GetClientSecretRefOk() (*string, bool)`

GetClientSecretRefOk returns a tuple with the ClientSecretRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientSecretRef

`func (o *IdPBindingResponse) SetClientSecretRef(v string)`

SetClientSecretRef sets ClientSecretRef field to given value.


### GetDiscoveryUrl

`func (o *IdPBindingResponse) GetDiscoveryUrl() string`

GetDiscoveryUrl returns the DiscoveryUrl field if non-nil, zero value otherwise.

### GetDiscoveryUrlOk

`func (o *IdPBindingResponse) GetDiscoveryUrlOk() (*string, bool)`

GetDiscoveryUrlOk returns a tuple with the DiscoveryUrl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDiscoveryUrl

`func (o *IdPBindingResponse) SetDiscoveryUrl(v string)`

SetDiscoveryUrl sets DiscoveryUrl field to given value.


### GetClaimMappings

`func (o *IdPBindingResponse) GetClaimMappings() map[string]string`

GetClaimMappings returns the ClaimMappings field if non-nil, zero value otherwise.

### GetClaimMappingsOk

`func (o *IdPBindingResponse) GetClaimMappingsOk() (*map[string]string, bool)`

GetClaimMappingsOk returns a tuple with the ClaimMappings field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClaimMappings

`func (o *IdPBindingResponse) SetClaimMappings(v map[string]string)`

SetClaimMappings sets ClaimMappings field to given value.

### HasClaimMappings

`func (o *IdPBindingResponse) HasClaimMappings() bool`

HasClaimMappings returns a boolean if a field has been set.

### GetRequiredAcr

`func (o *IdPBindingResponse) GetRequiredAcr() []string`

GetRequiredAcr returns the RequiredAcr field if non-nil, zero value otherwise.

### GetRequiredAcrOk

`func (o *IdPBindingResponse) GetRequiredAcrOk() (*[]string, bool)`

GetRequiredAcrOk returns a tuple with the RequiredAcr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequiredAcr

`func (o *IdPBindingResponse) SetRequiredAcr(v []string)`

SetRequiredAcr sets RequiredAcr field to given value.

### HasRequiredAcr

`func (o *IdPBindingResponse) HasRequiredAcr() bool`

HasRequiredAcr returns a boolean if a field has been set.

### GetRequiredAmr

`func (o *IdPBindingResponse) GetRequiredAmr() []string`

GetRequiredAmr returns the RequiredAmr field if non-nil, zero value otherwise.

### GetRequiredAmrOk

`func (o *IdPBindingResponse) GetRequiredAmrOk() (*[]string, bool)`

GetRequiredAmrOk returns a tuple with the RequiredAmr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequiredAmr

`func (o *IdPBindingResponse) SetRequiredAmr(v []string)`

SetRequiredAmr sets RequiredAmr field to given value.

### HasRequiredAmr

`func (o *IdPBindingResponse) HasRequiredAmr() bool`

HasRequiredAmr returns a boolean if a field has been set.

### GetJitPolicy

`func (o *IdPBindingResponse) GetJitPolicy() IdPBindingResponseJitPolicy`

GetJitPolicy returns the JitPolicy field if non-nil, zero value otherwise.

### GetJitPolicyOk

`func (o *IdPBindingResponse) GetJitPolicyOk() (*IdPBindingResponseJitPolicy, bool)`

GetJitPolicyOk returns a tuple with the JitPolicy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetJitPolicy

`func (o *IdPBindingResponse) SetJitPolicy(v IdPBindingResponseJitPolicy)`

SetJitPolicy sets JitPolicy field to given value.


### GetStatus

`func (o *IdPBindingResponse) GetStatus() IdPBindingResponseStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *IdPBindingResponse) GetStatusOk() (*IdPBindingResponseStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *IdPBindingResponse) SetStatus(v IdPBindingResponseStatus)`

SetStatus sets Status field to given value.


### GetAlias

`func (o *IdPBindingResponse) GetAlias() string`

GetAlias returns the Alias field if non-nil, zero value otherwise.

### GetAliasOk

`func (o *IdPBindingResponse) GetAliasOk() (*string, bool)`

GetAliasOk returns a tuple with the Alias field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAlias

`func (o *IdPBindingResponse) SetAlias(v string)`

SetAlias sets Alias field to given value.

### HasAlias

`func (o *IdPBindingResponse) HasAlias() bool`

HasAlias returns a boolean if a field has been set.

### GetPrimary

`func (o *IdPBindingResponse) GetPrimary() bool`

GetPrimary returns the Primary field if non-nil, zero value otherwise.

### GetPrimaryOk

`func (o *IdPBindingResponse) GetPrimaryOk() (*bool, bool)`

GetPrimaryOk returns a tuple with the Primary field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrimary

`func (o *IdPBindingResponse) SetPrimary(v bool)`

SetPrimary sets Primary field to given value.


### GetCreatedAt

`func (o *IdPBindingResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *IdPBindingResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *IdPBindingResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *IdPBindingResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *IdPBindingResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *IdPBindingResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


