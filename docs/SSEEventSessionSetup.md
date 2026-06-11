# SSEEventSessionSetup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SessionId** | **string** | Identifier of the Session being set up (UUIDv7). | 
**Jti** | **string** | The issued token&#39;s &#x60;jti&#x60;. Equals the session identifier.  | 
**Kind** | [**SessionKind**](SessionKind.md) |  | 
**Target** | [**SessionTarget**](SessionTarget.md) |  | 
**ExpiresAt** | **time.Time** | Expiry timestamp (UTC) the listener tears down at. | 
**IdleTimeoutSeconds** | Pointer to **int32** | Idle window in whole seconds the listener applies locally.  | [optional] 
**CallbackUrl** | **string** | The per-session callback URL under &#x60;/v1/nodes/{id}/sessions/{session_id}&#x60; the Node posts per-kind activity to.  | 

## Methods

### NewSSEEventSessionSetup

`func NewSSEEventSessionSetup(sessionId string, jti string, kind SessionKind, target SessionTarget, expiresAt time.Time, callbackUrl string, ) *SSEEventSessionSetup`

NewSSEEventSessionSetup instantiates a new SSEEventSessionSetup object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSSEEventSessionSetupWithDefaults

`func NewSSEEventSessionSetupWithDefaults() *SSEEventSessionSetup`

NewSSEEventSessionSetupWithDefaults instantiates a new SSEEventSessionSetup object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSessionId

`func (o *SSEEventSessionSetup) GetSessionId() string`

GetSessionId returns the SessionId field if non-nil, zero value otherwise.

### GetSessionIdOk

`func (o *SSEEventSessionSetup) GetSessionIdOk() (*string, bool)`

GetSessionIdOk returns a tuple with the SessionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSessionId

`func (o *SSEEventSessionSetup) SetSessionId(v string)`

SetSessionId sets SessionId field to given value.


### GetJti

`func (o *SSEEventSessionSetup) GetJti() string`

GetJti returns the Jti field if non-nil, zero value otherwise.

### GetJtiOk

`func (o *SSEEventSessionSetup) GetJtiOk() (*string, bool)`

GetJtiOk returns a tuple with the Jti field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetJti

`func (o *SSEEventSessionSetup) SetJti(v string)`

SetJti sets Jti field to given value.


### GetKind

`func (o *SSEEventSessionSetup) GetKind() SessionKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *SSEEventSessionSetup) GetKindOk() (*SessionKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *SSEEventSessionSetup) SetKind(v SessionKind)`

SetKind sets Kind field to given value.


### GetTarget

`func (o *SSEEventSessionSetup) GetTarget() SessionTarget`

GetTarget returns the Target field if non-nil, zero value otherwise.

### GetTargetOk

`func (o *SSEEventSessionSetup) GetTargetOk() (*SessionTarget, bool)`

GetTargetOk returns a tuple with the Target field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTarget

`func (o *SSEEventSessionSetup) SetTarget(v SessionTarget)`

SetTarget sets Target field to given value.


### GetExpiresAt

`func (o *SSEEventSessionSetup) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *SSEEventSessionSetup) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *SSEEventSessionSetup) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetIdleTimeoutSeconds

`func (o *SSEEventSessionSetup) GetIdleTimeoutSeconds() int32`

GetIdleTimeoutSeconds returns the IdleTimeoutSeconds field if non-nil, zero value otherwise.

### GetIdleTimeoutSecondsOk

`func (o *SSEEventSessionSetup) GetIdleTimeoutSecondsOk() (*int32, bool)`

GetIdleTimeoutSecondsOk returns a tuple with the IdleTimeoutSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdleTimeoutSeconds

`func (o *SSEEventSessionSetup) SetIdleTimeoutSeconds(v int32)`

SetIdleTimeoutSeconds sets IdleTimeoutSeconds field to given value.

### HasIdleTimeoutSeconds

`func (o *SSEEventSessionSetup) HasIdleTimeoutSeconds() bool`

HasIdleTimeoutSeconds returns a boolean if a field has been set.

### GetCallbackUrl

`func (o *SSEEventSessionSetup) GetCallbackUrl() string`

GetCallbackUrl returns the CallbackUrl field if non-nil, zero value otherwise.

### GetCallbackUrlOk

`func (o *SSEEventSessionSetup) GetCallbackUrlOk() (*string, bool)`

GetCallbackUrlOk returns a tuple with the CallbackUrl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCallbackUrl

`func (o *SSEEventSessionSetup) SetCallbackUrl(v string)`

SetCallbackUrl sets CallbackUrl field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


