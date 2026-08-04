# NodeStateSession

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SessionId** | **string** | Identifier of the Session (UUIDv7). | 
**Jti** | **string** | The issued token&#39;s &#x60;jti&#x60;. Equals the session identifier.  | 
**Kind** | [**SessionKind**](SessionKind.md) |  | 
**Target** | [**SessionTarget**](SessionTarget.md) |  | 
**ExpiresAt** | **time.Time** | Expiry timestamp (UTC) the listener tears down at. | 
**IdleTimeoutSeconds** | Pointer to **int32** | Idle window in whole seconds the listener applies locally.  | [optional] 

## Methods

### NewNodeStateSession

`func NewNodeStateSession(sessionId string, jti string, kind SessionKind, target SessionTarget, expiresAt time.Time, ) *NodeStateSession`

NewNodeStateSession instantiates a new NodeStateSession object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateSessionWithDefaults

`func NewNodeStateSessionWithDefaults() *NodeStateSession`

NewNodeStateSessionWithDefaults instantiates a new NodeStateSession object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSessionId

`func (o *NodeStateSession) GetSessionId() string`

GetSessionId returns the SessionId field if non-nil, zero value otherwise.

### GetSessionIdOk

`func (o *NodeStateSession) GetSessionIdOk() (*string, bool)`

GetSessionIdOk returns a tuple with the SessionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSessionId

`func (o *NodeStateSession) SetSessionId(v string)`

SetSessionId sets SessionId field to given value.


### GetJti

`func (o *NodeStateSession) GetJti() string`

GetJti returns the Jti field if non-nil, zero value otherwise.

### GetJtiOk

`func (o *NodeStateSession) GetJtiOk() (*string, bool)`

GetJtiOk returns a tuple with the Jti field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetJti

`func (o *NodeStateSession) SetJti(v string)`

SetJti sets Jti field to given value.


### GetKind

`func (o *NodeStateSession) GetKind() SessionKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *NodeStateSession) GetKindOk() (*SessionKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *NodeStateSession) SetKind(v SessionKind)`

SetKind sets Kind field to given value.


### GetTarget

`func (o *NodeStateSession) GetTarget() SessionTarget`

GetTarget returns the Target field if non-nil, zero value otherwise.

### GetTargetOk

`func (o *NodeStateSession) GetTargetOk() (*SessionTarget, bool)`

GetTargetOk returns a tuple with the Target field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTarget

`func (o *NodeStateSession) SetTarget(v SessionTarget)`

SetTarget sets Target field to given value.


### GetExpiresAt

`func (o *NodeStateSession) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *NodeStateSession) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *NodeStateSession) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetIdleTimeoutSeconds

`func (o *NodeStateSession) GetIdleTimeoutSeconds() int32`

GetIdleTimeoutSeconds returns the IdleTimeoutSeconds field if non-nil, zero value otherwise.

### GetIdleTimeoutSecondsOk

`func (o *NodeStateSession) GetIdleTimeoutSecondsOk() (*int32, bool)`

GetIdleTimeoutSecondsOk returns a tuple with the IdleTimeoutSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdleTimeoutSeconds

`func (o *NodeStateSession) SetIdleTimeoutSeconds(v int32)`

SetIdleTimeoutSeconds sets IdleTimeoutSeconds field to given value.

### HasIdleTimeoutSeconds

`func (o *NodeStateSession) HasIdleTimeoutSeconds() bool`

HasIdleTimeoutSeconds returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


