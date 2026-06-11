# BootstrapTokenIssueRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | [**BootstrapTokenIssueRequestKind**](BootstrapTokenIssueRequestKind.md) |  | 
**EnvPrefix** | **string** | Lowercase ASCII letter run encoded as the environment segment of the plaintext. Same regex enforced by the aggregate and the parser, so the surface and the storage layer agree on the allowed alphabet.  | 
**TtlSeconds** | **int32** | Lifetime of the BootstrapToken in seconds. Bounded by the aggregate&#39;s &#x60;[MinTTL&#x3D;5m, MaxTTL&#x3D;24h]&#x60; window so a forgotten token cannot become a long-lived bearer credential .  | 

## Methods

### NewBootstrapTokenIssueRequest

`func NewBootstrapTokenIssueRequest(kind BootstrapTokenIssueRequestKind, envPrefix string, ttlSeconds int32, ) *BootstrapTokenIssueRequest`

NewBootstrapTokenIssueRequest instantiates a new BootstrapTokenIssueRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBootstrapTokenIssueRequestWithDefaults

`func NewBootstrapTokenIssueRequestWithDefaults() *BootstrapTokenIssueRequest`

NewBootstrapTokenIssueRequestWithDefaults instantiates a new BootstrapTokenIssueRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKind

`func (o *BootstrapTokenIssueRequest) GetKind() BootstrapTokenIssueRequestKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *BootstrapTokenIssueRequest) GetKindOk() (*BootstrapTokenIssueRequestKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *BootstrapTokenIssueRequest) SetKind(v BootstrapTokenIssueRequestKind)`

SetKind sets Kind field to given value.


### GetEnvPrefix

`func (o *BootstrapTokenIssueRequest) GetEnvPrefix() string`

GetEnvPrefix returns the EnvPrefix field if non-nil, zero value otherwise.

### GetEnvPrefixOk

`func (o *BootstrapTokenIssueRequest) GetEnvPrefixOk() (*string, bool)`

GetEnvPrefixOk returns a tuple with the EnvPrefix field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnvPrefix

`func (o *BootstrapTokenIssueRequest) SetEnvPrefix(v string)`

SetEnvPrefix sets EnvPrefix field to given value.


### GetTtlSeconds

`func (o *BootstrapTokenIssueRequest) GetTtlSeconds() int32`

GetTtlSeconds returns the TtlSeconds field if non-nil, zero value otherwise.

### GetTtlSecondsOk

`func (o *BootstrapTokenIssueRequest) GetTtlSecondsOk() (*int32, bool)`

GetTtlSecondsOk returns a tuple with the TtlSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTtlSeconds

`func (o *BootstrapTokenIssueRequest) SetTtlSeconds(v int32)`

SetTtlSeconds sets TtlSeconds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


