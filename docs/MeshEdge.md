# MeshEdge

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SourceNodeId** | **string** | Node from which the WireGuard handshake originates. Pinned against the live Peer aggregate so a stale read never returns an edge for a retired Node.  | 
**TargetNodeId** | **string** | Peer Node the handshake terminates against. Same liveness guarantee as &#x60;source_node_id&#x60;.  | 
**Mode** | [**MeshEdgeMode**](MeshEdgeMode.md) |  | 
**RelayNodeId** | **string** | Bridge Node currently serving as the relay fallback for this edge. Always populated when &#x60;mode&#x60; is &#x60;relayed&#x60;; always &#x60;null&#x60; when &#x60;mode&#x60; is &#x60;direct&#x60;.  | 
**Status** | [**MeshEdgeStatus**](MeshEdgeStatus.md) |  | 

## Methods

### NewMeshEdge

`func NewMeshEdge(sourceNodeId string, targetNodeId string, mode MeshEdgeMode, relayNodeId string, status MeshEdgeStatus, ) *MeshEdge`

NewMeshEdge instantiates a new MeshEdge object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewMeshEdgeWithDefaults

`func NewMeshEdgeWithDefaults() *MeshEdge`

NewMeshEdgeWithDefaults instantiates a new MeshEdge object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSourceNodeId

`func (o *MeshEdge) GetSourceNodeId() string`

GetSourceNodeId returns the SourceNodeId field if non-nil, zero value otherwise.

### GetSourceNodeIdOk

`func (o *MeshEdge) GetSourceNodeIdOk() (*string, bool)`

GetSourceNodeIdOk returns a tuple with the SourceNodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSourceNodeId

`func (o *MeshEdge) SetSourceNodeId(v string)`

SetSourceNodeId sets SourceNodeId field to given value.


### GetTargetNodeId

`func (o *MeshEdge) GetTargetNodeId() string`

GetTargetNodeId returns the TargetNodeId field if non-nil, zero value otherwise.

### GetTargetNodeIdOk

`func (o *MeshEdge) GetTargetNodeIdOk() (*string, bool)`

GetTargetNodeIdOk returns a tuple with the TargetNodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetNodeId

`func (o *MeshEdge) SetTargetNodeId(v string)`

SetTargetNodeId sets TargetNodeId field to given value.


### GetMode

`func (o *MeshEdge) GetMode() MeshEdgeMode`

GetMode returns the Mode field if non-nil, zero value otherwise.

### GetModeOk

`func (o *MeshEdge) GetModeOk() (*MeshEdgeMode, bool)`

GetModeOk returns a tuple with the Mode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMode

`func (o *MeshEdge) SetMode(v MeshEdgeMode)`

SetMode sets Mode field to given value.


### GetRelayNodeId

`func (o *MeshEdge) GetRelayNodeId() string`

GetRelayNodeId returns the RelayNodeId field if non-nil, zero value otherwise.

### GetRelayNodeIdOk

`func (o *MeshEdge) GetRelayNodeIdOk() (*string, bool)`

GetRelayNodeIdOk returns a tuple with the RelayNodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelayNodeId

`func (o *MeshEdge) SetRelayNodeId(v string)`

SetRelayNodeId sets RelayNodeId field to given value.


### GetStatus

`func (o *MeshEdge) GetStatus() MeshEdgeStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *MeshEdge) GetStatusOk() (*MeshEdgeStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *MeshEdge) SetStatus(v MeshEdgeStatus)`

SetStatus sets Status field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


