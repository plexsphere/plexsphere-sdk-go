# NodeStateExecution

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ExecutionId** | **string** | Identifier of the Execution the dispatch belongs to (UUIDv7). | 
**Action** | **string** | Name of the dispatched action. | 
**Type** | [**ActionKind**](ActionKind.md) |  | 
**Parameters** | Pointer to **map[string]interface{}** | Opaque JSON parameter document passed verbatim to the action. &#x60;null&#x60; when the dispatch carries no parameters.  | [optional] 
**Status** | [**NodeStateExecutionStatus**](NodeStateExecutionStatus.md) |  | 
**RequestedAt** | **time.Time** | Timestamp the dispatch was requested (UTC). | 
**ExpiresAt** | **time.Time** | Absolute deadline (UTC) the Node must report a terminal result within. The pull carries the absolute expiry rather than the event payload&#39;s relative &#x60;timeout_seconds&#x60; because pull delivery is delayed by the reconcile cadence.  | 

## Methods

### NewNodeStateExecution

`func NewNodeStateExecution(executionId string, action string, type_ ActionKind, status NodeStateExecutionStatus, requestedAt time.Time, expiresAt time.Time, ) *NodeStateExecution`

NewNodeStateExecution instantiates a new NodeStateExecution object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateExecutionWithDefaults

`func NewNodeStateExecutionWithDefaults() *NodeStateExecution`

NewNodeStateExecutionWithDefaults instantiates a new NodeStateExecution object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetExecutionId

`func (o *NodeStateExecution) GetExecutionId() string`

GetExecutionId returns the ExecutionId field if non-nil, zero value otherwise.

### GetExecutionIdOk

`func (o *NodeStateExecution) GetExecutionIdOk() (*string, bool)`

GetExecutionIdOk returns a tuple with the ExecutionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExecutionId

`func (o *NodeStateExecution) SetExecutionId(v string)`

SetExecutionId sets ExecutionId field to given value.


### GetAction

`func (o *NodeStateExecution) GetAction() string`

GetAction returns the Action field if non-nil, zero value otherwise.

### GetActionOk

`func (o *NodeStateExecution) GetActionOk() (*string, bool)`

GetActionOk returns a tuple with the Action field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAction

`func (o *NodeStateExecution) SetAction(v string)`

SetAction sets Action field to given value.


### GetType

`func (o *NodeStateExecution) GetType() ActionKind`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *NodeStateExecution) GetTypeOk() (*ActionKind, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *NodeStateExecution) SetType(v ActionKind)`

SetType sets Type field to given value.


### GetParameters

`func (o *NodeStateExecution) GetParameters() map[string]interface{}`

GetParameters returns the Parameters field if non-nil, zero value otherwise.

### GetParametersOk

`func (o *NodeStateExecution) GetParametersOk() (*map[string]interface{}, bool)`

GetParametersOk returns a tuple with the Parameters field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParameters

`func (o *NodeStateExecution) SetParameters(v map[string]interface{})`

SetParameters sets Parameters field to given value.

### HasParameters

`func (o *NodeStateExecution) HasParameters() bool`

HasParameters returns a boolean if a field has been set.

### GetStatus

`func (o *NodeStateExecution) GetStatus() NodeStateExecutionStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *NodeStateExecution) GetStatusOk() (*NodeStateExecutionStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *NodeStateExecution) SetStatus(v NodeStateExecutionStatus)`

SetStatus sets Status field to given value.


### GetRequestedAt

`func (o *NodeStateExecution) GetRequestedAt() time.Time`

GetRequestedAt returns the RequestedAt field if non-nil, zero value otherwise.

### GetRequestedAtOk

`func (o *NodeStateExecution) GetRequestedAtOk() (*time.Time, bool)`

GetRequestedAtOk returns a tuple with the RequestedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequestedAt

`func (o *NodeStateExecution) SetRequestedAt(v time.Time)`

SetRequestedAt sets RequestedAt field to given value.


### GetExpiresAt

`func (o *NodeStateExecution) GetExpiresAt() time.Time`

GetExpiresAt returns the ExpiresAt field if non-nil, zero value otherwise.

### GetExpiresAtOk

`func (o *NodeStateExecution) GetExpiresAtOk() (*time.Time, bool)`

GetExpiresAtOk returns a tuple with the ExpiresAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresAt

`func (o *NodeStateExecution) SetExpiresAt(v time.Time)`

SetExpiresAt sets ExpiresAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


