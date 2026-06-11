# APITokenIssueResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Token identifier (UUIDv7). | 
**Plaintext** | **string** | The psk-shaped plaintext; returned exactly once. | 
**EnvPrefix** | **string** | Environment segment embedded in the plaintext. | 
**ExpiresAt** | **time.Time** | RFC 3339 expiry timestamp. | 

## Methods

### NewAPITokenIssueResponse

`func NewAPITokenIssueResponse(id string, plaintext string, envPrefix string, expiresAt time.Time, ) *APITokenIssueResponse`

NewAPITokenIssueResponse instantiates a new APITokenIssueResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAPITokenIssueResponseWithDefaults

`func NewAPITokenIssueResponseWithDefaults() *APITokenIssueResponse`

NewAPITokenIssueResponseWithDefaults instantiates a new APITokenIssueResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *APITokenIssueResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *APITokenIssueResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *APITokenIssueResponse) SetId(v string)`

SetId sets Id field to given value.


### GetPlaintext

`func (o *APITokenIssueResponse) GetPlaintext() string`

GetPlaintext returns the Plaintext field if non-nil, zero value otherwise.

### GetPlaintextOk

`func (o *APITokenIssueResponse) GetPlaintextOk() (*string, bool)`

GetPlaintextOk returns a tuple with the Plaintext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPlaintext

`func (o *APITokenIssueResponse) SetPlaintext(v string)`

SetPlaintext sets Plaintext field to given value.


### GetEnvPrefix

`func (o *APITokenIssueResponse) GetEnvPrefix() string`

GetEnvPrefix returns the EnvPrefix field if non-nil, zero value otherwise.

### GetEnvPrefixOk

`func (o *APITokenIssueResponse) GetEnvPrefixOk() (*string, bool)`

GetEnvPrefixOk returns a tuple with the EnvPrefix field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnvPrefix

`func (o *APITokenIssueResponse) SetEnvPrefix(v string)`

SetEnvPrefix sets EnvPrefix field to given value.


### GetExpiresAt

`func (o *APITokenIssueResponse) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *APITokenIssueResponse) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *APITokenIssueResponse) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


