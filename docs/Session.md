# Session

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Session identifier (UUIDv7). Equals the issued token&#39;s &#x60;jti&#x60;.  | 
**ProjectId** | **string** | Identifier of the owning Project (UUIDv7). | 
**DomainId** | **string** | Identifier of the owning Domain (UUIDv7) — the residency pivot the per-Domain session policy and concurrency budgets count against.  | 
**ResourceId** | **string** | Identifier of the targeted Resource (UUIDv7). | 
**IdentityId** | **string** | Identifier of the Identity the Session was issued to. | 
**Kind** | [**SessionKind**](SessionKind.md) |  | 
**Status** | [**SessionStatus**](SessionStatus.md) | Aggregate lifecycle status of the Session. | 
**IssuedAt** | **time.Time** | Issuance timestamp (UTC). | 
**ExpiresAt** | **time.Time** | Expiry timestamp (UTC) — issuance time plus the clamped TTL.  | 
**LastActiveAt** | **time.Time** | Timestamp of the most recent recorded activity (UTC); drives the idle-timeout sweeper.  | 
**IdleTimeoutSeconds** | Pointer to **int32** | Idle window in whole seconds — the Session is reclaimed when &#x60;last_active_at + idle_timeout&#x60; passes.  | [optional] 
**RevokedAt** | Pointer to **time.Time** | Revocation timestamp (UTC); &#x60;null&#x60; while the Session is live.  | [optional] 
**RevokeReason** | Pointer to [**RevokeReason**](RevokeReason.md) | Reason the Session was revoked. Omitted while the Session is live.  | [optional] 
**Target** | [**SessionTarget**](SessionTarget.md) |  | 

## Methods

### NewSession

`func NewSession(id string, projectId string, domainId string, resourceId string, identityId string, kind SessionKind, status SessionStatus, issuedAt time.Time, expiresAt time.Time, lastActiveAt time.Time, target SessionTarget, ) *Session`

NewSession instantiates a new Session object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSessionWithDefaults

`func NewSessionWithDefaults() *Session`

NewSessionWithDefaults instantiates a new Session object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *Session) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *Session) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *Session) SetId(v string)`

SetId sets Id field to given value.


### GetProjectId

`func (o *Session) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *Session) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *Session) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetDomainId

`func (o *Session) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *Session) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *Session) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetResourceId

`func (o *Session) GetResourceId() string`

GetResourceId returns the ResourceId field if non-nil, zero value otherwise.

### GetResourceIdOk

`func (o *Session) GetResourceIdOk() (*string, bool)`

GetResourceIdOk returns a tuple with the ResourceId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResourceId

`func (o *Session) SetResourceId(v string)`

SetResourceId sets ResourceId field to given value.


### GetIdentityId

`func (o *Session) GetIdentityId() string`

GetIdentityId returns the IdentityId field if non-nil, zero value otherwise.

### GetIdentityIdOk

`func (o *Session) GetIdentityIdOk() (*string, bool)`

GetIdentityIdOk returns a tuple with the IdentityId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdentityId

`func (o *Session) SetIdentityId(v string)`

SetIdentityId sets IdentityId field to given value.


### GetKind

`func (o *Session) GetKind() SessionKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *Session) GetKindOk() (*SessionKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *Session) SetKind(v SessionKind)`

SetKind sets Kind field to given value.


### GetStatus

`func (o *Session) GetStatus() SessionStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *Session) GetStatusOk() (*SessionStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *Session) SetStatus(v SessionStatus)`

SetStatus sets Status field to given value.


### GetIssuedAt

`func (o *Session) GetIssuedAt() time.Time`

GetIssuedAt returns the IssuedAt field if non-nil, zero value otherwise.

### GetIssuedAtOk

`func (o *Session) GetIssuedAtOk() (*time.Time, bool)`

GetIssuedAtOk returns a tuple with the IssuedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIssuedAt

`func (o *Session) SetIssuedAt(v time.Time)`

SetIssuedAt sets IssuedAt field to given value.


### GetExpiresAt

`func (o *Session) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *Session) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *Session) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetLastActiveAt

`func (o *Session) GetLastActiveAt() time.Time`

GetLastActiveAt returns the LastActiveAt field if non-nil, zero value otherwise.

### GetLastActiveAtOk

`func (o *Session) GetLastActiveAtOk() (*time.Time, bool)`

GetLastActiveAtOk returns a tuple with the LastActiveAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLastActiveAt

`func (o *Session) SetLastActiveAt(v time.Time)`

SetLastActiveAt sets LastActiveAt field to given value.


### GetIdleTimeoutSeconds

`func (o *Session) GetIdleTimeoutSeconds() int32`

GetIdleTimeoutSeconds returns the IdleTimeoutSeconds field if non-nil, zero value otherwise.

### GetIdleTimeoutSecondsOk

`func (o *Session) GetIdleTimeoutSecondsOk() (*int32, bool)`

GetIdleTimeoutSecondsOk returns a tuple with the IdleTimeoutSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdleTimeoutSeconds

`func (o *Session) SetIdleTimeoutSeconds(v int32)`

SetIdleTimeoutSeconds sets IdleTimeoutSeconds field to given value.

### HasIdleTimeoutSeconds

`func (o *Session) HasIdleTimeoutSeconds() bool`

HasIdleTimeoutSeconds returns a boolean if a field has been set.

### GetRevokedAt

`func (o *Session) GetRevokedAt() time.Time`

GetRevokedAt returns the RevokedAt field if non-nil, zero value otherwise.

### GetRevokedAtOk

`func (o *Session) GetRevokedAtOk() (*time.Time, bool)`

GetRevokedAtOk returns a tuple with the RevokedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevokedAt

`func (o *Session) SetRevokedAt(v time.Time)`

SetRevokedAt sets RevokedAt field to given value.

### HasRevokedAt

`func (o *Session) HasRevokedAt() bool`

HasRevokedAt returns a boolean if a field has been set.

### GetRevokeReason

`func (o *Session) GetRevokeReason() RevokeReason`

GetRevokeReason returns the RevokeReason field if non-nil, zero value otherwise.

### GetRevokeReasonOk

`func (o *Session) GetRevokeReasonOk() (*RevokeReason, bool)`

GetRevokeReasonOk returns a tuple with the RevokeReason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevokeReason

`func (o *Session) SetRevokeReason(v RevokeReason)`

SetRevokeReason sets RevokeReason field to given value.

### HasRevokeReason

`func (o *Session) HasRevokeReason() bool`

HasRevokeReason returns a boolean if a field has been set.

### GetTarget

`func (o *Session) GetTarget() SessionTarget`

GetTarget returns the Target field if non-nil, zero value otherwise.

### GetTargetOk

`func (o *Session) GetTargetOk() (*SessionTarget, bool)`

GetTargetOk returns a tuple with the Target field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTarget

`func (o *Session) SetTarget(v SessionTarget)`

SetTarget sets Target field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


