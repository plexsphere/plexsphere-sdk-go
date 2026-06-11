# MeshTopologyNode

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NodeId** | **string** | Node identifier (UUIDv7). Joins back to the per-Node read surfaces for drill-down.  | 
**MeshIp** | **string** | The Node&#39;s allocator-assigned mesh address — IPv4 or IPv6 depending on the Domain&#39;s mesh CIDR family.  | 
**Reachability** | [**MeshTopologyNodeReachability**](MeshTopologyNodeReachability.md) |  | 

## Methods

### NewMeshTopologyNode

`func NewMeshTopologyNode(nodeId string, meshIp string, reachability MeshTopologyNodeReachability, ) *MeshTopologyNode`

NewMeshTopologyNode instantiates a new MeshTopologyNode object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewMeshTopologyNodeWithDefaults

`func NewMeshTopologyNodeWithDefaults() *MeshTopologyNode`

NewMeshTopologyNodeWithDefaults instantiates a new MeshTopologyNode object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNodeId

`func (o *MeshTopologyNode) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *MeshTopologyNode) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *MeshTopologyNode) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetMeshIp

`func (o *MeshTopologyNode) GetMeshIp() string`

GetMeshIp returns the MeshIp field if non-nil, zero value otherwise.

### GetMeshIpOk

`func (o *MeshTopologyNode) GetMeshIpOk() (*string, bool)`

GetMeshIpOk returns a tuple with the MeshIp field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMeshIp

`func (o *MeshTopologyNode) SetMeshIp(v string)`

SetMeshIp sets MeshIp field to given value.


### GetReachability

`func (o *MeshTopologyNode) GetReachability() MeshTopologyNodeReachability`

GetReachability returns the Reachability field if non-nil, zero value otherwise.

### GetReachabilityOk

`func (o *MeshTopologyNode) GetReachabilityOk() (*MeshTopologyNodeReachability, bool)`

GetReachabilityOk returns a tuple with the Reachability field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReachability

`func (o *MeshTopologyNode) SetReachability(v MeshTopologyNodeReachability)`

SetReachability sets Reachability field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


