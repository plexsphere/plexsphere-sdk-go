# BridgeConfigUpdatedPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NodeId** | **string** | Addressed Node the delivered-config projection targets. Equals the &#x60;{id}&#x60; path parameter of the SSE subscription the envelope is delivered on.  | 
**BridgeResourceId** | **string** | Identifier of the bridge Resource aggregate the delivered-config projection was derived from. Two bridge Resources addressing the same Node produce two envelopes carrying distinct &#x60;bridge_resource_id&#x60; values; the consumer merges them by sorting on &#x60;bridge_resource_id&#x60; ascending.  | 
**EffectiveConfig** | [**NodeStateBridge**](NodeStateBridge.md) | The per-Node bridge-orchestrator delivered-config block the addressed Node MUST program for the named bridge Resource. Each child block is present-but-nullable so plexd&#39;s reconcile loop can diff by field presence; an all-null block is a legitimate state — it means the Node no longer matches the bridge Resource (e.g. the Resource was deleted or its selector no longer captures the Node).  | 

## Methods

### NewBridgeConfigUpdatedPayload

`func NewBridgeConfigUpdatedPayload(nodeId string, bridgeResourceId string, effectiveConfig NodeStateBridge, ) *BridgeConfigUpdatedPayload`

NewBridgeConfigUpdatedPayload instantiates a new BridgeConfigUpdatedPayload object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeConfigUpdatedPayloadWithDefaults

`func NewBridgeConfigUpdatedPayloadWithDefaults() *BridgeConfigUpdatedPayload`

NewBridgeConfigUpdatedPayloadWithDefaults instantiates a new BridgeConfigUpdatedPayload object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNodeId

`func (o *BridgeConfigUpdatedPayload) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *BridgeConfigUpdatedPayload) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *BridgeConfigUpdatedPayload) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetBridgeResourceId

`func (o *BridgeConfigUpdatedPayload) GetBridgeResourceId() string`

GetBridgeResourceId returns the BridgeResourceId field if non-nil, zero value otherwise.

### GetBridgeResourceIdOk

`func (o *BridgeConfigUpdatedPayload) GetBridgeResourceIdOk() (*string, bool)`

GetBridgeResourceIdOk returns a tuple with the BridgeResourceId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBridgeResourceId

`func (o *BridgeConfigUpdatedPayload) SetBridgeResourceId(v string)`

SetBridgeResourceId sets BridgeResourceId field to given value.


### GetEffectiveConfig

`func (o *BridgeConfigUpdatedPayload) GetEffectiveConfig() NodeStateBridge`

GetEffectiveConfig returns the EffectiveConfig field if non-nil, zero value otherwise.

### GetEffectiveConfigOk

`func (o *BridgeConfigUpdatedPayload) GetEffectiveConfigOk() (*NodeStateBridge, bool)`

GetEffectiveConfigOk returns a tuple with the EffectiveConfig field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEffectiveConfig

`func (o *BridgeConfigUpdatedPayload) SetEffectiveConfig(v NodeStateBridge)`

SetEffectiveConfig sets EffectiveConfig field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


