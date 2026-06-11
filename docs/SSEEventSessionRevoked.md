# SSEEventSessionRevoked

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SessionId** | **string** | Identifier of the revoked Session (UUIDv7). | 
**Jti** | **string** | The revoked token&#39;s &#x60;jti&#x60;. Equals the session identifier.  | 
**RevokedAt** | **time.Time** | Revocation timestamp (UTC). | 
**RevokeReason** | [**RevokeReason**](RevokeReason.md) |  | 

## Methods

### NewSSEEventSessionRevoked

`func NewSSEEventSessionRevoked(sessionId string, jti string, revokedAt time.Time, revokeReason RevokeReason, ) *SSEEventSessionRevoked`

NewSSEEventSessionRevoked instantiates a new SSEEventSessionRevoked object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSSEEventSessionRevokedWithDefaults

`func NewSSEEventSessionRevokedWithDefaults() *SSEEventSessionRevoked`

NewSSEEventSessionRevokedWithDefaults instantiates a new SSEEventSessionRevoked object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSessionId

`func (o *SSEEventSessionRevoked) GetSessionId() string`

GetSessionId returns the SessionId field if non-nil, zero value otherwise.

### GetSessionIdOk

`func (o *SSEEventSessionRevoked) GetSessionIdOk() (*string, bool)`

GetSessionIdOk returns a tuple with the SessionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSessionId

`func (o *SSEEventSessionRevoked) SetSessionId(v string)`

SetSessionId sets SessionId field to given value.


### GetJti

`func (o *SSEEventSessionRevoked) GetJti() string`

GetJti returns the Jti field if non-nil, zero value otherwise.

### GetJtiOk

`func (o *SSEEventSessionRevoked) GetJtiOk() (*string, bool)`

GetJtiOk returns a tuple with the Jti field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetJti

`func (o *SSEEventSessionRevoked) SetJti(v string)`

SetJti sets Jti field to given value.


### GetRevokedAt

`func (o *SSEEventSessionRevoked) GetRevokedAt() time.Time`

GetRevokedAt returns the RevokedAt field if non-nil, zero value otherwise.

### GetRevokedAtOk

`func (o *SSEEventSessionRevoked) GetRevokedAtOk() (*time.Time, bool)`

GetRevokedAtOk returns a tuple with the RevokedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevokedAt

`func (o *SSEEventSessionRevoked) SetRevokedAt(v time.Time)`

SetRevokedAt sets RevokedAt field to given value.


### GetRevokeReason

`func (o *SSEEventSessionRevoked) GetRevokeReason() RevokeReason`

GetRevokeReason returns the RevokeReason field if non-nil, zero value otherwise.

### GetRevokeReasonOk

`func (o *SSEEventSessionRevoked) GetRevokeReasonOk() (*RevokeReason, bool)`

GetRevokeReasonOk returns a tuple with the RevokeReason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevokeReason

`func (o *SSEEventSessionRevoked) SetRevokeReason(v RevokeReason)`

SetRevokeReason sets RevokeReason field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


