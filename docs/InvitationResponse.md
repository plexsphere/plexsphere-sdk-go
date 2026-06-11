# InvitationResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Invitation identifier (UUIDv7). | 
**DomainId** | **string** | Owning Domain identifier (UUIDv7). | 
**ExternalSubjectPseudonym** | **string** | Per-Domain pseudonym of the IdP-side &#x60;external_subject&#x60; (32 bytes, lowercase hex). The plaintext form is never echoed on the invitation read surface.  | 
**Status** | [**InvitationStatus**](InvitationStatus.md) |  | 
**ExpiresAt** | **time.Time** | Wall-clock timestamp the invitation transitions to &#x60;expired&#x60; if no Accept / Revoke has fired. Derived from &#x60;created_at + ttl_seconds&#x60;. The expiry sweeper flips elapsed pending rows to &#x60;expired&#x60; and appends the matching outbox event.  | 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**AcceptedAt** | Pointer to **time.Time** | Timestamp the invitation transitioned to &#x60;accepted&#x60;. Populated only when &#x60;status &#x3D;&#x3D; accepted&#x60;.  | [optional] 
**AcceptedUserId** | Pointer to **string** | Identifier of the User aggregate the OIDC sign-in callback resolved when accepting the invitation. Populated only when &#x60;status &#x3D;&#x3D; accepted&#x60;.  | [optional] 
**RevokedAt** | Pointer to **time.Time** | Timestamp the invitation transitioned to &#x60;revoked&#x60;. Populated only when &#x60;status &#x3D;&#x3D; revoked&#x60;.  | [optional] 
**ExpiredAt** | Pointer to **time.Time** | Timestamp the expiry sweeper flipped the row to &#x60;expired&#x60;. Populated only when &#x60;status &#x3D;&#x3D; expired&#x60; .  | [optional] 
**InitialTuples** | Pointer to [**[]InvitationInitialTuple**](InvitationInitialTuple.md) | Bounded list of relation tuples staged on the invitation. Returned verbatim from the persistence layer so the operator can preview which tuples will land on Accept .  | [optional] 

## Methods

### NewInvitationResponse

`func NewInvitationResponse(id string, domainId string, externalSubjectPseudonym string, status InvitationStatus, expiresAt time.Time, createdAt time.Time, ) *InvitationResponse`

NewInvitationResponse instantiates a new InvitationResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewInvitationResponseWithDefaults

`func NewInvitationResponseWithDefaults() *InvitationResponse`

NewInvitationResponseWithDefaults instantiates a new InvitationResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *InvitationResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *InvitationResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *InvitationResponse) SetId(v string)`

SetId sets Id field to given value.


### GetDomainId

`func (o *InvitationResponse) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *InvitationResponse) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *InvitationResponse) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetExternalSubjectPseudonym

`func (o *InvitationResponse) GetExternalSubjectPseudonym() string`

GetExternalSubjectPseudonym returns the ExternalSubjectPseudonym field if non-nil, zero value otherwise.

### GetExternalSubjectPseudonymOk

`func (o *InvitationResponse) GetExternalSubjectPseudonymOk() (*string, bool)`

GetExternalSubjectPseudonymOk returns a tuple with the ExternalSubjectPseudonym field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExternalSubjectPseudonym

`func (o *InvitationResponse) SetExternalSubjectPseudonym(v string)`

SetExternalSubjectPseudonym sets ExternalSubjectPseudonym field to given value.


### GetStatus

`func (o *InvitationResponse) GetStatus() InvitationStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *InvitationResponse) GetStatusOk() (*InvitationStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *InvitationResponse) SetStatus(v InvitationStatus)`

SetStatus sets Status field to given value.


### GetExpiresAt

`func (o *InvitationResponse) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *InvitationResponse) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *InvitationResponse) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetCreatedAt

`func (o *InvitationResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *InvitationResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *InvitationResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetAcceptedAt

`func (o *InvitationResponse) GetAcceptedAt() time.Time`

GetAcceptedAt returns the AcceptedAt field if non-nil, zero value otherwise.

### GetAcceptedAtOk

`func (o *InvitationResponse) GetAcceptedAtOk() (*time.Time, bool)`

GetAcceptedAtOk returns a tuple with the AcceptedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcceptedAt

`func (o *InvitationResponse) SetAcceptedAt(v time.Time)`

SetAcceptedAt sets AcceptedAt field to given value.

### HasAcceptedAt

`func (o *InvitationResponse) HasAcceptedAt() bool`

HasAcceptedAt returns a boolean if a field has been set.

### GetAcceptedUserId

`func (o *InvitationResponse) GetAcceptedUserId() string`

GetAcceptedUserId returns the AcceptedUserId field if non-nil, zero value otherwise.

### GetAcceptedUserIdOk

`func (o *InvitationResponse) GetAcceptedUserIdOk() (*string, bool)`

GetAcceptedUserIdOk returns a tuple with the AcceptedUserId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcceptedUserId

`func (o *InvitationResponse) SetAcceptedUserId(v string)`

SetAcceptedUserId sets AcceptedUserId field to given value.

### HasAcceptedUserId

`func (o *InvitationResponse) HasAcceptedUserId() bool`

HasAcceptedUserId returns a boolean if a field has been set.

### GetRevokedAt

`func (o *InvitationResponse) GetRevokedAt() time.Time`

GetRevokedAt returns the RevokedAt field if non-nil, zero value otherwise.

### GetRevokedAtOk

`func (o *InvitationResponse) GetRevokedAtOk() (*time.Time, bool)`

GetRevokedAtOk returns a tuple with the RevokedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevokedAt

`func (o *InvitationResponse) SetRevokedAt(v time.Time)`

SetRevokedAt sets RevokedAt field to given value.

### HasRevokedAt

`func (o *InvitationResponse) HasRevokedAt() bool`

HasRevokedAt returns a boolean if a field has been set.

### GetExpiredAt

`func (o *InvitationResponse) GetExpiredAt() time.Time`

GetExpiredAt returns the ExpiredAt field if non-nil, zero value otherwise.

### GetExpiredAtOk

`func (o *InvitationResponse) GetExpiredAtOk() (*time.Time, bool)`

GetExpiredAtOk returns a tuple with the ExpiredAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiredAt

`func (o *InvitationResponse) SetExpiredAt(v time.Time)`

SetExpiredAt sets ExpiredAt field to given value.

### HasExpiredAt

`func (o *InvitationResponse) HasExpiredAt() bool`

HasExpiredAt returns a boolean if a field has been set.

### GetInitialTuples

`func (o *InvitationResponse) GetInitialTuples() []InvitationInitialTuple`

GetInitialTuples returns the InitialTuples field if non-nil, zero value otherwise.

### GetInitialTuplesOk

`func (o *InvitationResponse) GetInitialTuplesOk() (*[]InvitationInitialTuple, bool)`

GetInitialTuplesOk returns a tuple with the InitialTuples field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInitialTuples

`func (o *InvitationResponse) SetInitialTuples(v []InvitationInitialTuple)`

SetInitialTuples sets InitialTuples field to given value.

### HasInitialTuples

`func (o *InvitationResponse) HasInitialTuples() bool`

HasInitialTuples returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


