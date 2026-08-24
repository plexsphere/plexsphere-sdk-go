# SinkCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | Pointer to **string** | Identifier to declare the sink under (UUIDv7). Absent lets the server mint one. A caller that stores connection material mints the id first so it can derive the KV path the material is written to before the sink exists.  | [optional] 
**Slug** | **string** | Kebab-case handle, unique among the Domain&#39;s sinks. Leading and trailing whitespace is refused rather than trimmed.  | 
**DisplayName** | **string** | Human-readable name the sink is listed under. | 
**SinkType** | [**TenantSinkType**](TenantSinkType.md) |  | 
**Endpoint** | **string** | Address to deliver to: an &#x60;https&#x60; URL for &#x60;otlp&#x60;, a host and port pair for &#x60;syslog&#x60;. A host naming a literal address inside the platform&#39;s own network is refused.  | 
**Tls** | Pointer to [**SinkTLS**](SinkTLS.md) |  | [optional] 
**Credential** | Pointer to [**SinkCredentialInput**](SinkCredentialInput.md) |  | [optional] 
**Settings** | Pointer to [**SinkSettings**](SinkSettings.md) |  | [optional] 

## Methods

### NewSinkCreateRequest

`func NewSinkCreateRequest(slug string, displayName string, sinkType TenantSinkType, endpoint string, ) *SinkCreateRequest`

NewSinkCreateRequest instantiates a new SinkCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkCreateRequestWithDefaults

`func NewSinkCreateRequestWithDefaults() *SinkCreateRequest`

NewSinkCreateRequestWithDefaults instantiates a new SinkCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *SinkCreateRequest) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *SinkCreateRequest) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *SinkCreateRequest) SetId(v string)`

SetId sets Id field to given value.

### HasId

`func (o *SinkCreateRequest) HasId() bool`

HasId returns a boolean if a field has been set.

### GetSlug

`func (o *SinkCreateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *SinkCreateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *SinkCreateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *SinkCreateRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *SinkCreateRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *SinkCreateRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetSinkType

`func (o *SinkCreateRequest) GetSinkType() TenantSinkType`

GetSinkType returns the SinkType field if non-nil, zero value otherwise.

### GetSinkTypeOk

`func (o *SinkCreateRequest) GetSinkTypeOk() (*TenantSinkType, bool)`

GetSinkTypeOk returns a tuple with the SinkType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSinkType

`func (o *SinkCreateRequest) SetSinkType(v TenantSinkType)`

SetSinkType sets SinkType field to given value.


### GetEndpoint

`func (o *SinkCreateRequest) GetEndpoint() string`

GetEndpoint returns the Endpoint field if non-nil, zero value otherwise.

### GetEndpointOk

`func (o *SinkCreateRequest) GetEndpointOk() (*string, bool)`

GetEndpointOk returns a tuple with the Endpoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEndpoint

`func (o *SinkCreateRequest) SetEndpoint(v string)`

SetEndpoint sets Endpoint field to given value.


### GetTls

`func (o *SinkCreateRequest) GetTls() SinkTLS`

GetTls returns the Tls field if non-nil, zero value otherwise.

### GetTlsOk

`func (o *SinkCreateRequest) GetTlsOk() (*SinkTLS, bool)`

GetTlsOk returns a tuple with the Tls field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTls

`func (o *SinkCreateRequest) SetTls(v SinkTLS)`

SetTls sets Tls field to given value.

### HasTls

`func (o *SinkCreateRequest) HasTls() bool`

HasTls returns a boolean if a field has been set.

### GetCredential

`func (o *SinkCreateRequest) GetCredential() SinkCredentialInput`

GetCredential returns the Credential field if non-nil, zero value otherwise.

### GetCredentialOk

`func (o *SinkCreateRequest) GetCredentialOk() (*SinkCredentialInput, bool)`

GetCredentialOk returns a tuple with the Credential field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCredential

`func (o *SinkCreateRequest) SetCredential(v SinkCredentialInput)`

SetCredential sets Credential field to given value.

### HasCredential

`func (o *SinkCreateRequest) HasCredential() bool`

HasCredential returns a boolean if a field has been set.

### GetSettings

`func (o *SinkCreateRequest) GetSettings() SinkSettings`

GetSettings returns the Settings field if non-nil, zero value otherwise.

### GetSettingsOk

`func (o *SinkCreateRequest) GetSettingsOk() (*SinkSettings, bool)`

GetSettingsOk returns a tuple with the Settings field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSettings

`func (o *SinkCreateRequest) SetSettings(v SinkSettings)`

SetSettings sets Settings field to given value.

### HasSettings

`func (o *SinkCreateRequest) HasSettings() bool`

HasSettings returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


