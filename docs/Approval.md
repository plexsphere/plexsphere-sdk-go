# Approval

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Approval identifier (UUIDv7). | 
**DomainId** | **string** | Identifier of the owning Domain — the residency pivot the ReBAC gate authorises against.  | 
**ProposerSubject** | **string** | ReBAC subject string of the principal that raised the proposal. A caller may never approve a proposal whose &#x60;proposer_subject&#x60; is themselves.  | 
**ActionKind** | **string** | Kind of action the proposal would perform once approved. Matched against the Domain &#x60;ApprovalPolicy&#x60; rules to decide whether the proposal is gated.  | 
**TargetResource** | **string** | Resource the proposed action targets. Matched against the optional &#x60;target_resource&#x60; of a policy rule.  | 
**Payload** | Pointer to **map[string]interface{}** | Raw JSON action payload applied verbatim once the proposal is approved. Opaque to the approval workflow — it carries the parameters of the action the proposer intends to run.  | [optional] 
**State** | [**ApprovalState**](ApprovalState.md) |  | 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**DecidedAt** | Pointer to **time.Time** | Timestamp the proposal reached a terminal state (UTC). &#x60;null&#x60; or omitted while the proposal is still &#x60;proposed&#x60; or &#x60;pending-approval&#x60;.  | [optional] 
**DecidedBySubject** | Pointer to **string** | ReBAC subject string of the principal that decided the proposal. &#x60;null&#x60; or omitted while undecided and for the unattended &#x60;expired&#x60; path.  | [optional] 
**DecisionReason** | Pointer to **string** | Free-text rationale recorded with the decision. &#x60;null&#x60; or omitted while undecided and for the unattended &#x60;expired&#x60; path. For a break-glass override the rationale value is PII and is NOT surfaced here verbatim — only its field name is projected onto &#x60;caveat_context&#x60;.  | [optional] 
**ExpiresAt** | **time.Time** | Deadline past which the background sweeper expires an un-decided proposal (UTC).  | 
**CaveatContext** | Pointer to **map[string][]string** | Names-only projection of the caveat field NAMES referenced on the decision&#39;s audit row — for a break-glass override this carries the &#x60;reason&#x60; field name. Values never cross this boundary: the map keys are caveat NAMES and the arrays are caveat-parameter NAMES, mirroring the Platform Audit Log invariant. &#x60;null&#x60; or omitted while the proposal carries no decision audit row.  | [optional] 

## Methods

### NewApproval

`func NewApproval(id string, domainId string, proposerSubject string, actionKind string, targetResource string, state ApprovalState, createdAt time.Time, expiresAt time.Time, ) *Approval`

NewApproval instantiates a new Approval object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewApprovalWithDefaults

`func NewApprovalWithDefaults() *Approval`

NewApprovalWithDefaults instantiates a new Approval object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *Approval) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *Approval) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *Approval) SetId(v string)`

SetId sets Id field to given value.


### GetDomainId

`func (o *Approval) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *Approval) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *Approval) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetProposerSubject

`func (o *Approval) GetProposerSubject() string`

GetProposerSubject returns the ProposerSubject field if non-nil, zero value otherwise.

### GetProposerSubjectOk

`func (o *Approval) GetProposerSubjectOk() (*string, bool)`

GetProposerSubjectOk returns a tuple with the ProposerSubject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProposerSubject

`func (o *Approval) SetProposerSubject(v string)`

SetProposerSubject sets ProposerSubject field to given value.


### GetActionKind

`func (o *Approval) GetActionKind() string`

GetActionKind returns the ActionKind field if non-nil, zero value otherwise.

### GetActionKindOk

`func (o *Approval) GetActionKindOk() (*string, bool)`

GetActionKindOk returns a tuple with the ActionKind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetActionKind

`func (o *Approval) SetActionKind(v string)`

SetActionKind sets ActionKind field to given value.


### GetTargetResource

`func (o *Approval) GetTargetResource() string`

