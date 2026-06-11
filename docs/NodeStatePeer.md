# NodeStatePeer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NodeId** | **string** | Peer&#39;s Node identifier. Plexd&#39;s reconcile loop keys peers by id.  | 
**MeshIp** | **string** | Peer&#39;s allocator-assigned mesh address. Plexd programs the WireGuard endpoint from this field.  | 
**PublicKey** | **string** | Peer&#39;s WireGuard public key, base64-encoded with standard padding.  | 
**FallbackEndpoint** | Pointer to **string** | Canonical bridge &#x60;host:port&#x60; that plexd programs as a NAT-traversal relay when direct peer-to-peer connectivity is unavailable. Empty or absent means no bridge is currently assigned for this peer. Format: &#x60;&lt;inet-or-hostname&gt;:&lt;port&gt;&#x60;.  | [optional] 

## Methods

### NewNodeStatePeer

`func NewNodeStatePeer(nodeId string, meshIp string, publicKey string, ) *NodeStatePeer`

NewNodeStatePeer instantiates a new NodeStatePeer object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStatePeerWithDefaults

`func NewNodeStatePeerWithDefaults() *NodeStatePeer`

NewNodeStatePeerWithDefaults instantiates a new NodeStatePeer object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNodeId

`func (o *NodeStatePeer) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *NodeStatePeer) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *NodeStatePeer) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetMeshIp

`func (o *NodeStatePeer) GetMeshIp() string`

GetMeshIp returns the MeshIp field if non-nil, zero value otherwise.

### GetMeshIpOk

`func (o *NodeStatePeer) GetMeshIpOk() (*string, bool)`

GetMeshIpOk returns a tuple with the MeshIp field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMeshIp

`func (o *NodeStatePeer) SetMeshIp(v string)`

SetMeshIp sets MeshIp field to given value.


### GetPublicKey

`func (o *NodeStatePeer) GetPublicKey() string`

GetPublicKey returns the PublicKey field if non-nil, zero value otherwise.

### GetPublicKeyOk

`func (o *NodeStatePeer) GetPublicKeyOk() (*string, bool)`

GetPublicKeyOk returns a tuple with the PublicKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPublicKey

`func (o *NodeStatePeer) SetPublicKey(v string)`

SetPublicKey sets PublicKey field to given value.


### GetFallbackEndpoint

`func (o *NodeStatePeer) GetFallbackEndpoint() string`

GetFallbackEndpoint returns the FallbackEndpoint field if non-nil, zero value otherwise.

### GetFallbackEndpointOk

`func (o *NodeStatePeer) GetFallbackEndpointOk() (*string, bool)`

GetFallbackEndpointOk returns a tuple with the FallbackEndpoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFallbackEndpoint

`func (o *NodeStatePeer) SetFallbackEndpoint(v string)`

SetFallbackEndpoint sets FallbackEndpoint field to given value.

### HasFallbackEndpoint

`func (o *NodeStatePeer) HasFallbackEndpoint() bool`

HasFallbackEndpoint returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


