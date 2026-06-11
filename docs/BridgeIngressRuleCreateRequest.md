# BridgeIngressRuleCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Slug** | **string** | Stable identity of the rule within its Resource. Unique per &#x60;(resource_id, slug)&#x60;; a collision surfaces as &#x60;409 slug_conflict&#x60;.  | 
**SniHost** | **string** | TLS SNI host the rule terminates. Unique per &#x60;(resource_id, sni_host)&#x60;; a collision surfaces as &#x60;409 slug_conflict&#x60;.  | 
**TargetNodeId** | **string** | Node the rule forwards to. A Node outside the bridge Resource&#39;s owning Domain surfaces as &#x60;400 target_node_not_in_domain&#x60;.  | 
**TargetPort** | **int32** | TCP port on the target Node. Outside &#x60;1..65535&#x60; the write is rejected with &#x60;400 relay_port_out_of_range&#x60;.  | 
**AcmeAccountRef** | Pointer to **string** | Optional opaque reference to the ACME account used to issue the rule&#39;s certificate. &#x60;null&#x60; or absent means the operator supplies certificates out of band rather than via ACME issuance.  | [optional] 

## Methods

### NewBridgeIngressRuleCreateRequest

`func NewBridgeIngressRuleCreateRequest(slug string, sniHost string, targetNodeId string, targetPort int32, ) *BridgeIngressRuleCreateRequest`

NewBridgeIngressRuleCreateRequest instantiates a new BridgeIngressRuleCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeIngressRuleCreateRequestWithDefaults

`func NewBridgeIngressRuleCreateRequestWithDefaults() *BridgeIngressRuleCreateRequest`

NewBridgeIngressRuleCreateRequestWithDefaults instantiates a new BridgeIngressRuleCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSlug

`func (o *BridgeIngressRuleCreateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *BridgeIngressRuleCreateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *BridgeIngressRuleCreateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetSniHost

`func (o *BridgeIngressRuleCreateRequest) GetSniHost() string`

GetSniHost returns the SniHost field if non-nil, zero value otherwise.

### GetSniHostOk

`func (o *BridgeIngressRuleCreateRequest) GetSniHostOk() (*string, bool)`

GetSniHostOk returns a tuple with the SniHost field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSniHost

`func (o *BridgeIngressRuleCreateRequest) SetSniHost(v string)`

SetSniHost sets SniHost field to given value.


### GetTargetNodeId

`func (o *BridgeIngressRuleCreateRequest) GetTargetNodeId() string`

GetTargetNodeId returns the TargetNodeId field if non-nil, zero value otherwise.

### GetTargetNodeIdOk

`func (o *BridgeIngressRuleCreateRequest) GetTargetNodeIdOk() (*string, bool)`

GetTargetNodeIdOk returns a tuple with the TargetNodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetNodeId

`func (o *BridgeIngressRuleCreateRequest) SetTargetNodeId(v string)`

SetTargetNodeId sets TargetNodeId field to given value.


### GetTargetPort

`func (o *BridgeIngressRuleCreateRequest) GetTargetPort() int32`

GetTargetPort returns the TargetPort field if non-nil, zero value otherwise.

### GetTargetPortOk

`func (o *BridgeIngressRuleCreateRequest) GetTargetPortOk() (*int32, bool)`

GetTargetPortOk returns a tuple with the TargetPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetPort

`func (o *BridgeIngressRuleCreateRequest) SetTargetPort(v int32)`

SetTargetPort sets TargetPort field to given value.


### GetAcmeAccountRef

`func (o *BridgeIngressRuleCreateRequest) GetAcmeAccountRef() string`

GetAcmeAccountRef returns the AcmeAccountRef field if non-nil, zero value otherwise.

### GetAcmeAccountRefOk

`func (o *BridgeIngressRuleCreateRequest) GetAcmeAccountRefOk() (*string, bool)`

GetAcmeAccountRefOk returns a tuple with the AcmeAccountRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcmeAccountRef

`func (o *BridgeIngressRuleCreateRequest) SetAcmeAccountRef(v string)`

SetAcmeAccountRef sets AcmeAccountRef field to given value.

### HasAcmeAccountRef

`func (o *BridgeIngressRuleCreateRequest) HasAcmeAccountRef() bool`

HasAcmeAccountRef returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


