# SinkUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ExpectedUpdatedAt** | **time.Time** | The &#x60;updated_at&#x60; the client read the sink at. The write is applied only if the stored sink still carries it; a sink changed since that read is refused with &#x60;409 sink_cas_conflict&#x60; and nothing is written.  | 
**Slug** | **string** | Kebab-case handle, unique among the Domain&#39;s sinks. Moving it onto a slug another sink of the Domain holds is refused with &#x60;409 sink_slug_taken&#x60;.  | 
**DisplayName** | **string** | Human-readable name the sink is listed under. | 
**SinkType** | [**TenantSinkType**](TenantSinkType.md) |  | 
**Endpoint** | **string** | Address to deliver to, valid for the stated type. A host naming a literal address inside the platform&#39;s own network is refused.  | 
**Tls** | Pointer to [**SinkTLS**](SinkTLS.md) |  | [optional] 
**Credential** | Pointer to [**SinkCredentialInput**](SinkCredentialInput.md) |  | [optional] 
**Settings** | Pointer to [**SinkSettings**](SinkSettings.md) |  | [optional] 

## Methods

### NewSinkUpdateRequest

`func NewSinkUpdateRequest(expectedUpdatedAt time.Time, slug string, displayName string, sinkType TenantSinkType, endpoint string, ) *SinkUpdateRequest`

NewSinkUpdateRequest instantiates a new SinkUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkUpdateRequestWithDefaults

`func NewSinkUpdateRequestWithDefaults() *SinkUpdateRequest`

NewSinkUpdateRequestWithDefaults instantiates a new SinkUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetExpectedUpdatedAt

`func (o *SinkUpdateRequest) GetExpectedUpdatedAt() time.Time`

GetExpectedUpdatedAt returns the ExpectedUpdatedAt field if non-nil, zero value otherwise.

### GetExpectedUpdatedAtOk

`func (o *SinkUpdateRequest) GetExpectedUpdatedAtOk() (*time.Time, bool)`

GetExpectedUpdatedAtOk returns a tuple with the ExpectedUpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpectedUpdatedAt

`func (o *SinkUpdateRequest) SetExpectedUpdatedAt(v time.Time)`

SetExpectedUpdatedAt sets ExpectedUpdatedAt field to given value.


### GetSlug

`func (o *SinkUpdateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *SinkUpdateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *SinkUpdateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *SinkUpdateRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *SinkUpdateRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *SinkUpdateRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetSinkType

`func (o *SinkUpdateRequest) GetSinkType() TenantSinkType`

GetSinkType returns the SinkType field if non-nil, zero value otherwise.

### GetSinkTypeOk

`func (o *SinkUpdateRequest) GetSinkTypeOk() (*TenantSinkType, bool)`

GetSinkTypeOk returns a tuple with the SinkType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSinkType

`func (o *SinkUpdateRequest) SetSinkType(v TenantSinkType)`

SetSinkType sets SinkType field to given value.


### GetEndpoint

`func (o *SinkUpdateRequest) GetEndpoint() string`

GetEndpoint returns the Endpoint field if non-nil, zero value otherwise.

### GetEndpointOk

`func (o *SinkUpdateRequest) GetEndpointOk() (*string, bool)`

GetEndpointOk returns a tuple with the Endpoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEndpoint

`func (o *SinkUpdateRequest) SetEndpoint(v string)`

SetEndpoint sets Endpoint field to given value.


### GetTls

`func (o *SinkUpdateRequest) GetTls() SinkTLS`

GetTls returns the Tls field if non-nil, zero value otherwise.

### GetTlsOk

`func (o *SinkUpdateRequest) GetTlsOk() (*SinkTLS, bool)`

GetTlsOk returns a tuple with the Tls field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTls

`func (o *SinkUpdateRequest) SetTls(v SinkTLS)`

SetTls sets Tls field to given value.

### HasTls

`func (o *SinkUpdateRequest) HasTls() bool`

HasTls returns a boolean if a field has been set.

### GetCredential

`func (o *SinkUpdateRequest) GetCredential() SinkCredentialInput`

GetCredential returns the Credential field if non-nil, zero value otherwise.

### GetCredentialOk

`func (o *SinkUpdateRequest) GetCredentialOk() (*SinkCredentialInput, bool)`

GetCredentialOk returns a tuple with the Credential field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCredential

`func (o *SinkUpdateRequest) SetCredential(v SinkCredentialInput)`

SetCredential sets Credential field to given value.

### HasCredential

`func (o *SinkUpdateRequest) HasCredential() bool`

HasCredential returns a boolean if a field has been set.

### GetSettings

`func (o *SinkUpdateRequest) GetSettings() SinkSettings`

GetSettings returns the Settings field if non-nil, zero value otherwise.

### GetSettingsOk

`func (o *SinkUpdateRequest) GetSettingsOk() (*SinkSettings, bool)`

GetSettingsOk returns a tuple with the Settings field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSettings

`func (o *SinkUpdateRequest) SetSettings(v SinkSettings)`

SetSettings sets Settings field to given value.

### HasSettings

`func (o *SinkUpdateRequest) HasSettings() bool`

HasSettings returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


