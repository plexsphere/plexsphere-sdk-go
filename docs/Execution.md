# Execution

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Execution identifier (UUIDv7). | 
**ProjectId** | **string** | Identifier of the owning Project (UUIDv7). | 
**DomainId** | **string** | Identifier of the owning Domain (UUIDv7) — the residency pivot the per-Domain concurrent-execution budget is counted against.  | 
**Action** | **string** | Name of the dispatched action. | 
**Type** | [**ActionKind**](ActionKind.md) |  | 
**Status** | [**ExecutionStatus**](ExecutionStatus.md) | Aggregate status of the Execution, derived from its per-Node targets.  | 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Timestamp of the Execution&#39;s most recent advance (UTC). | 
**Targets** | [**[]ExecutionTarget**](ExecutionTarget.md) | Per-Node invocations the Execution fanned out to. | 

## Methods

### NewExecution

`func NewExecution(id string, projectId string, domainId string, action string, type_ ActionKind, status ExecutionStatus, createdAt time.Time, updatedAt time.Time, targets []ExecutionTarget, ) *Execution`

NewExecution instantiates a new Execution object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewExecutionWithDefaults

`func NewExecutionWithDefaults() *Execution`

NewExecutionWithDefaults instantiates a new Execution object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *Execution) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *Execution) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *Execution) SetId(v string)`

SetId sets Id field to given value.


### GetProjectId

`func (o *Execution) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *Execution) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *Execution) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetDomainId

`func (o *Execution) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *Execution) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *Execution) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetAction

`func (o *Execution) GetAction() string`

GetAction returns the Action field if non-nil, zero value otherwise.

### GetActionOk

`func (o *Execution) GetActionOk() (*string, bool)`

GetActionOk returns a tuple with the Action field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAction

`func (o *Execution) SetAction(v string)`

SetAction sets Action field to given value.


### GetType

`func (o *Execution) GetType() ActionKind`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *Execution) GetTypeOk() (*ActionKind, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *Execution) SetType(v ActionKind)`

SetType sets Type field to given value.


### GetStatus

`func (o *Execution) GetStatus() ExecutionStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *Execution) GetStatusOk() (*ExecutionStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *Execution) SetStatus(v ExecutionStatus)`

SetStatus sets Status field to given value.


### GetCreatedAt

`func (o *Execution) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *Execution) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *Execution) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *Execution) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *Execution) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *Execution) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.


### GetTargets

`func (o *Execution) GetTargets() []ExecutionTarget`

GetTargets returns the Targets field if non-nil, zero value otherwise.

### GetTargetsOk

`func (o *Execution) GetTargetsOk() (*[]ExecutionTarget, bool)`

GetTargetsOk returns a tuple with the Targets field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargets

`func (o *Execution) SetTargets(v []ExecutionTarget)`

SetTargets sets Targets field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


