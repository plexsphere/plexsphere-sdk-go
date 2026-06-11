# InvitationCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ExternalSubject** | **string** | IdP-side subject identifier (typically the OIDC &#x60;sub&#x60; claim or operator-known login name) the invitation is staged for. Whitespace-only is rejected by the aggregate .  | 
**TtlSeconds** | Pointer to **int32** | Lifetime of the invitation in seconds, applied to &#x60;created_at&#x60; to derive &#x60;expires_at&#x60;. Out-of-range values surface as &#x60;400 invalid_ttl&#x60;. Defaults to 86400 (24h); ceiling is 7 days.  | [optional] [default to 86400]
**InitialTuples** | Pointer to [**[]InvitationInitialTuple**](InvitationInitialTuple.md) | Optional bounded list (max 32) of relation tuples to write into SpiceDB atomically when the invitation is accepted. Exceeding the cap surfaces as &#x60;422 too_many_initial_tuples&#x60;.  | [optional] 

## Methods

### NewInvitationCreateRequest

`func NewInvitationCreateRequest(externalSubject string, ) *InvitationCreateRequest`

NewInvitationCreateRequest instantiates a new InvitationCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewInvitationCreateRequestWithDefaults

`func NewInvitationCreateRequestWithDefaults() *InvitationCreateRequest`

NewInvitationCreateRequestWithDefaults instantiates a new InvitationCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetExternalSubject

`func (o *InvitationCreateRequest) GetExternalSubject() string`

GetExternalSubject returns the ExternalSubject field if non-nil, zero value otherwise.

### GetExternalSubjectOk

`func (o *InvitationCreateRequest) GetExternalSubjectOk() (*string, bool)`

GetExternalSubjectOk returns a tuple with the ExternalSubject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExternalSubject

`func (o *InvitationCreateRequest) SetExternalSubject(v string)`

SetExternalSubject sets ExternalSubject field to given value.


### GetTtlSeconds

`func (o *InvitationCreateRequest) GetTtlSeconds() int32`

GetTtlSeconds returns the TtlSeconds field if non-nil, zero value otherwise.

### GetTtlSecondsOk

`func (o *InvitationCreateRequest) GetTtlSecondsOk() (*int32, bool)`

GetTtlSecondsOk returns a tuple with the TtlSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTtlSeconds

`func (o *InvitationCreateRequest) SetTtlSeconds(v int32)`

SetTtlSeconds sets TtlSeconds field to given value.

### HasTtlSeconds

`func (o *InvitationCreateRequest) HasTtlSeconds() bool`

HasTtlSeconds returns a boolean if a field has been set.

### GetInitialTuples

`func (o *InvitationCreateRequest) GetInitialTuples() []InvitationInitialTuple`

GetInitialTuples returns the InitialTuples field if non-nil, zero value otherwise.

### GetInitialTuplesOk

`func (o *InvitationCreateRequest) GetInitialTuplesOk() (*[]InvitationInitialTuple, bool)`

GetInitialTuplesOk returns a tuple with the InitialTuples field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInitialTuples

`func (o *InvitationCreateRequest) SetInitialTuples(v []InvitationInitialTuple)`

SetInitialTuples sets InitialTuples field to given value.

### HasInitialTuples

`func (o *InvitationCreateRequest) HasInitialTuples() bool`

HasInitialTuples returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


