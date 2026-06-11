# MeshTopology

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DomainId** | **string** | The Domain the topology describes. Echoes the path parameter so a renderer can sanity-check the response against the request URL.  | 
**GeneratedAt** | **time.Time** | Server-side timestamp at which the snapshot was assembled. Renderers display it alongside the topology so an operator can spot a stale view.  | 
**Nodes** | [**[]MeshTopologyNode**](MeshTopologyNode.md) | Every anchored Peer Node in the Domain at &#x60;generated_at&#x60;. Order is stable but unspecified — renderers MUST NOT rely on the listing order for layout.  | 
**Edges** | [**[]MeshEdge**](MeshEdge.md) | Every directed mesh edge between two Nodes in &#x60;nodes&#x60; at &#x60;generated_at&#x60;. Edges are directional; a fully meshed pair of Nodes produces two entries.  | 

## Methods

### NewMeshTopology

`func NewMeshTopology(domainId string, generatedAt time.Time, nodes []MeshTopologyNode, edges []MeshEdge, ) *MeshTopology`

NewMeshTopology instantiates a new MeshTopology object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewMeshTopologyWithDefaults

`func NewMeshTopologyWithDefaults() *MeshTopology`

NewMeshTopologyWithDefaults instantiates a new MeshTopology object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDomainId

`func (o *MeshTopology) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *MeshTopology) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *MeshTopology) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetGeneratedAt

`func (o *MeshTopology) GetGeneratedAt() time.Time`

GetGeneratedAt returns the GeneratedAt field if non-nil, zero value otherwise.

### GetGeneratedAtOk

`func (o *MeshTopology) GetGeneratedAtOk() (*time.Time, bool)`

GetGeneratedAtOk returns a tuple with the GeneratedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGeneratedAt

`func (o *MeshTopology) SetGeneratedAt(v time.Time)`

SetGeneratedAt sets GeneratedAt field to given value.


### GetNodes

`func (o *MeshTopology) GetNodes() []MeshTopologyNode`

GetNodes returns the Nodes field if non-nil, zero value otherwise.

### GetNodesOk

`func (o *MeshTopology) GetNodesOk() (*[]MeshTopologyNode, bool)`

GetNodesOk returns a tuple with the Nodes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodes

`func (o *MeshTopology) SetNodes(v []MeshTopologyNode)`

SetNodes sets Nodes field to given value.


### GetEdges

`func (o *MeshTopology) GetEdges() []MeshEdge`

GetEdges returns the Edges field if non-nil, zero value otherwise.

### GetEdgesOk

`func (o *MeshTopology) GetEdgesOk() (*[]MeshEdge, bool)`

GetEdgesOk returns a tuple with the Edges field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEdges

`func (o *MeshTopology) SetEdges(v []MeshEdge)`

SetEdges sets Edges field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


