# HeartbeatResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AcceptedAt** | **time.Time** | Server-side timestamp at which the heartbeat fact was committed. Distinct from &#x60;client_now&#x60; so the caller can estimate one-way latency and clock-skew.  | 
**Reconcile** | **bool** | When &#x60;true&#x60;, the controller is asking the caller to issue a fresh &#x60;GET /v1/nodes/{id}/state&#x60; reconciliation pull because the snapshot the caller is operating against has drifted. Defaults to &#x60;false&#x60; — later stories flip this flag when the controller observes a divergence .  | 
**RotateKeys** | **bool** | When &#x60;true&#x60;, a mesh-key rotation is pending for the heartbeating Node: the caller MUST generate a fresh Curve25519 keypair and complete the rotation via &#x60;POST /v1/keys/rotate&#x60;. This flag is load-bearing — it is the heartbeat-channel half of the two-channel rotation dispatch (the SSE &#x60;rotate_keys&#x60; event is the other half), so a Node that reconnected rather than holding a live SSE stream still learns it must rotate within one heartbeat interval. &#x60;false&#x60; when no &#x60;peer_key_rotation&#x60; row is pending for the Node.  | 

## Methods

### NewHeartbeatResponse

`func NewHeartbeatResponse(acceptedAt time.Time, reconcile bool, rotateKeys bool, ) *HeartbeatResponse`

NewHeartbeatResponse instantiates a new HeartbeatResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewHeartbeatResponseWithDefaults

`func NewHeartbeatResponseWithDefaults() *HeartbeatResponse`

NewHeartbeatResponseWithDefaults instantiates a new HeartbeatResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAcceptedAt

`func (o *HeartbeatResponse) GetAcceptedAt() time.Time`

GetAcceptedAt returns the AcceptedAt field if non-nil, zero value otherwise.

### GetAcceptedAtOk

`func (o *HeartbeatResponse) GetAcceptedAtOk() (*time.Time, bool)`

GetAcceptedAtOk returns a tuple with the AcceptedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcceptedAt

`func (o *HeartbeatResponse) SetAcceptedAt(v time.Time)`

SetAcceptedAt sets AcceptedAt field to given value.


### GetReconcile

`func (o *HeartbeatResponse) GetReconcile() bool`

GetReconcile returns the Reconcile field if non-nil, zero value otherwise.

### GetReconcileOk

`func (o *HeartbeatResponse) GetReconcileOk() (*bool, bool)`

GetReconcileOk returns a tuple with the Reconcile field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReconcile

`func (o *HeartbeatResponse) SetReconcile(v bool)`

SetReconcile sets Reconcile field to given value.


### GetRotateKeys

`func (o *HeartbeatResponse) GetRotateKeys() bool`

GetRotateKeys returns the RotateKeys field if non-nil, zero value otherwise.

### GetRotateKeysOk

`func (o *HeartbeatResponse) GetRotateKeysOk() (*bool, bool)`

GetRotateKeysOk returns a tuple with the RotateKeys field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRotateKeys

`func (o *HeartbeatResponse) SetRotateKeys(v bool)`

SetRotateKeys sets RotateKeys field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


