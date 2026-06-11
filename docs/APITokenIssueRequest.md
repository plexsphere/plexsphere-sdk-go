# APITokenIssueRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IdentityRef** | **string** | Identifier of the user or ServiceIdentity the token binds to. Format is &#x60;user:&lt;uuid&gt;&#x60; or &#x60;service:&lt;uuid&gt;&#x60;.  | 
**EnvPrefix** | [**APITokenIssueRequestEnvPrefix**](APITokenIssueRequestEnvPrefix.md) |  | 
**TtlSeconds** | Pointer to **int32** | Optional TTL in seconds. If omitted, the server applies the deployment default.  | [optional] 

## Methods

### NewAPITokenIssueRequest

`func NewAPITokenIssueRequest(identityRef string, envPrefix APITokenIssueRequestEnvPrefix, ) *APITokenIssueRequest`

NewAPITokenIssueRequest instantiates a new APITokenIssueRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAPITokenIssueRequestWithDefaults

`func NewAPITokenIssueRequestWithDefaults() *APITokenIssueRequest`

NewAPITokenIssueRequestWithDefaults instantiates a new APITokenIssueRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetIdentityRef

`func (o *APITokenIssueRequest) GetIdentityRef() string`

GetIdentityRef returns the IdentityRef field if non-nil, zero value otherwise.

### GetIdentityRefOk

`func (o *APITokenIssueRequest) GetIdentityRefOk() (*string, bool)`

GetIdentityRefOk returns a tuple with the IdentityRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdentityRef

`func (o *APITokenIssueRequest) SetIdentityRef(v string)`

SetIdentityRef sets IdentityRef field to given value.


### GetEnvPrefix

`func (o *APITokenIssueRequest) GetEnvPrefix() APITokenIssueRequestEnvPrefix`

GetEnvPrefix returns the EnvPrefix field if non-nil, zero value otherwise.

### GetEnvPrefixOk

`func (o *APITokenIssueRequest) GetEnvPrefixOk() (*APITokenIssueRequestEnvPrefix, bool)`

GetEnvPrefixOk returns a tuple with the EnvPrefix field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnvPrefix

`func (o *APITokenIssueRequest) SetEnvPrefix(v APITokenIssueRequestEnvPrefix)`

SetEnvPrefix sets EnvPrefix field to given value.


### GetTtlSeconds

`func (o *APITokenIssueRequest) GetTtlSeconds() int32`

GetTtlSeconds returns the TtlSeconds field if non-nil, zero value otherwise.

### GetTtlSecondsOk

`func (o *APITokenIssueRequest) GetTtlSecondsOk() (*int32, bool)`

GetTtlSecondsOk returns a tuple with the TtlSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTtlSeconds

`func (o *APITokenIssueRequest) SetTtlSeconds(v int32)`

SetTtlSeconds sets TtlSeconds field to given value.

### HasTtlSeconds

`func (o *APITokenIssueRequest) HasTtlSeconds() bool`

HasTtlSeconds returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


