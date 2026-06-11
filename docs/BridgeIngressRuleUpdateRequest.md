# BridgeIngressRuleUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SniHost** | **string** | TLS SNI host the rule terminates. Unique per &#x60;(resource_id, sni_host)&#x60;; a collision surfaces as &#x60;409 slug_conflict&#x60;.  | 
**TargetNodeId** | **string** | Node the rule forwards to. A Node outside the bridge Resource&#39;s owning Domain surfaces as &#x60;400 target_node_not_in_domain&#x60;.  | 
**TargetPort** | **int32** | TCP port on the target Node. Outside &#x60;1..65535&#x60; the write is rejected with &#x60;400 relay_port_out_of_range&#x60;.  | 
**AcmeAccountRef** | Pointer to **string** | Optional opaque reference to the ACME account used to issue the rule&#39;s certificate. &#x60;null&#x60; or absent means the operator supplies certificates out of band.  | [optional] 

## Methods

### NewBridgeIngressRuleUpdateRequest

`func NewBridgeIngressRuleUpdateRequest(sniHost string, targetNodeId string, targetPort int32, ) *BridgeIngressRuleUpdateRequest`

NewBridgeIngressRuleUpdateRequest instantiates a new BridgeIngressRuleUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeIngressRuleUpdateRequestWithDefaults

`func NewBridgeIngressRuleUpdateRequestWithDefaults() *BridgeIngressRuleUpdateRequest`

NewBridgeIngressRuleUpdateRequestWithDefaults instantiates a new BridgeIngressRuleUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSniHost

`func (o *BridgeIngressRuleUpdateRequest) GetSniHost() string`

GetSniHost returns the SniHost field if non-nil, zero value otherwise.

### GetSniHostOk

`func (o *BridgeIngressRuleUpdateRequest) GetSniHostOk() (*string, bool)`

GetSniHostOk returns a tuple with the SniHost field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSniHost

`func (o *BridgeIngressRuleUpdateRequest) SetSniHost(v string)`

SetSniHost sets SniHost field to given value.


### GetTargetNodeId

`func (o *BridgeIngressRuleUpdateRequest) GetTargetNodeId() string`

GetTargetNodeId returns the TargetNodeId field if non-nil, zero value otherwise.

### GetTargetNodeIdOk

`func (o *BridgeIngressRuleUpdateRequest) GetTargetNodeIdOk() (*string, bool)`

GetTargetNodeIdOk returns a tuple with the TargetNodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetNodeId

`func (o *BridgeIngressRuleUpdateRequest) SetTargetNodeId(v string)`

SetTargetNodeId sets TargetNodeId field to given value.


### GetTargetPort

`func (o *BridgeIngressRuleUpdateRequest) GetTargetPort() int32`

GetTargetPort returns the TargetPort field if non-nil, zero value otherwise.

### GetTargetPortOk

`func (o *BridgeIngressRuleUpdateRequest) GetTargetPortOk() (*int32, bool)`

GetTargetPortOk returns a tuple with the TargetPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetPort

`func (o *BridgeIngressRuleUpdateRequest) SetTargetPort(v int32)`

SetTargetPort sets TargetPort field to given value.


### GetAcmeAccountRef

`func (o *BridgeIngressRuleUpdateRequest) GetAcmeAccountRef() string`

GetAcmeAccountRef returns the AcmeAccountRef field if non-nil, zero value otherwise.

### GetAcmeAccountRefOk

`func (o *BridgeIngressRuleUpdateRequest) GetAcmeAccountRefOk() (*string, bool)`

GetAcmeAccountRefOk returns a tuple with the AcmeAccountRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcmeAccountRef

`func (o *BridgeIngressRuleUpdateRequest) SetAcmeAccountRef(v string)`

SetAcmeAccountRef sets AcmeAccountRef field to given value.

### HasAcmeAccountRef

`func (o *BridgeIngressRuleUpdateRequest) HasAcmeAccountRef() bool`

HasAcmeAccountRef returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


