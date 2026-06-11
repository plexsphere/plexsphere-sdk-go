# BridgeUserAccessProviderResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Provider identifier (UUIDv7). | 
**Slug** | **string** | Stable identity of the provider within its Resource. | 
**Kind** | [**BridgeUserAccessProviderKind**](BridgeUserAccessProviderKind.md) |  | 
**InterfaceName** | **string** | Name of the network interface the provider programs on the Node. | 
**ListenPort** | **int32** | UDP port the provider listens on. | 
**MaxPeers** | **int32** | Maximum number of peers the provider admits. | 
**AuthSecretRef** | **string** | Opaque reference to the provider&#39;s authentication material in the form &#x60;secret:&lt;domain&gt;/&lt;project&gt;/&lt;name&gt;(:&lt;version&gt;)?&#x60;.  | 
**RoutingPolicy** | **map[string]interface{}** | Free-form JSON routing-policy document. | 
**CreatedAt** | **time.Time** | Provider creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). | 

## Methods

### NewBridgeUserAccessProviderResponse

`func NewBridgeUserAccessProviderResponse(id string, slug string, kind BridgeUserAccessProviderKind, interfaceName string, listenPort int32, maxPeers int32, authSecretRef string, routingPolicy map[string]interface{}, createdAt time.Time, updatedAt time.Time, ) *BridgeUserAccessProviderResponse`

NewBridgeUserAccessProviderResponse instantiates a new BridgeUserAccessProviderResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeUserAccessProviderResponseWithDefaults

`func NewBridgeUserAccessProviderResponseWithDefaults() *BridgeUserAccessProviderResponse`

NewBridgeUserAccessProviderResponseWithDefaults instantiates a new BridgeUserAccessProviderResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *BridgeUserAccessProviderResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *BridgeUserAccessProviderResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *BridgeUserAccessProviderResponse) SetId(v string)`

SetId sets Id field to given value.


### GetSlug

`func (o *BridgeUserAccessProviderResponse) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *BridgeUserAccessProviderResponse) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *BridgeUserAccessProviderResponse) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetKind

`func (o *BridgeUserAccessProviderResponse) GetKind() BridgeUserAccessProviderKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *BridgeUserAccessProviderResponse) GetKindOk() (*BridgeUserAccessProviderKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *BridgeUserAccessProviderResponse) SetKind(v BridgeUserAccessProviderKind)`

SetKind sets Kind field to given value.


### GetInterfaceName

`func (o *BridgeUserAccessProviderResponse) GetInterfaceName() string`

GetInterfaceName returns the InterfaceName field if non-nil, zero value otherwise.

### GetInterfaceNameOk

`func (o *BridgeUserAccessProviderResponse) GetInterfaceNameOk() (*string, bool)`

GetInterfaceNameOk returns a tuple with the InterfaceName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInterfaceName

`func (o *BridgeUserAccessProviderResponse) SetInterfaceName(v string)`

SetInterfaceName sets InterfaceName field to given value.


### GetListenPort

`func (o *BridgeUserAccessProviderResponse) GetListenPort() int32`

GetListenPort returns the ListenPort field if non-nil, zero value otherwise.

### GetListenPortOk

`func (o *BridgeUserAccessProviderResponse) GetListenPortOk() (*int32, bool)`

GetListenPortOk returns a tuple with the ListenPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetListenPort

`func (o *BridgeUserAccessProviderResponse) SetListenPort(v int32)`

SetListenPort sets ListenPort field to given value.


### GetMaxPeers

`func (o *BridgeUserAccessProviderResponse) GetMaxPeers() int32`

GetMaxPeers returns the MaxPeers field if non-nil, zero value otherwise.

### GetMaxPeersOk

`func (o *BridgeUserAccessProviderResponse) GetMaxPeersOk() (*int32, bool)`

GetMaxPeersOk returns a tuple with the MaxPeers field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMaxPeers

`func (o *BridgeUserAccessProviderResponse) SetMaxPeers(v int32)`

SetMaxPeers sets MaxPeers field to given value.


### GetAuthSecretRef

`func (o *BridgeUserAccessProviderResponse) GetAuthSecretRef() string`

GetAuthSecretRef returns the AuthSecretRef field if non-nil, zero value otherwise.

### GetAuthSecretRefOk

`func (o *BridgeUserAccessProviderResponse) GetAuthSecretRefOk() (*string, bool)`

GetAuthSecretRefOk returns a tuple with the AuthSecretRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAuthSecretRef

`func (o *BridgeUserAccessProviderResponse) SetAuthSecretRef(v string)`

SetAuthSecretRef sets AuthSecretRef field to given value.


### GetRoutingPolicy

`func (o *BridgeUserAccessProviderResponse) GetRoutingPolicy() map[string]interface{}`

GetRoutingPolicy returns the RoutingPolicy field if non-nil, zero value otherwise.

### GetRoutingPolicyOk

`func (o *BridgeUserAccessProviderResponse) GetRoutingPolicyOk() (*map[string]interface{}, bool)`

GetRoutingPolicyOk returns a tuple with the RoutingPolicy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRoutingPolicy

`func (o *BridgeUserAccessProviderResponse) SetRoutingPolicy(v map[string]interface{})`

SetRoutingPolicy sets RoutingPolicy field to given value.


### GetCreatedAt

`func (o *BridgeUserAccessProviderResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *BridgeUserAccessProviderResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *BridgeUserAccessProviderResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *BridgeUserAccessProviderResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *BridgeUserAccessProviderResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *BridgeUserAccessProviderResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


