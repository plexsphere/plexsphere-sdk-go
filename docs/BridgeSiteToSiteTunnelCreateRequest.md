# BridgeSiteToSiteTunnelCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Slug** | **string** | Stable identity of the tunnel within its Resource. Unique per &#x60;(resource_id, slug)&#x60;; a collision surfaces as &#x60;409 slug_conflict&#x60;.  | 
**Kind** | [**BridgeSiteToSiteTunnelKind**](BridgeSiteToSiteTunnelKind.md) |  | 
**RemoteHost** | **string** | Hostname or address of the remote tunnel endpoint. | 
**RemotePort** | **int32** | Port on the remote tunnel endpoint. Outside &#x60;1..65535&#x60; the write is rejected with &#x60;400 relay_port_out_of_range&#x60;.  | 
**AuthSecretRef** | **string** | Opaque reference to the tunnel&#39;s authentication material in the form &#x60;secret:&lt;domain&gt;/&lt;project&gt;/&lt;name&gt;(:&lt;version&gt;)?&#x60;. The platform stores the reference, never the material; a malformed reference surfaces as &#x60;400 secret_ref_malformed&#x60;.  | 
**AllowedSubnets** | **[]string** | CIDR prefixes the tunnel routes. An empty list surfaces as &#x60;400 allowed_subnet_empty&#x60;.  | 
**RoutingPolicy** | [**BridgeSiteToSiteTunnelRoutingPolicy**](BridgeSiteToSiteTunnelRoutingPolicy.md) |  | 

## Methods

### NewBridgeSiteToSiteTunnelCreateRequest

`func NewBridgeSiteToSiteTunnelCreateRequest(slug string, kind BridgeSiteToSiteTunnelKind, remoteHost string, remotePort int32, authSecretRef string, allowedSubnets []string, routingPolicy BridgeSiteToSiteTunnelRoutingPolicy, ) *BridgeSiteToSiteTunnelCreateRequest`

NewBridgeSiteToSiteTunnelCreateRequest instantiates a new BridgeSiteToSiteTunnelCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeSiteToSiteTunnelCreateRequestWithDefaults

`func NewBridgeSiteToSiteTunnelCreateRequestWithDefaults() *BridgeSiteToSiteTunnelCreateRequest`

NewBridgeSiteToSiteTunnelCreateRequestWithDefaults instantiates a new BridgeSiteToSiteTunnelCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSlug

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *BridgeSiteToSiteTunnelCreateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetKind

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetKind() BridgeSiteToSiteTunnelKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetKindOk() (*BridgeSiteToSiteTunnelKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *BridgeSiteToSiteTunnelCreateRequest) SetKind(v BridgeSiteToSiteTunnelKind)`

SetKind sets Kind field to given value.


### GetRemoteHost

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetRemoteHost() string`

GetRemoteHost returns the RemoteHost field if non-nil, zero value otherwise.

### GetRemoteHostOk

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetRemoteHostOk() (*string, bool)`

GetRemoteHostOk returns a tuple with the RemoteHost field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRemoteHost

`func (o *BridgeSiteToSiteTunnelCreateRequest) SetRemoteHost(v string)`

SetRemoteHost sets RemoteHost field to given value.


### GetRemotePort

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetRemotePort() int32`

GetRemotePort returns the RemotePort field if non-nil, zero value otherwise.

### GetRemotePortOk

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetRemotePortOk() (*int32, bool)`

GetRemotePortOk returns a tuple with the RemotePort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRemotePort

`func (o *BridgeSiteToSiteTunnelCreateRequest) SetRemotePort(v int32)`

SetRemotePort sets RemotePort field to given value.


### GetAuthSecretRef

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetAuthSecretRef() string`

GetAuthSecretRef returns the AuthSecretRef field if non-nil, zero value otherwise.

### GetAuthSecretRefOk

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetAuthSecretRefOk() (*string, bool)`

GetAuthSecretRefOk returns a tuple with the AuthSecretRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAuthSecretRef

`func (o *BridgeSiteToSiteTunnelCreateRequest) SetAuthSecretRef(v string)`

SetAuthSecretRef sets AuthSecretRef field to given value.


### GetAllowedSubnets

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetAllowedSubnets() []string`

GetAllowedSubnets returns the AllowedSubnets field if non-nil, zero value otherwise.

### GetAllowedSubnetsOk

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetAllowedSubnetsOk() (*[]string, bool)`

GetAllowedSubnetsOk returns a tuple with the AllowedSubnets field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAllowedSubnets

`func (o *BridgeSiteToSiteTunnelCreateRequest) SetAllowedSubnets(v []string)`

SetAllowedSubnets sets AllowedSubnets field to given value.


### GetRoutingPolicy

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetRoutingPolicy() BridgeSiteToSiteTunnelRoutingPolicy`

GetRoutingPolicy returns the RoutingPolicy field if non-nil, zero value otherwise.

### GetRoutingPolicyOk

`func (o *BridgeSiteToSiteTunnelCreateRequest) GetRoutingPolicyOk() (*BridgeSiteToSiteTunnelRoutingPolicy, bool)`

GetRoutingPolicyOk returns a tuple with the RoutingPolicy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRoutingPolicy

`func (o *BridgeSiteToSiteTunnelCreateRequest) SetRoutingPolicy(v BridgeSiteToSiteTunnelRoutingPolicy)`

SetRoutingPolicy sets RoutingPolicy field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


