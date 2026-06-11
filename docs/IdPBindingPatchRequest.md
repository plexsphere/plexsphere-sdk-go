# IdPBindingPatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DiscoveryUrl** | Pointer to **string** | OIDC discovery document URL (absolute http/https). | [optional] 
**ClaimMappings** | Pointer to **map[string]string** | Mapping of plexsphere claim name → IdP claim name. An empty map clears all mappings.  | [optional] 
**RequiredAcr** | Pointer to **[]string** | Required OIDC ACR values. | [optional] 
**RequiredAmr** | Pointer to **[]string** | Required OIDC AMR values. | [optional] 
**JitPolicy** | Pointer to [**IdPBindingRequestJitPolicy**](IdPBindingRequestJitPolicy.md) |  | [optional] 

## Methods

### NewIdPBindingPatchRequest

`func NewIdPBindingPatchRequest() *IdPBindingPatchRequest`

NewIdPBindingPatchRequest instantiates a new IdPBindingPatchRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIdPBindingPatchRequestWithDefaults

`func NewIdPBindingPatchRequestWithDefaults() *IdPBindingPatchRequest`

NewIdPBindingPatchRequestWithDefaults instantiates a new IdPBindingPatchRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDiscoveryUrl

`func (o *IdPBindingPatchRequest) GetDiscoveryUrl() string`

GetDiscoveryUrl returns the DiscoveryUrl field if non-nil, zero value otherwise.

### GetDiscoveryUrlOk

`func (o *IdPBindingPatchRequest) GetDiscoveryUrlOk() (*string, bool)`

GetDiscoveryUrlOk returns a tuple with the DiscoveryUrl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDiscoveryUrl

`func (o *IdPBindingPatchRequest) SetDiscoveryUrl(v string)`

SetDiscoveryUrl sets DiscoveryUrl field to given value.

### HasDiscoveryUrl

`func (o *IdPBindingPatchRequest) HasDiscoveryUrl() bool`

HasDiscoveryUrl returns a boolean if a field has been set.

### GetClaimMappings

`func (o *IdPBindingPatchRequest) GetClaimMappings() map[string]string`

GetClaimMappings returns the ClaimMappings field if non-nil, zero value otherwise.

### GetClaimMappingsOk

`func (o *IdPBindingPatchRequest) GetClaimMappingsOk() (*map[string]string, bool)`

GetClaimMappingsOk returns a tuple with the ClaimMappings field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClaimMappings

`func (o *IdPBindingPatchRequest) SetClaimMappings(v map[string]string)`

SetClaimMappings sets ClaimMappings field to given value.

### HasClaimMappings

`func (o *IdPBindingPatchRequest) HasClaimMappings() bool`

HasClaimMappings returns a boolean if a field has been set.

### GetRequiredAcr

`func (o *IdPBindingPatchRequest) GetRequiredAcr() []string`

GetRequiredAcr returns the RequiredAcr field if non-nil, zero value otherwise.

### GetRequiredAcrOk

`func (o *IdPBindingPatchRequest) GetRequiredAcrOk() (*[]string, bool)`

GetRequiredAcrOk returns a tuple with the RequiredAcr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequiredAcr

`func (o *IdPBindingPatchRequest) SetRequiredAcr(v []string)`

SetRequiredAcr sets RequiredAcr field to given value.

### HasRequiredAcr

`func (o *IdPBindingPatchRequest) HasRequiredAcr() bool`

HasRequiredAcr returns a boolean if a field has been set.

### GetRequiredAmr

`func (o *IdPBindingPatchRequest) GetRequiredAmr() []string`

GetRequiredAmr returns the RequiredAmr field if non-nil, zero value otherwise.

### GetRequiredAmrOk

`func (o *IdPBindingPatchRequest) GetRequiredAmrOk() (*[]string, bool)`

GetRequiredAmrOk returns a tuple with the RequiredAmr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequiredAmr

`func (o *IdPBindingPatchRequest) SetRequiredAmr(v []string)`

SetRequiredAmr sets RequiredAmr field to given value.

### HasRequiredAmr

`func (o *IdPBindingPatchRequest) HasRequiredAmr() bool`

HasRequiredAmr returns a boolean if a field has been set.

### GetJitPolicy

`func (o *IdPBindingPatchRequest) GetJitPolicy() IdPBindingRequestJitPolicy`

GetJitPolicy returns the JitPolicy field if non-nil, zero value otherwise.

### GetJitPolicyOk

`func (o *IdPBindingPatchRequest) GetJitPolicyOk() (*IdPBindingRequestJitPolicy, bool)`

GetJitPolicyOk returns a tuple with the JitPolicy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetJitPolicy

`func (o *IdPBindingPatchRequest) SetJitPolicy(v IdPBindingRequestJitPolicy)`

SetJitPolicy sets JitPolicy field to given value.

### HasJitPolicy

`func (o *IdPBindingPatchRequest) HasJitPolicy() bool`

HasJitPolicy returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


