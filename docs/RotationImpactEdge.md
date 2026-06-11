# RotationImpactEdge

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PeerNodeId** | **string** | Peer at the other end of the affected edge — joins back to the per-Node read surfaces for drill-down.  | 
**CurrentKid** | **string** | Key id of the PSK currently in force on this edge. Mirrors the &#x60;kid&#x60; field on &#x60;KeysRotateResponse&#x60; so a renderer can display \&quot;before / after\&quot; the dry-run with a single mapping.  | 
**CurrentWrapKeyVersion** | **int32** | Version of the active wrap key under which the in-force PSK is wrapped. Paired with &#x60;current_kid&#x60; it pins the exact wrapping epoch the rotation would supersede.  | 

## Methods

### NewRotationImpactEdge

`func NewRotationImpactEdge(peerNodeId string, currentKid string, currentWrapKeyVersion int32, ) *RotationImpactEdge`

NewRotationImpactEdge instantiates a new RotationImpactEdge object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRotationImpactEdgeWithDefaults

`func NewRotationImpactEdgeWithDefaults() *RotationImpactEdge`

NewRotationImpactEdgeWithDefaults instantiates a new RotationImpactEdge object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPeerNodeId

`func (o *RotationImpactEdge) GetPeerNodeId() string`

GetPeerNodeId returns the PeerNodeId field if non-nil, zero value otherwise.

### GetPeerNodeIdOk

`func (o *RotationImpactEdge) GetPeerNodeIdOk() (*string, bool)`

GetPeerNodeIdOk returns a tuple with the PeerNodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPeerNodeId

`func (o *RotationImpactEdge) SetPeerNodeId(v string)`

SetPeerNodeId sets PeerNodeId field to given value.


### GetCurrentKid

`func (o *RotationImpactEdge) GetCurrentKid() string`

GetCurrentKid returns the CurrentKid field if non-nil, zero value otherwise.

### GetCurrentKidOk

`func (o *RotationImpactEdge) GetCurrentKidOk() (*string, bool)`

GetCurrentKidOk returns a tuple with the CurrentKid field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCurrentKid

`func (o *RotationImpactEdge) SetCurrentKid(v string)`

SetCurrentKid sets CurrentKid field to given value.


### GetCurrentWrapKeyVersion

`func (o *RotationImpactEdge) GetCurrentWrapKeyVersion() int32`

GetCurrentWrapKeyVersion returns the CurrentWrapKeyVersion field if non-nil, zero value otherwise.

### GetCurrentWrapKeyVersionOk

`func (o *RotationImpactEdge) GetCurrentWrapKeyVersionOk() (*int32, bool)`

GetCurrentWrapKeyVersionOk returns a tuple with the CurrentWrapKeyVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCurrentWrapKeyVersion

`func (o *RotationImpactEdge) SetCurrentWrapKeyVersion(v int32)`

SetCurrentWrapKeyVersion sets CurrentWrapKeyVersion field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


