# CloudCredentialResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Cloud Credential identifier (UUIDv7). | 
**CloudId** | **string** | Identifier of the owning Cloud — the residency pivot the ReBAC gate authorises against.  | 
**DisplayName** | **string** | Human-readable Cloud Credential name. | 
**Version** | **int64** | Monotonic broker-row version. Starts at 1 on issuance and increments on every rotate.  | 
**Status** | [**CloudCredentialStatus**](CloudCredentialStatus.md) |  | 
**ExpiresAt** | **time.Time** | Wall-clock expiry budget (UTC). | 
**RevokedAt** | Pointer to **time.Time** | Revocation timestamp (UTC). &#x60;null&#x60; until the credential is revoked by an operator.  | [optional] 
**ExpiredAt** | Pointer to **time.Time** | Expiry-observed timestamp (UTC). &#x60;null&#x60; until the sweeper marks the credential expired.  | [optional] 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). Bumped by every lifecycle mutator — rotate, revoke, expire.  | 

## Methods

### NewCloudCredentialResponse

`func NewCloudCredentialResponse(id string, cloudId string, displayName string, version int64, status CloudCredentialStatus, expiresAt time.Time, createdAt time.Time, updatedAt time.Time, ) *CloudCredentialResponse`

NewCloudCredentialResponse instantiates a new CloudCredentialResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudCredentialResponseWithDefaults

`func NewCloudCredentialResponseWithDefaults() *CloudCredentialResponse`

NewCloudCredentialResponseWithDefaults instantiates a new CloudCredentialResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *CloudCredentialResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *CloudCredentialResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *CloudCredentialResponse) SetId(v string)`

SetId sets Id field to given value.


### GetCloudId

`func (o *CloudCredentialResponse) GetCloudId() string`

GetCloudId returns the CloudId field if non-nil, zero value otherwise.

### GetCloudIdOk

`func (o *CloudCredentialResponse) GetCloudIdOk() (*string, bool)`

GetCloudIdOk returns a tuple with the CloudId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudId

`func (o *CloudCredentialResponse) SetCloudId(v string)`

SetCloudId sets CloudId field to given value.


### GetDisplayName

`func (o *CloudCredentialResponse) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *CloudCredentialResponse) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *CloudCredentialResponse) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetVersion

`func (o *CloudCredentialResponse) GetVersion() int64`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *CloudCredentialResponse) GetVersionOk() (*int64, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *CloudCredentialResponse) SetVersion(v int64)`

SetVersion sets Version field to given value.


### GetStatus

`func (o *CloudCredentialResponse) GetStatus() CloudCredentialStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *CloudCredentialResponse) GetStatusOk() (*CloudCredentialStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *CloudCredentialResponse) SetStatus(v CloudCredentialStatus)`

SetStatus sets Status field to given value.


### GetExpiresAt

`func (o *CloudCredentialResponse) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *CloudCredentialResponse) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *CloudCredentialResponse) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetRevokedAt

`func (o *CloudCredentialResponse) GetRevokedAt() time.Time`

GetRevokedAt returns the RevokedAt field if non-nil, zero value otherwise.

### GetRevokedAtOk

`func (o *CloudCredentialResponse) GetRevokedAtOk() (*time.Time, bool)`

GetRevokedAtOk returns a tuple with the RevokedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevokedAt

`func (o *CloudCredentialResponse) SetRevokedAt(v time.Time)`

SetRevokedAt sets RevokedAt field to given value.

### HasRevokedAt

`func (o *CloudCredentialResponse) HasRevokedAt() bool`

HasRevokedAt returns a boolean if a field has been set.

### GetExpiredAt

`func (o *CloudCredentialResponse) GetExpiredAt() time.Time`

GetExpiredAt returns the ExpiredAt field if non-nil, zero value otherwise.

### GetExpiredAtOk

`func (o *CloudCredentialResponse) GetExpiredAtOk() (*time.Time, bool)`

GetExpiredAtOk returns a tuple with the ExpiredAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiredAt

`func (o *CloudCredentialResponse) SetExpiredAt(v time.Time)`

SetExpiredAt sets ExpiredAt field to given value.

### HasExpiredAt

`func (o *CloudCredentialResponse) HasExpiredAt() bool`

HasExpiredAt returns a boolean if a field has been set.

### GetCreatedAt

`func (o *CloudCredentialResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *CloudCredentialResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *CloudCredentialResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *CloudCredentialResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *CloudCredentialResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *CloudCredentialResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


