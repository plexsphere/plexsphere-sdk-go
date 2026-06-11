# CredentialRotateMaterial

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Payload** | **string** | Base64-encoded secret bytes written under &#x60;data.payload&#x60; in KV-v2. Empty payload is rejected with &#x60;400 invalid_rotate_material&#x60;.  | 
**TtlSeconds** | **int64** | Expiry budget in seconds from which the broker derives the refreshed &#x60;expires_at&#x60;. Must be a positive whole number of seconds (≤ 365 days).  | 
**KeyValues** | Pointer to **map[string]string** | Optional flat data map written alongside the payload in KV-v2. Keys and values are caller-owned and never returned.  | [optional] 

## Methods

### NewCredentialRotateMaterial

`func NewCredentialRotateMaterial(payload string, ttlSeconds int64, ) *CredentialRotateMaterial`

NewCredentialRotateMaterial instantiates a new CredentialRotateMaterial object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCredentialRotateMaterialWithDefaults

`func NewCredentialRotateMaterialWithDefaults() *CredentialRotateMaterial`

NewCredentialRotateMaterialWithDefaults instantiates a new CredentialRotateMaterial object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPayload

`func (o *CredentialRotateMaterial) GetPayload() string`

GetPayload returns the Payload field if non-nil, zero value otherwise.

### GetPayloadOk

`func (o *CredentialRotateMaterial) GetPayloadOk() (*string, bool)`

GetPayloadOk returns a tuple with the Payload field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPayload

`func (o *CredentialRotateMaterial) SetPayload(v string)`

SetPayload sets Payload field to given value.


### GetTtlSeconds

`func (o *CredentialRotateMaterial) GetTtlSeconds() int64`

GetTtlSeconds returns the TtlSeconds field if non-nil, zero value otherwise.

### GetTtlSecondsOk

`func (o *CredentialRotateMaterial) GetTtlSecondsOk() (*int64, bool)`

GetTtlSecondsOk returns a tuple with the TtlSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTtlSeconds

`func (o *CredentialRotateMaterial) SetTtlSeconds(v int64)`

SetTtlSeconds sets TtlSeconds field to given value.


### GetKeyValues

`func (o *CredentialRotateMaterial) GetKeyValues() map[string]string`

GetKeyValues returns the KeyValues field if non-nil, zero value otherwise.

### GetKeyValuesOk

`func (o *CredentialRotateMaterial) GetKeyValuesOk() (*map[string]string, bool)`

GetKeyValuesOk returns a tuple with the KeyValues field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKeyValues

`func (o *CredentialRotateMaterial) SetKeyValues(v map[string]string)`

SetKeyValues sets KeyValues field to given value.

### HasKeyValues

`func (o *CredentialRotateMaterial) HasKeyValues() bool`

HasKeyValues returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


