# ExecutionTarget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NodeId** | **string** | Identifier of the target Node (UUIDv7). | 
**Status** | [**ExecutionStatus**](ExecutionStatus.md) |  | 
**CreatedAt** | **time.Time** | Target creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Timestamp of the target&#39;s most recent status advance (UTC). | 
**OutputRef** | Pointer to [**OutputRef**](OutputRef.md) | Pointer to the output the invocation produced. Present only once the target reaches a terminal status that collected output; omitted otherwise.  | [optional] 

## Methods

### NewExecutionTarget

`func NewExecutionTarget(nodeId string, status ExecutionStatus, createdAt time.Time, updatedAt time.Time, ) *ExecutionTarget`

NewExecutionTarget instantiates a new ExecutionTarget object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewExecutionTargetWithDefaults

`func NewExecutionTargetWithDefaults() *ExecutionTarget`

NewExecutionTargetWithDefaults instantiates a new ExecutionTarget object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNodeId

`func (o *ExecutionTarget) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *ExecutionTarget) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *ExecutionTarget) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetStatus

`func (o *ExecutionTarget) GetStatus() ExecutionStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *ExecutionTarget) GetStatusOk() (*ExecutionStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *ExecutionTarget) SetStatus(v ExecutionStatus)`

SetStatus sets Status field to given value.


### GetCreatedAt

`func (o *ExecutionTarget) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *ExecutionTarget) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *ExecutionTarget) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *ExecutionTarget) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *ExecutionTarget) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *ExecutionTarget) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.


### GetOutputRef

`func (o *ExecutionTarget) GetOutputRef() OutputRef`

GetOutputRef returns the OutputRef field if non-nil, zero value otherwise.

### GetOutputRefOk

`func (o *ExecutionTarget) GetOutputRefOk() (*OutputRef, bool)`

GetOutputRefOk returns a tuple with the OutputRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOutputRef

`func (o *ExecutionTarget) SetOutputRef(v OutputRef)`

SetOutputRef sets OutputRef field to given value.

### HasOutputRef

`func (o *ExecutionTarget) HasOutputRef() bool`

HasOutputRef returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


