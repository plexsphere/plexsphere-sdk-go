# SinkEnablement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable identifier of the enablement (UUIDv7). | 
**ProjectId** | **string** | Project the grant is filed for. | 
**SinkId** | **string** | Sink the grant addresses. | 
**State** | [**SinkEnablementState**](SinkEnablementState.md) |  | 
**RequestedBy** | **string** | Principal that asked for the grant. | 
**DecidedBySubject** | Pointer to **string** | ReBAC subject of the principal that moved the enablement out of &#x60;requested&#x60;. Absent while the enablement is undecided.  | [optional] 
**DecidedAt** | Pointer to **time.Time** | RFC 3339 timestamp the decision was recorded. Absent while the enablement is undecided.  | [optional] 
**DecisionReason** | Pointer to **string** | Rationale recorded with the decision. A rejection and a revocation both carry one; an approval records none, so the field is absent on an approved enablement.  | [optional] 
**CreatedAt** | **time.Time** | RFC 3339 timestamp the enablement was filed. | 
**SyncPending** | Pointer to **bool** | Set on a grant response only. &#x60;true&#x60; means the grant COMMITTED — the row moved and its event is durable — but the arm that mirrors it into the authorization graph has not completed, so the grant is not yet effective. The caller must NOT retry: the retry is refused by the live-unique index and reports a conflict for work that already happened. The committed event drives the same mutation through the authz-sync arm.  | [optional] 

## Methods

### NewSinkEnablement

`func NewSinkEnablement(id string, projectId string, sinkId string, state SinkEnablementState, requestedBy string, createdAt time.Time, ) *SinkEnablement`

NewSinkEnablement instantiates a new SinkEnablement object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkEnablementWithDefaults

`func NewSinkEnablementWithDefaults() *SinkEnablement`

NewSinkEnablementWithDefaults instantiates a new SinkEnablement object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *SinkEnablement) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *SinkEnablement) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *SinkEnablement) SetId(v string)`

SetId sets Id field to given value.


### GetProjectId

`func (o *SinkEnablement) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *SinkEnablement) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *SinkEnablement) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetSinkId

`func (o *SinkEnablement) GetSinkId() string`

GetSinkId returns the SinkId field if non-nil, zero value otherwise.

### GetSinkIdOk

`func (o *SinkEnablement) GetSinkIdOk() (*string, bool)`

GetSinkIdOk returns a tuple with the SinkId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSinkId

`func (o *SinkEnablement) SetSinkId(v string)`

SetSinkId sets SinkId field to given value.


### GetState

`func (o *SinkEnablement) GetState() SinkEnablementState`

GetState returns the State field if non-nil, zero value otherwise.

### GetStateOk

`func (o *SinkEnablement) GetStateOk() (*SinkEnablementState, bool)`

GetStateOk returns a tuple with the State field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetState

`func (o *SinkEnablement) SetState(v SinkEnablementState)`

SetState sets State field to given value.


### GetRequestedBy

`func (o *SinkEnablement) GetRequestedBy() string`

GetRequestedBy returns the RequestedBy field if non-nil, zero value otherwise.

### GetRequestedByOk

`func (o *SinkEnablement) GetRequestedByOk() (*string, bool)`

GetRequestedByOk returns a tuple with the RequestedBy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequestedBy

`func (o *SinkEnablement) SetRequestedBy(v string)`

SetRequestedBy sets RequestedBy field to given value.


### GetDecidedBySubject

`func (o *SinkEnablement) GetDecidedBySubject() string`

GetDecidedBySubject returns the DecidedBySubject field if non-nil, zero value otherwise.

### GetDecidedBySubjectOk

`func (o *SinkEnablement) GetDecidedBySubjectOk() (*string, bool)`

GetDecidedBySubjectOk returns a tuple with the DecidedBySubject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDecidedBySubject

`func (o *SinkEnablement) SetDecidedBySubject(v string)`

SetDecidedBySubject sets DecidedBySubject field to given value.

### HasDecidedBySubject

`func (o *SinkEnablement) HasDecidedBySubject() bool`

HasDecidedBySubject returns a boolean if a field has been set.

### GetDecidedAt

`func (o *SinkEnablement) GetDecidedAt() time.Time`

GetDecidedAt returns the DecidedAt field if non-nil, zero value otherwise.

### GetDecidedAtOk

`func (o *SinkEnablement) GetDecidedAtOk() (*time.Time, bool)`

GetDecidedAtOk returns a tuple with the DecidedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDecidedAt

`func (o *SinkEnablement) SetDecidedAt(v time.Time)`

SetDecidedAt sets DecidedAt field to given value.

### HasDecidedAt

`func (o *SinkEnablement) HasDecidedAt() bool`

HasDecidedAt returns a boolean if a field has been set.

### GetDecisionReason

`func (o *SinkEnablement) GetDecisionReason() string`

GetDecisionReason returns the DecisionReason field if non-nil, zero value otherwise.

### GetDecisionReasonOk

`func (o *SinkEnablement) GetDecisionReasonOk() (*string, bool)`

GetDecisionReasonOk returns a tuple with the DecisionReason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDecisionReason

`func (o *SinkEnablement) SetDecisionReason(v string)`

SetDecisionReason sets DecisionReason field to given value.

### HasDecisionReason

`func (o *SinkEnablement) HasDecisionReason() bool`

HasDecisionReason returns a boolean if a field has been set.

### GetCreatedAt

`func (o *SinkEnablement) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *SinkEnablement) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *SinkEnablement) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetSyncPending

`func (o *SinkEnablement) GetSyncPending() bool`

GetSyncPending returns the SyncPending field if non-nil, zero value otherwise.

### GetSyncPendingOk

`func (o *SinkEnablement) GetSyncPendingOk() (*bool, bool)`

GetSyncPendingOk returns a tuple with the SyncPending field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSyncPending

`func (o *SinkEnablement) SetSyncPending(v bool)`

SetSyncPending sets SyncPending field to given value.

### HasSyncPending

`func (o *SinkEnablement) HasSyncPending() bool`

HasSyncPending returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


