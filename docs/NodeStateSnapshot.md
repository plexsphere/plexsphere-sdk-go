# NodeStateSnapshot

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Peers** | [**[]NodeStatePeer**](NodeStatePeer.md) | Peer set the addressed Node should program into its WireGuard table. One entry per other Node in the addressed Node&#39;s Domain — the addressed Node itself is excluded so plexd does not program a self-peer . Ordered by &#x60;node_id&#x60; ascending so two consecutive pulls against the same ledger snapshot are byte-equal.  | 
**Reachability** | [**Reachability**](Reachability.md) | Latest &#x60;Reachability&#x60; projection for the addressed Node, carried inside the reconciliation-pull payload so plexd sees the same health view that &#x60;GET /v1/nodes/{id}/reachability&#x60; exposes without an additional round-trip.  | 
**Policy** | [**NodeStatePolicy**](NodeStatePolicy.md) | Policy block — present-but-empty placeholder populates the wire shape. May be &#x60;null&#x60; until then; the field itself is always present so plexd&#39;s reconcile loop can diff by field presence.  | 
**Bridge** | [**NodeStateBridge**](NodeStateBridge.md) | Bridge orchestrator block — present-but-empty placeholder  populates the wire shape. May be &#x60;null&#x60; until then; the field itself is always present.  | 
**State** | [**NodeStateReports**](NodeStateReports.md) | Node-state block for the addressed Node: its node-state entries fanned into the &#x60;metadata&#x60;, &#x60;data&#x60;, and &#x60;reports&#x60; buckets of &#x60;NodeStateReports&#x60;. Populated after a successful reconciliation pull — each bucket is &#x60;[]&#x60; (never &#x60;null&#x60;) when the Node carries no entry of that kind. The field is always present so plexd&#39;s reconcile loop can diff by field presence; it is &#x60;null&#x60; only when the snapshot carries no node-state projection at all.  | 
**Reports** | [**NodeStateReports**](NodeStateReports.md) | Forward-compatibility mirror of &#x60;state&#x60;: the controller points it at the same &#x60;NodeStateReports&#x60; value so the convergence with the SSE event taxonomy stays explicit and a future split between live state and rolled-up reports lands without an OpenAPI break. Always equals &#x60;state&#x60; today. The field is always present and is &#x60;null&#x60; only when &#x60;state&#x60; is.  | 

## Methods

### NewNodeStateSnapshot

`func NewNodeStateSnapshot(peers []NodeStatePeer, reachability Reachability, policy NodeStatePolicy, bridge NodeStateBridge, state NodeStateReports, reports NodeStateReports, ) *NodeStateSnapshot`

NewNodeStateSnapshot instantiates a new NodeStateSnapshot object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateSnapshotWithDefaults

`func NewNodeStateSnapshotWithDefaults() *NodeStateSnapshot`

NewNodeStateSnapshotWithDefaults instantiates a new NodeStateSnapshot object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPeers

`func (o *NodeStateSnapshot) GetPeers() []NodeStatePeer`

GetPeers returns the Peers field if non-nil, zero value otherwise.

### GetPeersOk

`func (o *NodeStateSnapshot) GetPeersOk() (*[]NodeStatePeer, bool)`

GetPeersOk returns a tuple with the Peers field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPeers

`func (o *NodeStateSnapshot) SetPeers(v []NodeStatePeer)`

SetPeers sets Peers field to given value.


### GetReachability

`func (o *NodeStateSnapshot) GetReachability() Reachability`

GetReachability returns the Reachability field if non-nil, zero value otherwise.

### GetReachabilityOk

`func (o *NodeStateSnapshot) GetReachabilityOk() (*Reachability, bool)`

GetReachabilityOk returns a tuple with the Reachability field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReachability

`func (o *NodeStateSnapshot) SetReachability(v Reachability)`

SetReachability sets Reachability field to given value.


### GetPolicy

`func (o *NodeStateSnapshot) GetPolicy() NodeStatePolicy`

GetPolicy returns the Policy field if non-nil, zero value otherwise.

### GetPolicyOk

`func (o *NodeStateSnapshot) GetPolicyOk() (*NodeStatePolicy, bool)`

GetPolicyOk returns a tuple with the Policy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPolicy

`func (o *NodeStateSnapshot) SetPolicy(v NodeStatePolicy)`

SetPolicy sets Policy field to given value.


### GetBridge

`func (o *NodeStateSnapshot) GetBridge() NodeStateBridge`

GetBridge returns the Bridge field if non-nil, zero value otherwise.

### GetBridgeOk

`func (o *NodeStateSnapshot) GetBridgeOk() (*NodeStateBridge, bool)`

GetBridgeOk returns a tuple with the Bridge field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBridge

`func (o *NodeStateSnapshot) SetBridge(v NodeStateBridge)`

SetBridge sets Bridge field to given value.


### GetState

`func (o *NodeStateSnapshot) GetState() NodeStateReports`

GetState returns the State field if non-nil, zero value otherwise.

### GetStateOk

`func (o *NodeStateSnapshot) GetStateOk() (*NodeStateReports, bool)`

GetStateOk returns a tuple with the State field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetState

`func (o *NodeStateSnapshot) SetState(v NodeStateReports)`

SetState sets State field to given value.


### GetReports

`func (o *NodeStateSnapshot) GetReports() NodeStateReports`

GetReports returns the Reports field if non-nil, zero value otherwise.

### GetReportsOk

`func (o *NodeStateSnapshot) GetReportsOk() (*NodeStateReports, bool)`

GetReportsOk returns a tuple with the Reports field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReports

`func (o *NodeStateSnapshot) SetReports(v NodeStateReports)`

SetReports sets Reports field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


