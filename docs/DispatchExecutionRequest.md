# DispatchExecutionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Action** | **string** | Name of the action to dispatch. | 
**Type** | Pointer to [**ActionKind**](ActionKind.md) | Kind of action to dispatch (&#x60;builtin&#x60; or &#x60;hook&#x60;). Defaults to &#x60;builtin&#x60; when omitted.  | [optional] 
**Parameters** | Pointer to **map[string]interface{}** | Opaque JSON parameter document passed verbatim to the action.  | [optional] 
**TimeoutSeconds** | Pointer to **int32** | Per-dispatch execution timeout in whole seconds. A background reconciler times out an invocation whose Node never reports a terminal result within this window.  | [optional] 
**Selector** | Pointer to **string** | Opaque label selector resolving the target cohort. Supply EXACTLY ONE of &#x60;selector&#x60; or &#x60;node_id&#x60;; supplying both, or neither, is rejected.  | [optional] 
**NodeId** | Pointer to **string** | Identifier of a single target Node (UUIDv7). Supply EXACTLY ONE of &#x60;node_id&#x60; or &#x60;selector&#x60;; supplying both, or neither, is rejected.  | [optional] 

## Methods

### NewDispatchExecutionRequest

`func NewDispatchExecutionRequest(action string, ) *DispatchExecutionRequest`

NewDispatchExecutionRequest instantiates a new DispatchExecutionRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDispatchExecutionRequestWithDefaults

`func NewDispatchExecutionRequestWithDefaults() *DispatchExecutionRequest`

NewDispatchExecutionRequestWithDefaults instantiates a new DispatchExecutionRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAction

`func (o *DispatchExecutionRequest) GetAction() string`

GetAction returns the Action field if non-nil, zero value otherwise.

### GetActionOk

`func (o *DispatchExecutionRequest) GetActionOk() (*string, bool)`

GetActionOk returns a tuple with the Action field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAction

`func (o *DispatchExecutionRequest) SetAction(v string)`

SetAction sets Action field to given value.


### GetType

`func (o *DispatchExecutionRequest) GetType() ActionKind`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *DispatchExecutionRequest) GetTypeOk() (*ActionKind, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *DispatchExecutionRequest) SetType(v ActionKind)`

SetType sets Type field to given value.

### HasType

`func (o *DispatchExecutionRequest) HasType() bool`

HasType returns a boolean if a field has been set.

### GetParameters

`func (o *DispatchExecutionRequest) GetParameters() map[string]interface{}`

GetParameters returns the Parameters field if non-nil, zero value otherwise.

### GetParametersOk

`func (o *DispatchExecutionRequest) GetParametersOk() (*map[string]interface{}, bool)`

GetParametersOk returns a tuple with the Parameters field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParameters

`func (o *DispatchExecutionRequest) SetParameters(v map[string]interface{})`

SetParameters sets Parameters field to given value.

### HasParameters

`func (o *DispatchExecutionRequest) HasParameters() bool`

HasParameters returns a boolean if a field has been set.

### GetTimeoutSeconds

`func (o *DispatchExecutionRequest) GetTimeoutSeconds() int32`

GetTimeoutSeconds returns the TimeoutSeconds field if non-nil, zero value otherwise.

### GetTimeoutSecondsOk

`func (o *DispatchExecutionRequest) GetTimeoutSecondsOk() (*int32, bool)`

GetTimeoutSecondsOk returns a tuple with the TimeoutSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTimeoutSeconds

`func (o *DispatchExecutionRequest) SetTimeoutSeconds(v int32)`

SetTimeoutSeconds sets TimeoutSeconds field to given value.

### HasTimeoutSeconds

`func (o *DispatchExecutionRequest) HasTimeoutSeconds() bool`

HasTimeoutSeconds returns a boolean if a field has been set.

### GetSelector

`func (o *DispatchExecutionRequest) GetSelector() string`

GetSelector returns the Selector field if non-nil, zero value otherwise.

### GetSelectorOk

`func (o *DispatchExecutionRequest) GetSelectorOk() (*string, bool)`

GetSelectorOk returns a tuple with the Selector field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSelector

`func (o *DispatchExecutionRequest) SetSelector(v string)`

SetSelector sets Selector field to given value.

### HasSelector

`func (o *DispatchExecutionRequest) HasSelector() bool`

HasSelector returns a boolean if a field has been set.

### GetNodeId

`func (o *DispatchExecutionRequest) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *DispatchExecutionRequest) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *DispatchExecutionRequest) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.

### HasNodeId

`func (o *DispatchExecutionRequest) HasNodeId() bool`

HasNodeId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