GetTargetResource returns the TargetResource field if non-nil, zero value otherwise.

### GetTargetResourceOk

`func (o *Approval) GetTargetResourceOk() (*string, bool)`

GetTargetResourceOk returns a tuple with the TargetResource field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetResource

`func (o *Approval) SetTargetResource(v string)`

SetTargetResource sets TargetResource field to given value.


### GetPayload

`func (o *Approval) GetPayload() map[string]interface{}`

GetPayload returns the Payload field if non-nil, zero value otherwise.

### GetPayloadOk

`func (o *Approval) GetPayloadOk() (*map[string]interface{}, bool)`

GetPayloadOk returns a tuple with the Payload field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPayload

`func (o *Approval) SetPayload(v map[string]interface{})`

SetPayload sets Payload field to given value.

### HasPayload

`func (o *Approval) HasPayload() bool`

HasPayload returns a boolean if a field has been set.

### GetState

`func (o *Approval) GetState() ApprovalState`

GetState returns the State field if non-nil, zero value otherwise.

### GetStateOk

`func (o *Approval) GetStateOk() (*ApprovalState, bool)`

GetStateOk returns a tuple with the State field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetState

`func (o *Approval) SetState(v ApprovalState)`

SetState sets State field to given value.


### GetCreatedAt

`func (o *Approval) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *Approval) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *Approval) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetDecidedAt

`func (o *Approval) GetDecidedAt() time.Time`

GetDecidedAt returns the DecidedAt field if non-nil, zero value otherwise.

### GetDecidedAtOk

`func (o *Approval) GetDecidedAtOk() (*time.Time, bool)`

GetDecidedAtOk returns a tuple with the DecidedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDecidedAt

`func (o *Approval) SetDecidedAt(v time.Time)`

SetDecidedAt sets DecidedAt field to given value.

### HasDecidedAt

`func (o *Approval) HasDecidedAt() bool`

HasDecidedAt returns a boolean if a field has been set.

### GetDecidedBySubject

`func (o *Approval) GetDecidedBySubject() string`

GetDecidedBySubject returns the DecidedBySubject field if non-nil, zero value otherwise.

### GetDecidedBySubjectOk

`func (o *Approval) GetDecidedBySubjectOk() (*string, bool)`

GetDecidedBySubjectOk returns a tuple with the DecidedBySubject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDecidedBySubject

`func (o *Approval) SetDecidedBySubject(v string)`

SetDecidedBySubject sets DecidedBySubject field to given value.

### HasDecidedBySubject

`func (o *Approval) HasDecidedBySubject() bool`

HasDecidedBySubject returns a boolean if a field has been set.

### GetDecisionReason

`func (o *Approval) GetDecisionReason() string`

GetDecisionReason returns the DecisionReason field if non-nil, zero value otherwise.

### GetDecisionReasonOk

`func (o *Approval) GetDecisionReasonOk() (*string, bool)`

GetDecisionReasonOk returns a tuple with the DecisionReason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDecisionReason

`func (o *Approval) SetDecisionReason(v string)`

SetDecisionReason sets DecisionReason field to given value.

### HasDecisionReason

`func (o *Approval) HasDecisionReason() bool`

HasDecisionReason returns a boolean if a field has been set.

### GetExpiresAt

`func (o *Approval) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *Approval) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *Approval) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.


### GetCaveatContext

`func (o *Approval) GetCaveatContext() map[string][]string`

GetCaveatContext returns the CaveatContext field if non-nil, zero value otherwise.

### GetCaveatContextOk

`func (o *Approval) GetCaveatContextOk() (*map[string][]string, bool)`

GetCaveatContextOk returns a tuple with the CaveatContext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaveatContext

`func (o *Approval) SetCaveatContext(v map[string][]string)`

SetCaveatContext sets CaveatContext field to given value.

### HasCaveatContext

`func (o *Approval) HasCaveatContext() bool`

HasCaveatContext returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


