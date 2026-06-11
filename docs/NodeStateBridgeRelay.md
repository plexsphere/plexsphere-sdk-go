# NodeStateBridgeRelay

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Enabled** | **bool** | Whether the relay is active. | 
**ListenPort** | **int32** | UDP port the relay listens on. | 
**Assignments** | [**[]NodeStateBridgeRelayAssignment**](NodeStateBridgeRelayAssignment.md) | Per-peer relay fallback-endpoint assignments, ordered deterministically by &#x60;peer_node_id&#x60; so two consecutive pulls against the same ledger snapshot are byte-equal. An empty array is a legitimate state.  | 

## Methods

### NewNodeStateBridgeRelay

`func NewNodeStateBridgeRelay(enabled bool, listenPort int32, assignments []NodeStateBridgeRelayAssignment, ) *NodeStateBridgeRelay`

NewNodeStateBridgeRelay instantiates a new NodeStateBridgeRelay object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateBridgeRelayWithDefaults

`func NewNodeStateBridgeRelayWithDefaults() *NodeStateBridgeRelay`

NewNodeStateBridgeRelayWithDefaults instantiates a new NodeStateBridgeRelay object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetEnabled

`func (o *NodeStateBridgeRelay) GetEnabled() bool`

GetEnabled returns the Enabled field if non-nil, zero value otherwise.

### GetEnabledOk

`func (o *NodeStateBridgeRelay) GetEnabledOk() (*bool, bool)`

GetEnabledOk returns a tuple with the Enabled field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnabled

`func (o *NodeStateBridgeRelay) SetEnabled(v bool)`

SetEnabled sets Enabled field to given value.


### GetListenPort

`func (o *NodeStateBridgeRelay) GetListenPort() int32`

GetListenPort returns the ListenPort field if non-nil, zero value otherwise.

### GetListenPortOk

`func (o *NodeStateBridgeRelay) GetListenPortOk() (*int32, bool)`

GetListenPortOk returns a tuple with the ListenPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetListenPort

`func (o *NodeStateBridgeRelay) SetListenPort(v int32)`

SetListenPort sets ListenPort field to given value.


### GetAssignments

`func (o *NodeStateBridgeRelay) GetAssignments() []NodeStateBridgeRelayAssignment`

GetAssignments returns the Assignments field if non-nil, zero value otherwise.

### GetAssignmentsOk

`func (o *NodeStateBridgeRelay) GetAssignmentsOk() (*[]NodeStateBridgeRelayAssignment, bool)`

GetAssignmentsOk returns a tuple with the Assignments field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAssignments

`func (o *NodeStateBridgeRelay) SetAssignments(v []NodeStateBridgeRelayAssignment)`

SetAssignments sets Assignments field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


