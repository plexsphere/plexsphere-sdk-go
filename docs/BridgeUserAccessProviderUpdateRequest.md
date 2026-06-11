# BridgeUserAccessProviderUpdateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | [**BridgeUserAccessProviderKind**](BridgeUserAccessProviderKind.md) |  | 
**InterfaceName** | **string** | Name of the network interface the provider programs on the Node. | 
**ListenPort** | **int32** | UDP port the provider listens on. Outside &#x60;1..65535&#x60; the write is rejected with &#x60;400 relay_port_out_of_range&#x60;.  | 
**MaxPeers** | **int32** | Maximum number of peers the provider admits. | 
**AuthSecretRef** | **string** | Opaque reference to the provider&#39;s authentication material in the form &#x60;secret:&lt;domain&gt;/&lt;project&gt;/&lt;name&gt;(:&lt;version&gt;)?&#x60;. The platform stores the reference, never the material; a malformed reference surfaces as &#x60;400 secret_ref_malformed&#x60;.  | 
**RoutingPolicy** | **map[string]interface{}** | Free-form JSON routing-policy document, persisted as JSONB.  | 

## Methods

### NewBridgeUserAccessProviderUpdateRequest

`func NewBridgeUserAccessProviderUpdateRequest(kind BridgeUserAccessProviderKind, interfaceName string, listenPort int32, maxPeers int32, authSecretRef string, routingPolicy map[string]interface{}, ) *BridgeUserAccessProviderUpdateRequest`

NewBridgeUserAccessProviderUpdateRequest instantiates a new BridgeUserAccessProviderUpdateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeUserAccessProviderUpdateRequestWithDefaults

`func NewBridgeUserAccessProviderUpdateRequestWithDefaults() *BridgeUserAccessProviderUpdateRequest`

NewBridgeUserAccessProviderUpdateRequestWithDefaults instantiates a new BridgeUserAccessProviderUpdateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKind

`func (o *BridgeUserAccessProviderUpdateRequest) GetKind() BridgeUserAccessProviderKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *BridgeUserAccessProviderUpdateRequest) GetKindOk() (*BridgeUserAccessProviderKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *BridgeUserAccessProviderUpdateRequest) SetKind(v BridgeUserAccessProviderKind)`

SetKind sets Kind field to given value.


### GetInterfaceName

`func (o *BridgeUserAccessProviderUpdateRequest) GetInterfaceName() string`

GetInterfaceName returns the InterfaceName field if non-nil, zero value otherwise.

### GetInterfaceNameOk

`func (o *BridgeUserAccessProviderUpdateRequest) GetInterfaceNameOk() (*string, bool)`

GetInterfaceNameOk returns a tuple with the InterfaceName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInterfaceName

`func (o *BridgeUserAccessProviderUpdateRequest) SetInterfaceName(v string)`

SetInterfaceName sets InterfaceName field to given value.


### GetListenPort

`func (o *BridgeUserAccessProviderUpdateRequest) GetListenPort() int32`

GetListenPort returns the ListenPort field if non-nil, zero value otherwise.

### GetListenPortOk

`func (o *BridgeUserAccessProviderUpdateRequest) GetListenPortOk() (*int32, bool)`

GetListenPortOk returns a tuple with the ListenPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetListenPort

`func (o *BridgeUserAccessProviderUpdateRequest) SetListenPort(v int32)`

SetListenPort sets ListenPort field to given value.


### GetMaxPeers

`func (o *BridgeUserAccessProviderUpdateRequest) GetMaxPeers() int32`

GetMaxPeers returns the MaxPeers field if non-nil, zero value otherwise.

### GetMaxPeersOk

`func (o *BridgeUserAccessProviderUpdateRequest) GetMaxPeersOk() (*int32, bool)`

GetMaxPeersOk returns a tuple with the MaxPeers field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMaxPeers

`func (o *BridgeUserAccessProviderUpdateRequest) SetMaxPeers(v int32)`

SetMaxPeers sets MaxPeers field to given value.


### GetAuthSecretRef

`func (o *BridgeUserAccessProviderUpdateRequest) GetAuthSecretRef() string`

GetAuthSecretRef returns the AuthSecretRef field if non-nil, zero value otherwise.

### GetAuthSecretRefOk

`func (o *BridgeUserAccessProviderUpdateRequest) GetAuthSecretRefOk() (*string, bool)`

GetAuthSecretRefOk returns a tuple with the AuthSecretRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAuthSecretRef

`func (o *BridgeUserAccessProviderUpdateRequest) SetAuthSecretRef(v string)`

SetAuthSecretRef sets AuthSecretRef field to given value.


### GetRoutingPolicy

`func (o *BridgeUserAccessProviderUpdateRequest) GetRoutingPolicy() map[string]interface{}`

GetRoutingPolicy returns the RoutingPolicy field if non-nil, zero value otherwise.

### GetRoutingPolicyOk

`func (o *BridgeUserAccessProviderUpdateRequest) GetRoutingPolicyOk() (*map[string]interface{}, bool)`

GetRoutingPolicyOk returns a tuple with the RoutingPolicy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRoutingPolicy

`func (o *BridgeUserAccessProviderUpdateRequest) SetRoutingPolicy(v map[string]interface{})`

SetRoutingPolicy sets RoutingPolicy field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


