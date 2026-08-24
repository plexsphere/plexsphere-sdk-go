# Sink

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable identifier of the sink (UUIDv7). | 
**DomainId** | Pointer to **string** | Domain that declared the sink. Absent on a built-in sink, which belongs to no Domain.  | [optional] 
**Slug** | **string** | Kebab-case handle the sink is addressed by within its scope — unique per Domain for a tenant sink, globally for a built-in one.  | 
**DisplayName** | **string** | Human-readable name the sink is listed under. | 
**SinkType** | [**SinkType**](SinkType.md) |  | 
**BuiltIn** | **bool** | Whether the sink is platform-provided. A built-in sink is reachable from a route without an enablement and is neither updatable nor deletable.  | 
**Endpoint** | **string** | Address the sink delivers to — a URL or a host and port pair, depending on the type. Empty on a built-in sink, which the platform addresses through its own configuration.  | 
**Tls** | Pointer to [**SinkTLS**](SinkTLS.md) |  | [optional] 
**Credential** | Pointer to [**SinkCredential**](SinkCredential.md) |  | [optional] 
**Settings** | Pointer to [**SinkSettings**](SinkSettings.md) |  | [optional] 
**CreatedAt** | **time.Time** | RFC 3339 timestamp the sink was declared. | 
**UpdatedAt** | **time.Time** | RFC 3339 timestamp the sink was last changed. | 

## Methods

### NewSink

`func NewSink(id string, slug string, displayName string, sinkType SinkType, builtIn bool, endpoint string, createdAt time.Time, updatedAt time.Time, ) *Sink`

NewSink instantiates a new Sink object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkWithDefaults

`func NewSinkWithDefaults() *Sink`

NewSinkWithDefaults instantiates a new Sink object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *Sink) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *Sink) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *Sink) SetId(v string)`

SetId sets Id field to given value.


### GetDomainId

`func (o *Sink) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *Sink) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *Sink) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.

### HasDomainId

`func (o *Sink) HasDomainId() bool`

HasDomainId returns a boolean if a field has been set.

### GetSlug

`func (o *Sink) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *Sink) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *Sink) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *Sink) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *Sink) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *Sink) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetSinkType

`func (o *Sink) GetSinkType() SinkType`

GetSinkType returns the SinkType field if non-nil, zero value otherwise.

### GetSinkTypeOk

`func (o *Sink) GetSinkTypeOk() (*SinkType, bool)`

GetSinkTypeOk returns a tuple with the SinkType field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSinkType

`func (o *Sink) SetSinkType(v SinkType)`

SetSinkType sets SinkType field to given value.


### GetBuiltIn

`func (o *Sink) GetBuiltIn() bool`

GetBuiltIn returns the BuiltIn field if non-nil, zero value otherwise.

### GetBuiltInOk

`func (o *Sink) GetBuiltInOk() (*bool, bool)`

GetBuiltInOk returns a tuple with the BuiltIn field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBuiltIn

`func (o *Sink) SetBuiltIn(v bool)`

SetBuiltIn sets BuiltIn field to given value.


### GetEndpoint

`func (o *Sink) GetEndpoint() string`

GetEndpoint returns the Endpoint field if non-nil, zero value otherwise.

### GetEndpointOk

`func (o *Sink) GetEndpointOk() (*string, bool)`

GetEndpointOk returns a tuple with the Endpoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEndpoint

`func (o *Sink) SetEndpoint(v string)`

SetEndpoint sets Endpoint field to given value.


### GetTls

`func (o *Sink) GetTls() SinkTLS`

GetTls returns the Tls field if non-nil, zero value otherwise.

### GetTlsOk

`func (o *Sink) GetTlsOk() (*SinkTLS, bool)`

GetTlsOk returns a tuple with the Tls field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTls

`func (o *Sink) SetTls(v SinkTLS)`

SetTls sets Tls field to given value.

### HasTls

`func (o *Sink) HasTls() bool`

HasTls returns a boolean if a field has been set.

### GetCredential

`func (o *Sink) GetCredential() SinkCredential`

GetCredential returns the Credential field if non-nil, zero value otherwise.

### GetCredentialOk

`func (o *Sink) GetCredentialOk() (*SinkCredential, bool)`

GetCredentialOk returns a tuple with the Credential field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCredential

`func (o *Sink) SetCredential(v SinkCredential)`

SetCredential sets Credential field to given value.

### HasCredential

`func (o *Sink) HasCredential() bool`

HasCredential returns a boolean if a field has been set.

### GetSettings

`func (o *Sink) GetSettings() SinkSettings`

GetSettings returns the Settings field if non-nil, zero value otherwise.

### GetSettingsOk

`func (o *Sink) GetSettingsOk() (*SinkSettings, bool)`

GetSettingsOk returns a tuple with the Settings field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSettings

`func (o *Sink) SetSettings(v SinkSettings)`

SetSettings sets Settings field to given value.

### HasSettings

`func (o *Sink) HasSettings() bool`

HasSettings returns a boolean if a field has been set.

### GetCreatedAt

`func (o *Sink) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *Sink) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *Sink) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *Sink) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *Sink) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *Sink) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


