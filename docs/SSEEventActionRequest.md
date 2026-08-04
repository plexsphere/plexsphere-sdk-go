# SSEEventActionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventId** | **string** | Fresh per-dispatch-event identifier (UUIDv7), distinct from &#x60;execution_id&#x60; so the event carries its own identity.  | 
**OccurredAt** | **time.Time** | Timestamp the event was produced (UTC). | 
**ExecutionId** | **string** | Identifier of the Execution the dispatch belongs to (UUIDv7). | 
**NodeId** | **string** | The single target Node this event addresses (UUIDv7). | 
**Action** | **string** | Name of the dispatched action. | 
**Type** | [**ActionKind**](ActionKind.md) |  | 
**Parameters** | Pointer to **map[string]interface{}** | Opaque JSON parameter document passed verbatim to the action. &#x60;null&#x60; when the dispatch carries no parameters.  | [optional] 
**TimeoutSeconds** | **int32** | Per-dispatch timeout in whole seconds the Node must report a terminal result within.  | 
**CallbackUrl** | **string** | Absolute URL the Node reports its result back to, built per the template &#x60;{base}/v1/nodes/{node_id}/executions/{execution_id}&#x60;.  | 

## Methods

### NewSSEEventActionRequest

`func NewSSEEventActionRequest(eventId string, occurredAt time.Time, executionId string, nodeId string, action string, type_ ActionKind, timeoutSeconds int32, callbackUrl string, ) *SSEEventActionRequest`

NewSSEEventActionRequest instantiates a new SSEEventActionRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSSEEventActionRequestWithDefaults

`func NewSSEEventActionRequestWithDefaults() *SSEEventActionRequest`

NewSSEEventActionRequestWithDefaults instantiates a new SSEEventActionRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetEventId

`func (o *SSEEventActionRequest) GetEventId() string`

GetEventId returns the EventId field if non-nil, zero value otherwise.

### GetEventIdOk

`func (o *SSEEventActionRequest) GetEventIdOk() (*string, bool)`

GetEventIdOk returns a tuple with the EventId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEventId

`func (o *SSEEventActionRequest) SetEventId(v string)`

SetEventId sets EventId field to given value.


### GetOccurredAt

`func (o *SSEEventActionRequest) GetOccurredAt() time.Time`

GetOccurredAt returns the OccurredAt field if non-nil, zero value otherwise.

### GetOccurredAtOk

`func (o *SSEEventActionRequest) GetOccurredAtOk() (*time.Time, bool)`

GetOccurredAtOk returns a tuple with the OccurredAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOccurredAt

`func (o *SSEEventActionRequest) SetOccurredAt(v time.Time)`

SetOccurredAt sets OccurredAt field to given value.


### GetExecutionId

`func (o *SSEEventActionRequest) GetExecutionId() string`

GetExecutionId returns the ExecutionId field if non-nil, zero value otherwise.

### GetExecutionIdOk

`func (o *SSEEventActionRequest) GetExecutionIdOk() (*string, bool)`

GetExecutionIdOk returns a tuple with the ExecutionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExecutionId

`func (o *SSEEventActionRequest) SetExecutionId(v string)`

SetExecutionId sets ExecutionId field to given value.


### GetNodeId

`func (o *SSEEventActionRequest) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *SSEEventActionRequest) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *SSEEventActionRequest) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetAction

`func (o *SSEEventActionRequest) GetAction() string`

GetAction returns the Action field if non-nil, zero value otherwise.

### GetActionOk

`func (o *SSEEventActionRequest) GetActionOk() (*string, bool)`

GetActionOk returns a tuple with the Action field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAction

`func (o *SSEEventActionRequest) SetAction(v string)`

SetAction sets Action field to given value.


### GetType

`func (o *SSEEventActionRequest) GetType() ActionKind`

GetType returns the Type field if non-nil, zero value otherwise.

### GetTypeOk

`func (o *SSEEventActionRequest) GetTypeOk() (*ActionKind, bool)`

GetTypeOk returns a tuple with the Type field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetType

`func (o *SSEEventActionRequest) SetType(v ActionKind)`

SetType sets Type field to given value.


### GetParameters

`func (o *SSEEventActionRequest) GetParameters() map[string]interface{}`

GetParameters returns the Parameters field if non-nil, zero value otherwise.

### GetParametersOk

`func (o *SSEEventActionRequest) GetParametersOk() (*map[string]interface{}, bool)`

GetParametersOk returns a tuple with the Parameters field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParameters

`func (o *SSEEventActionRequest) SetParameters(v map[string]interface{})`

SetParameters sets Parameters field to given value.

### HasParameters

`func (o *SSEEventActionRequest) HasParameters() bool`

HasParameters returns a boolean if a field has been set.

### GetTimeoutSeconds

`func (o *SSEEventActionRequest) GetTimeoutSeconds() int32`

GetTimeoutSeconds returns the TimeoutSeconds field if non-nil, zero value otherwise.

### GetTimeoutSecondsOk

`func (o *SSEEventActionRequest) GetTimeoutSecondsOk() (*int32, bool)`

GetTimeoutSecondsOk returns a tuple with the TimeoutSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTimeoutSeconds

`func (o *SSEEventActionRequest) SetTimeoutSeconds(v int32)`

SetTimeoutSeconds sets TimeoutSeconds field to given value.


### GetCallbackUrl

`func (o *SSEEventActionRequest) GetCallbackUrl() string`

GetCallbackUrl returns the CallbackUrl field if non-nil, zero value otherwise.

### GetCallbackUrlOk

`func (o *SSEEventActionRequest) GetCallbackUrlOk() (*string, bool)`

GetCallbackUrlOk returns a tuple with the CallbackUrl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCallbackUrl

`func (o *SSEEventActionRequest) SetCallbackUrl(v string)`

SetCallbackUrl sets CallbackUrl field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


