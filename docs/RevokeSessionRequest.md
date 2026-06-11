# RevokeSessionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RevokeReason** | [**RevokeReason**](RevokeReason.md) | Reason for the revocation. Only the operator-driven values are accepted here — the sweeper reasons (&#x60;ttl_expired&#x60;, &#x60;idle_timeout&#x60;) are set internally, never by this call.  | 

## Methods

### NewRevokeSessionRequest

`func NewRevokeSessionRequest(revokeReason RevokeReason, ) *RevokeSessionRequest`

NewRevokeSessionRequest instantiates a new RevokeSessionRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRevokeSessionRequestWithDefaults

`func NewRevokeSessionRequestWithDefaults() *RevokeSessionRequest`

NewRevokeSessionRequestWithDefaults instantiates a new RevokeSessionRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetRevokeReason

`func (o *RevokeSessionRequest) GetRevokeReason() RevokeReason`

GetRevokeReason returns the RevokeReason field if non-nil, zero value otherwise.

### GetRevokeReasonOk

`func (o *RevokeSessionRequest) GetRevokeReasonOk() (*RevokeReason, bool)`

GetRevokeReasonOk returns a tuple with the RevokeReason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevokeReason

`func (o *RevokeSessionRequest) SetRevokeReason(v RevokeReason)`

SetRevokeReason sets RevokeReason field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


