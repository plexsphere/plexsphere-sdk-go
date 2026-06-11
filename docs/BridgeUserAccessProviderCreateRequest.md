# BridgeUserAccessProviderCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Slug** | **string** | Stable identity of the provider within its Resource. Unique per &#x60;(resource_id, slug)&#x60;; a collision surfaces as &#x60;409 slug_conflict&#x60;.  | 
**Kind** | [**BridgeUserAccessProviderKind**](BridgeUserAccessProviderKind.md) |  | 
**InterfaceName** | **string** | Name of the network interface the provider programs on the Node. | 
**ListenPort** | **int32** | UDP port the provider listens on. Outside &#x60;1..65535&#x60; the write is rejected with &#x60;400 relay_port_out_of_range&#x60;.  | 
**MaxPeers** | **int32** | Maximum number of peers the provider admits. | 
**AuthSecretRef** | **string** | Opaque reference to the provider&#39;s authentication material in the form &#x60;secret:&lt;domain&gt;/&lt;project&gt;/&lt;name&gt;(:&lt;version&gt;)?&#x60;. The platform stores the reference, never the material; a malformed reference surfaces as &#x60;400 secret_ref_malformed&#x60;.  | 
**RoutingPolicy** | **map[string]interface{}** | Free-form JSON routing-policy document, persisted as JSONB. The platform stores it opaquely; the agent-side driver interprets it.  | 

## Methods

### NewBridgeUserAccessProviderCreateRequest

`func NewBridgeUserAccessProviderCreateRequest(slug string, kind BridgeUserAccessProviderKind, interfaceName string, listenPort int32, maxPeers int32, authSecretRef string, routingPolicy map[string]interface{}, ) *BridgeUserAccessProviderCreateRequest`

NewBridgeUserAccessProviderCreateRequest instantiates a new BridgeUserAccessProviderCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeUserAccessProviderCreateRequestWithDefaults

`func NewBridgeUserAccessProviderCreateRequestWithDefaults() *BridgeUserAccessProviderCreateRequest`

NewBridgeUserAccessProviderCreateRequestWithDefaults instantiates a new BridgeUserAccessProviderCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSlug

`func (o *BridgeUserAccessProviderCreateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *BridgeUserAccessProviderCreateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *BridgeUserAccessProviderCreateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetKind

`func (o *BridgeUserAccessProviderCreateRequest) GetKind() BridgeUserAccessProviderKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *BridgeUserAccessProviderCreateRequest) GetKindOk() (*BridgeUserAccessProviderKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *BridgeUserAccessProviderCreateRequest) SetKind(v BridgeUserAccessProviderKind)`

SetKind sets Kind field to given value.


### GetInterfaceName

`func (o *BridgeUserAccessProviderCreateRequest) GetInterfaceName() string`

GetInterfaceName returns the InterfaceName field if non-nil, zero value otherwise.

### GetInterfaceNameOk

`func (o *BridgeUserAccessProviderCreateRequest) GetInterfaceNameOk() (*string, bool)`

GetInterfaceNameOk returns a tuple with the InterfaceName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInterfaceName

`func (o *BridgeUserAccessProviderCreateRequest) SetInterfaceName(v string)`

SetInterfaceName sets InterfaceName field to given value.


### GetListenPort

`func (o *BridgeUserAccessProviderCreateRequest) GetListenPort() int32`

GetListenPort returns the ListenPort field if non-nil, zero value otherwise.

### GetListenPortOk

`func (o *BridgeUserAccessProviderCreateRequest) GetListenPortOk() (*int32, bool)`

GetListenPortOk returns a tuple with the ListenPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetListenPort

`func (o *BridgeUserAccessProviderCreateRequest) SetListenPort(v int32)`

SetListenPort sets ListenPort field to given value.


### GetMaxPeers

`func (o *BridgeUserAccessProviderCreateRequest) GetMaxPeers() int32`

GetMaxPeers returns the MaxPeers field if non-nil, zero value otherwise.

### GetMaxPeersOk

`func (o *BridgeUserAccessProviderCreateRequest) GetMaxPeersOk() (*int32, bool)`

GetMaxPeersOk returns a tuple with the MaxPeers field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMaxPeers

`func (o *BridgeUserAccessProviderCreateRequest) SetMaxPeers(v int32)`

SetMaxPeers sets MaxPeers field to given value.


### GetAuthSecretRef

`func (o *BridgeUserAccessProviderCreateRequest) GetAuthSecretRef() string`

GetAuthSecretRef returns the AuthSecretRef field if non-nil, zero value otherwise.

### GetAuthSecretRefOk

`func (o *BridgeUserAccessProviderCreateRequest) GetAuthSecretRefOk() (*string, bool)`

GetAuthSecretRefOk returns a tuple with the AuthSecretRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAuthSecretRef

`func (o *BridgeUserAccessProviderCreateRequest) SetAuthSecretRef(v string)`

SetAuthSecretRef sets AuthSecretRef field to given value.


### GetRoutingPolicy

`func (o *BridgeUserAccessProviderCreateRequest) GetRoutingPolicy() map[string]interface{}`

GetRoutingPolicy returns the RoutingPolicy field if non-nil, zero value otherwise.

### GetRoutingPolicyOk

`func (o *BridgeUserAccessProviderCreateRequest) GetRoutingPolicyOk() (*map[string]interface{}, bool)`

GetRoutingPolicyOk returns a tuple with the RoutingPolicy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRoutingPolicy

`func (o *BridgeUserAccessProviderCreateRequest) SetRoutingPolicy(v map[string]interface{})`

SetRoutingPolicy sets RoutingPolicy field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


