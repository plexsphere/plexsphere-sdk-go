# CredentialResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Credential identifier (UUIDv7). | 
**ProjectId** | **string** | Identifier of the owning Project — the residency pivot the ReBAC gate authorises against.  | 
**Version** | **int64** | Monotonic broker-row version. Starts at 1 on issuance and increments on every rotate.  | 
**Status** | [**CloudCredentialStatus**](CloudCredentialStatus.md) | Derived lifecycle status of the credential. &#x60;revoked&#x60; when &#x60;revoked_at&#x60; is set; otherwise &#x60;expired&#x60; when &#x60;expired_at&#x60; is set or &#x60;expires_at&#x60; is in the past; otherwise &#x60;active&#x60;. Computed by the read surface from the lifecycle timestamps — it is not a stored column. Reuses the shared &#x60;CloudCredentialStatus&#x60; closed enum (identical active/expired/revoked vocabulary and precedence) rather than declaring a byte-identical parallel enum.  | 
**ExpiresAt** | **time.Time** | Wall-clock expiry budget (UTC). | 
**RevokedAt** | Pointer to **time.Time** | Revocation timestamp (UTC). &#x60;null&#x60; until the credential is revoked by an operator.  | [optional] 
**ExpiredAt** | Pointer to **time.Time** | Expiry-observed timestamp (UTC). &#x60;null&#x60; until the sweeper marks the credential expired.  | [optional] 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). Bumped by every lifecycle mutator — rotate, revoke, expire.  | 

## Methods

### NewCredentialResponse

`func NewCredentialResponse(id string, projectId string, version int64, status CloudCredentialStatus, expiresAt time.Time, createdAt time.Time, updatedAt time.Time, ) *CredentialResponse`

NewCredentialResponse instantiates a new CredentialResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCredentialResponseWithDefaults

`func NewCredentialResponseWithDefaults() *CredentialResponse`

NewCredentialResponseWithDefaults instantiates a new CredentialResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *CredentialResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *CredentialResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *CredentialResponse) SetId(v string)`

SetId sets Id field to given value.


### GetProjectId

`func (o *CredentialResponse) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *CredentialResponse) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *CredentialResponse) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetVersion

`func (o *CredentialResponse) GetVersion() int64`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *CredentialResponse) GetVersionOk() (*int64, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *CredentialResponse) SetVersion(v int64)`

SetVersion sets Version field to given value.


### GetStatus

`func (o *CredentialResponse) GetStatus() CloudCredentialStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *CredentialResponse) GetStatusOk() (*CloudCredentialStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *CredentialResponse) SetStatus(v CloudCredentialStatus)`

SetStatus sets Status field to given value.


### GetExpiresAt

`func (o *CredentialResponse) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *CredentialResponse) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *CredentialResponse) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetRevokedAt

`func (o *CredentialResponse) GetRevokedAt() time.Time`

GetRevokedAt returns the RevokedAt field if non-nil, zero value otherwise.

### GetRevokedAtOk

`func (o *CredentialResponse) GetRevokedAtOk() (*time.Time, bool)`

GetRevokedAtOk returns a tuple with the RevokedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevokedAt

`func (o *CredentialResponse) SetRevokedAt(v time.Time)`

SetRevokedAt sets RevokedAt field to given value.

### HasRevokedAt

`func (o *CredentialResponse) HasRevokedAt() bool`

HasRevokedAt returns a boolean if a field has been set.

### GetExpiredAt

`func (o *CredentialResponse) GetExpiredAt() time.Time`

GetExpiredAt returns the ExpiredAt field if non-nil, zero value otherwise.

### GetExpiredAtOk

`func (o *CredentialResponse) GetExpiredAtOk() (*time.Time, bool)`

GetExpiredAtOk returns a tuple with the ExpiredAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiredAt

`func (o *CredentialResponse) SetExpiredAt(v time.Time)`

SetExpiredAt sets ExpiredAt field to given value.

### HasExpiredAt

`func (o *CredentialResponse) HasExpiredAt() bool`

HasExpiredAt returns a boolean if a field has been set.

### GetCreatedAt

`func (o *CredentialResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *CredentialResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *CredentialResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *CredentialResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *CredentialResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *CredentialResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


