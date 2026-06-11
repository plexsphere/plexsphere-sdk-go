# APITokenSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Token identifier (UUIDv7). | 
**EnvPrefix** | **string** | Environment segment embedded in the plaintext. | 
**LastUsedAt** | Pointer to **time.Time** | Most-recent authentication timestamp, if any. | [optional] 
**CreatedAt** | **time.Time** | Issuance timestamp. | 
**ExpiresAt** | **time.Time** | Expiry timestamp. | 
**RotatedAt** | Pointer to **time.Time** | Timestamp the token was most recently rotated. | [optional] 

## Methods

### NewAPITokenSummary

`func NewAPITokenSummary(id string, envPrefix string, createdAt time.Time, expiresAt time.Time, ) *APITokenSummary`

NewAPITokenSummary instantiates a new APITokenSummary object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAPITokenSummaryWithDefaults

`func NewAPITokenSummaryWithDefaults() *APITokenSummary`

NewAPITokenSummaryWithDefaults instantiates a new APITokenSummary object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *APITokenSummary) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *APITokenSummary) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *APITokenSummary) SetId(v string)`

SetId sets Id field to given value.


### GetEnvPrefix

`func (o *APITokenSummary) GetEnvPrefix() string`

GetEnvPrefix returns the EnvPrefix field if non-nil, zero value otherwise.

### GetEnvPrefixOk

`func (o *APITokenSummary) GetEnvPrefixOk() (*string, bool)`

GetEnvPrefixOk returns a tuple with the EnvPrefix field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnvPrefix

`func (o *APITokenSummary) SetEnvPrefix(v string)`

SetEnvPrefix sets EnvPrefix field to given value.


### GetLastUsedAt

`func (o *APITokenSummary) GetLastUsedAt() time.Time`

GetLastUsedAt returns the LastUsedAt field if non-nil, zero value otherwise.

### GetLastUsedAtOk

`func (o *APITokenSummary) GetLastUsedAtOk() (*time.Time, bool)`

GetLastUsedAtOk returns a tuple with the LastUsedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLastUsedAt

`func (o *APITokenSummary) SetLastUsedAt(v time.Time)`

SetLastUsedAt sets LastUsedAt field to given value.

### HasLastUsedAt

`func (o *APITokenSummary) HasLastUsedAt() bool`

HasLastUsedAt returns a boolean if a field has been set.

### GetCreatedAt

`func (o *APITokenSummary) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *APITokenSummary) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *APITokenSummary) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetExpiresAt

`func (o *APITokenSummary) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *APITokenSummary) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *APITokenSummary) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetRotatedAt

`func (o *APITokenSummary) GetRotatedAt() time.Time`

GetRotatedAt returns the RotatedAt field if non-nil, zero value otherwise.

### GetRotatedAtOk

`func (o *APITokenSummary) GetRotatedAtOk() (*time.Time, bool)`

GetRotatedAtOk returns a tuple with the RotatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRotatedAt

`func (o *APITokenSummary) SetRotatedAt(v time.Time)`

SetRotatedAt sets RotatedAt field to given value.

### HasRotatedAt

`func (o *APITokenSummary) HasRotatedAt() bool`

HasRotatedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


