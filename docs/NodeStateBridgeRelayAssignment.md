# NodeStateBridgeRelayAssignment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PeerNodeId** | **string** | Peer Node the relay fallback applies to. | 
**FallbackEndpoint** | **string** | Host the peer dials when direct connectivity is unavailable. | 
**FallbackEndpointPort** | **int32** | Port on the fallback endpoint the peer dials. | 

## Methods

### NewNodeStateBridgeRelayAssignment

`func NewNodeStateBridgeRelayAssignment(peerNodeId string, fallbackEndpoint string, fallbackEndpointPort int32, ) *NodeStateBridgeRelayAssignment`

NewNodeStateBridgeRelayAssignment instantiates a new NodeStateBridgeRelayAssignment object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateBridgeRelayAssignmentWithDefaults

`func NewNodeStateBridgeRelayAssignmentWithDefaults() *NodeStateBridgeRelayAssignment`

NewNodeStateBridgeRelayAssignmentWithDefaults instantiates a new NodeStateBridgeRelayAssignment object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPeerNodeId

`func (o *NodeStateBridgeRelayAssignment) GetPeerNodeId() string`

GetPeerNodeId returns the PeerNodeId field if non-nil, zero value otherwise.

### GetPeerNodeIdOk

`func (o *NodeStateBridgeRelayAssignment) GetPeerNodeIdOk() (*string, bool)`

GetPeerNodeIdOk returns a tuple with the PeerNodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPeerNodeId

`func (o *NodeStateBridgeRelayAssignment) SetPeerNodeId(v string)`

SetPeerNodeId sets PeerNodeId field to given value.


### GetFallbackEndpoint

`func (o *NodeStateBridgeRelayAssignment) GetFallbackEndpoint() string`

GetFallbackEndpoint returns the FallbackEndpoint field if non-nil, zero value otherwise.

### GetFallbackEndpointOk

`func (o *NodeStateBridgeRelayAssignment) GetFallbackEndpointOk() (*string, bool)`

GetFallbackEndpointOk returns a tuple with the FallbackEndpoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFallbackEndpoint

`func (o *NodeStateBridgeRelayAssignment) SetFallbackEndpoint(v string)`

SetFallbackEndpoint sets FallbackEndpoint field to given value.


### GetFallbackEndpointPort

`func (o *NodeStateBridgeRelayAssignment) GetFallbackEndpointPort() int32`

GetFallbackEndpointPort returns the FallbackEndpointPort field if non-nil, zero value otherwise.

### GetFallbackEndpointPortOk

`func (o *NodeStateBridgeRelayAssignment) GetFallbackEndpointPortOk() (*int32, bool)`

GetFallbackEndpointPortOk returns a tuple with the FallbackEndpointPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFallbackEndpointPort

`func (o *NodeStateBridgeRelayAssignment) SetFallbackEndpointPort(v int32)`

SetFallbackEndpointPort sets FallbackEndpointPort field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


