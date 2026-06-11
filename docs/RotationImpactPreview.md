# RotationImpactPreview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NodeId** | **string** | The Node whose rotation is being previewed. Echoes the path parameter so a renderer can sanity-check the response against the request URL.  | 
**PeerId** | **string** | Identifier of the live Peer the rotation would target. Mirrors &#x60;RotationTriggerResponse.peer_id&#x60; so the preview and the mutating trigger share a single mapping.  | 
**AffectedPeerCount** | **int32** | Number of peers whose pairwise PSK would be re-issued by the rotation. Equal to the length of &#x60;affected_edges&#x60;; duplicated as a top-level scalar so a renderer can show the count without expanding the edge listing.  | 
**AffectedEdges** | [**[]RotationImpactEdge**](RotationImpactEdge.md) | Explicit listing of peer edges that would receive a fresh pairwise PSK. Order is stable but unspecified — renderers MUST NOT rely on the listing order for layout.  | 
**AlreadyPending** | **bool** | True when a &#x60;peer_key_rotation&#x60; row is already pending for the addressed Node — i.e. a live &#x60;POST /v1/nodes/{id}/keys/rotate&#x60; would surface the same flag and append no second event. Operators switch on this flag to distinguish a fresh trigger from an idempotent no-op before confirming the rotation.  | 
**EstimatedDurationSeconds** | **int32** | Estimated wall-clock seconds the rotation will take, based on the current SSE fan-out and the affected peer count. Capacity planning hint — not a guarantee.  | 

## Methods

### NewRotationImpactPreview

`func NewRotationImpactPreview(nodeId string, peerId string, affectedPeerCount int32, affectedEdges []RotationImpactEdge, alreadyPending bool, estimatedDurationSeconds int32, ) *RotationImpactPreview`

NewRotationImpactPreview instantiates a new RotationImpactPreview object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRotationImpactPreviewWithDefaults

`func NewRotationImpactPreviewWithDefaults() *RotationImpactPreview`

NewRotationImpactPreviewWithDefaults instantiates a new RotationImpactPreview object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNodeId

`func (o *RotationImpactPreview) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *RotationImpactPreview) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *RotationImpactPreview) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetPeerId

`func (o *RotationImpactPreview) GetPeerId() string`

GetPeerId returns the PeerId field if non-nil, zero value otherwise.

### GetPeerIdOk

`func (o *RotationImpactPreview) GetPeerIdOk() (*string, bool)`

GetPeerIdOk returns a tuple with the PeerId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPeerId

`func (o *RotationImpactPreview) SetPeerId(v string)`

SetPeerId sets PeerId field to given value.


### GetAffectedPeerCount

`func (o *RotationImpactPreview) GetAffectedPeerCount() int32`

GetAffectedPeerCount returns the AffectedPeerCount field if non-nil, zero value otherwise.

### GetAffectedPeerCountOk

`func (o *RotationImpactPreview) GetAffectedPeerCountOk() (*int32, bool)`

GetAffectedPeerCountOk returns a tuple with the AffectedPeerCount field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAffectedPeerCount

`func (o *RotationImpactPreview) SetAffectedPeerCount(v int32)`

SetAffectedPeerCount sets AffectedPeerCount field to given value.


### GetAffectedEdges

`func (o *RotationImpactPreview) GetAffectedEdges() []RotationImpactEdge`

GetAffectedEdges returns the AffectedEdges field if non-nil, zero value otherwise.

### GetAffectedEdgesOk

`func (o *RotationImpactPreview) GetAffectedEdgesOk() (*[]RotationImpactEdge, bool)`

GetAffectedEdgesOk returns a tuple with the AffectedEdges field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAffectedEdges

`func (o *RotationImpactPreview) SetAffectedEdges(v []RotationImpactEdge)`

SetAffectedEdges sets AffectedEdges field to given value.


### GetAlreadyPending

`func (o *RotationImpactPreview) GetAlreadyPending() bool`

GetAlreadyPending returns the AlreadyPending field if non-nil, zero value otherwise.

### GetAlreadyPendingOk

`func (o *RotationImpactPreview) GetAlreadyPendingOk() (*bool, bool)`

GetAlreadyPendingOk returns a tuple with the AlreadyPending field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAlreadyPending

`func (o *RotationImpactPreview) SetAlreadyPending(v bool)`

SetAlreadyPending sets AlreadyPending field to given value.


### GetEstimatedDurationSeconds

`func (o *RotationImpactPreview) GetEstimatedDurationSeconds() int32`

GetEstimatedDurationSeconds returns the EstimatedDurationSeconds field if non-nil, zero value otherwise.

### GetEstimatedDurationSecondsOk

`func (o *RotationImpactPreview) GetEstimatedDurationSecondsOk() (*int32, bool)`

GetEstimatedDurationSecondsOk returns a tuple with the EstimatedDurationSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEstimatedDurationSeconds

`func (o *RotationImpactPreview) SetEstimatedDurationSeconds(v int32)`

SetEstimatedDurationSeconds sets EstimatedDurationSeconds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


