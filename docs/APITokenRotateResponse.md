# APITokenRotateResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Token identifier (UUIDv7). | 
**Plaintext** | **string** | New psk-shaped plaintext; returned exactly once. | 
**EnvPrefix** | **string** | Environment segment embedded in the plaintext. | 
**ExpiresAt** | **time.Time** | Expiry timestamp of the new plaintext. | 
**RotationDeadline** | **time.Time** | Retirement deadline of the rotated-from plaintext. Matches the value advertised in the &#x60;Sunset&#x60; response header.  | 

## Methods

### NewAPITokenRotateResponse

`func NewAPITokenRotateResponse(id string, plaintext string, envPrefix string, expiresAt time.Time, rotationDeadline time.Time, ) *APITokenRotateResponse`

NewAPITokenRotateResponse instantiates a new APITokenRotateResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAPITokenRotateResponseWithDefaults

`func NewAPITokenRotateResponseWithDefaults() *APITokenRotateResponse`

NewAPITokenRotateResponseWithDefaults instantiates a new APITokenRotateResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *APITokenRotateResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *APITokenRotateResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *APITokenRotateResponse) SetId(v string)`

SetId sets Id field to given value.


### GetPlaintext

`func (o *APITokenRotateResponse) GetPlaintext() string`

GetPlaintext returns the Plaintext field if non-nil, zero value otherwise.

### GetPlaintextOk

`func (o *APITokenRotateResponse) GetPlaintextOk() (*string, bool)`

GetPlaintextOk returns a tuple with the Plaintext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPlaintext

`func (o *APITokenRotateResponse) SetPlaintext(v string)`

SetPlaintext sets Plaintext field to given value.


### GetEnvPrefix

`func (o *APITokenRotateResponse) GetEnvPrefix() string`

GetEnvPrefix returns the EnvPrefix field if non-nil, zero value otherwise.

### GetEnvPrefixOk

`func (o *APITokenRotateResponse) GetEnvPrefixOk() (*string, bool)`

GetEnvPrefixOk returns a tuple with the EnvPrefix field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnvPrefix

`func (o *APITokenRotateResponse) SetEnvPrefix(v string)`

SetEnvPrefix sets EnvPrefix field to given value.


### GetExpiresAt

`func (o *APITokenRotateResponse) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *APITokenRotateResponse) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *APITokenRotateResponse) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetRotationDeadline

`func (o *APITokenRotateResponse) GetRotationDeadline() time.Time`

GetRotationDeadline returns the RotationDeadline field if non-nil, zero value otherwise.

### GetRotationDeadlineOk

`func (o *APITokenRotateResponse) GetRotationDeadlineOk() (*time.Time, bool)`

GetRotationDeadlineOk returns a tuple with the RotationDeadline field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRotationDeadline

`func (o *APITokenRotateResponse) SetRotationDeadline(v time.Time)`

SetRotationDeadline sets RotationDeadline field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


