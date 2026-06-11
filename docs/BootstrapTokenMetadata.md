# BootstrapTokenMetadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | BootstrapToken identifier (UUIDv7). | 
**ProjectId** | **string** | Project the token is scoped to. | 
**Kind** | [**BootstrapTokenMetadataKind**](BootstrapTokenMetadataKind.md) |  | 
**EnvPrefix** | **string** | Environment segment encoded in the plaintext at issuance time.  | 
**IssuedAt** | **time.Time** | Issuance timestamp (UTC). | 
**ExpiresAt** | **time.Time** | Absolute expiry timestamp (UTC). | 
**ConsumedAt** | Pointer to **time.Time** | Redemption timestamp, or null when the token has not yet been redeemed. A non-null value is terminal — a consumed token cannot be redeemed again.  | [optional] 
**RevokedAt** | Pointer to **time.Time** | Revocation timestamp, or null when the token is still live. A non-null value is terminal — a revoked token rejects redemption regardless of expiry.  | [optional] 
**IssuedByUserId** | **string** | User who issued the token.  | 

## Methods

### NewBootstrapTokenMetadata

`func NewBootstrapTokenMetadata(id string, projectId string, kind BootstrapTokenMetadataKind, envPrefix string, issuedAt time.Time, expiresAt time.Time, issuedByUserId string, ) *BootstrapTokenMetadata`

NewBootstrapTokenMetadata instantiates a new BootstrapTokenMetadata object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBootstrapTokenMetadataWithDefaults

`func NewBootstrapTokenMetadataWithDefaults() *BootstrapTokenMetadata`

NewBootstrapTokenMetadataWithDefaults instantiates a new BootstrapTokenMetadata object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *BootstrapTokenMetadata) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *BootstrapTokenMetadata) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *BootstrapTokenMetadata) SetId(v string)`

SetId sets Id field to given value.


### GetProjectId

`func (o *BootstrapTokenMetadata) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *BootstrapTokenMetadata) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *BootstrapTokenMetadata) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetKind

`func (o *BootstrapTokenMetadata) GetKind() BootstrapTokenMetadataKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *BootstrapTokenMetadata) GetKindOk() (*BootstrapTokenMetadataKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *BootstrapTokenMetadata) SetKind(v BootstrapTokenMetadataKind)`

SetKind sets Kind field to given value.


### GetEnvPrefix

`func (o *BootstrapTokenMetadata) GetEnvPrefix() string`

GetEnvPrefix returns the EnvPrefix field if non-nil, zero value otherwise.

### GetEnvPrefixOk

`func (o *BootstrapTokenMetadata) GetEnvPrefixOk() (*string, bool)`

GetEnvPrefixOk returns a tuple with the EnvPrefix field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnvPrefix

`func (o *BootstrapTokenMetadata) SetEnvPrefix(v string)`

SetEnvPrefix sets EnvPrefix field to given value.


### GetIssuedAt

`func (o *BootstrapTokenMetadata) GetIssuedAt() time.Time`

GetIssuedAt returns the IssuedAt field if non-nil, zero value otherwise.

### GetIssuedAtOk

`func (o *BootstrapTokenMetadata) GetIssuedAtOk() (*time.Time, bool)`

GetIssuedAtOk returns a tuple with the IssuedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIssuedAt

`func (o *BootstrapTokenMetadata) SetIssuedAt(v time.Time)`

SetIssuedAt sets IssuedAt field to given value.


### GetExpiresAt

`func (o *BootstrapTokenMetadata) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *BootstrapTokenMetadata) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *BootstrapTokenMetadata) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetConsumedAt

`func (o *BootstrapTokenMetadata) GetConsumedAt() time.Time`

GetConsumedAt returns the ConsumedAt field if non-nil, zero value otherwise.

### GetConsumedAtOk

`func (o *BootstrapTokenMetadata) GetConsumedAtOk() (*time.Time, bool)`

GetConsumedAtOk returns a tuple with the ConsumedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetConsumedAt

`func (o *BootstrapTokenMetadata) SetConsumedAt(v time.Time)`

SetConsumedAt sets ConsumedAt field to given value.

### HasConsumedAt

`func (o *BootstrapTokenMetadata) HasConsumedAt() bool`

HasConsumedAt returns a boolean if a field has been set.

### GetRevokedAt

`func (o *BootstrapTokenMetadata) GetRevokedAt() time.Time`

GetRevokedAt returns the RevokedAt field if non-nil, zero value otherwise.

### GetRevokedAtOk

`func (o *BootstrapTokenMetadata) GetRevokedAtOk() (*time.Time, bool)`

GetRevokedAtOk returns a tuple with the RevokedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevokedAt

`func (o *BootstrapTokenMetadata) SetRevokedAt(v time.Time)`

SetRevokedAt sets RevokedAt field to given value.

### HasRevokedAt

`func (o *BootstrapTokenMetadata) HasRevokedAt() bool`

HasRevokedAt returns a boolean if a field has been set.

### GetIssuedByUserId

`func (o *BootstrapTokenMetadata) GetIssuedByUserId() string`

GetIssuedByUserId returns the IssuedByUserId field if non-nil, zero value otherwise.

### GetIssuedByUserIdOk

`func (o *BootstrapTokenMetadata) GetIssuedByUserIdOk() (*string, bool)`

GetIssuedByUserIdOk returns a tuple with the IssuedByUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIssuedByUserId

`func (o *BootstrapTokenMetadata) SetIssuedByUserId(v string)`

SetIssuedByUserId sets IssuedByUserId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


