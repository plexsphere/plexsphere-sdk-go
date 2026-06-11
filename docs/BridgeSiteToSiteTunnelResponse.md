# BridgeSiteToSiteTunnelResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Tunnel identifier (UUIDv7). | 
**Slug** | **string** | Stable identity of the tunnel within its Resource. | 
**Kind** | [**BridgeSiteToSiteTunnelKind**](BridgeSiteToSiteTunnelKind.md) |  | 
**RemoteHost** | **string** | Hostname or address of the remote tunnel endpoint. | 
**RemotePort** | **int32** | Port on the remote tunnel endpoint. | 
**AuthSecretRef** | **string** | Opaque reference to the tunnel&#39;s authentication material in the form &#x60;secret:&lt;domain&gt;/&lt;project&gt;/&lt;name&gt;(:&lt;version&gt;)?&#x60;.  | 
**AllowedSubnets** | **[]string** | CIDR prefixes the tunnel routes. | 
**RoutingPolicy** | [**BridgeSiteToSiteTunnelRoutingPolicy**](BridgeSiteToSiteTunnelRoutingPolicy.md) |  | 
**CreatedAt** | **time.Time** | Tunnel creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). | 

## Methods

### NewBridgeSiteToSiteTunnelResponse

`func NewBridgeSiteToSiteTunnelResponse(id string, slug string, kind BridgeSiteToSiteTunnelKind, remoteHost string, remotePort int32, authSecretRef string, allowedSubnets []string, routingPolicy BridgeSiteToSiteTunnelRoutingPolicy, createdAt time.Time, updatedAt time.Time, ) *BridgeSiteToSiteTunnelResponse`

NewBridgeSiteToSiteTunnelResponse instantiates a new BridgeSiteToSiteTunnelResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeSiteToSiteTunnelResponseWithDefaults

`func NewBridgeSiteToSiteTunnelResponseWithDefaults() *BridgeSiteToSiteTunnelResponse`

NewBridgeSiteToSiteTunnelResponseWithDefaults instantiates a new BridgeSiteToSiteTunnelResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *BridgeSiteToSiteTunnelResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *BridgeSiteToSiteTunnelResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *BridgeSiteToSiteTunnelResponse) SetId(v string)`

SetId sets Id field to given value.


### GetSlug

`func (o *BridgeSiteToSiteTunnelResponse) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *BridgeSiteToSiteTunnelResponse) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *BridgeSiteToSiteTunnelResponse) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetKind

`func (o *BridgeSiteToSiteTunnelResponse) GetKind() BridgeSiteToSiteTunnelKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *BridgeSiteToSiteTunnelResponse) GetKindOk() (*BridgeSiteToSiteTunnelKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *BridgeSiteToSiteTunnelResponse) SetKind(v BridgeSiteToSiteTunnelKind)`

SetKind sets Kind field to given value.


### GetRemoteHost

`func (o *BridgeSiteToSiteTunnelResponse) GetRemoteHost() string`

GetRemoteHost returns the RemoteHost field if non-nil, zero value otherwise.

### GetRemoteHostOk

`func (o *BridgeSiteToSiteTunnelResponse) GetRemoteHostOk() (*string, bool)`

GetRemoteHostOk returns a tuple with the RemoteHost field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRemoteHost

`func (o *BridgeSiteToSiteTunnelResponse) SetRemoteHost(v string)`

SetRemoteHost sets RemoteHost field to given value.


### GetRemotePort

`func (o *BridgeSiteToSiteTunnelResponse) GetRemotePort() int32`

GetRemotePort returns the RemotePort field if non-nil, zero value otherwise.

### GetRemotePortOk

`func (o *BridgeSiteToSiteTunnelResponse) GetRemotePortOk() (*int32, bool)`

GetRemotePortOk returns a tuple with the RemotePort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRemotePort

`func (o *BridgeSiteToSiteTunnelResponse) SetRemotePort(v int32)`

SetRemotePort sets RemotePort field to given value.


### GetAuthSecretRef

`func (o *BridgeSiteToSiteTunnelResponse) GetAuthSecretRef() string`

GetAuthSecretRef returns the AuthSecretRef field if non-nil, zero value otherwise.

### GetAuthSecretRefOk

`func (o *BridgeSiteToSiteTunnelResponse) GetAuthSecretRefOk() (*string, bool)`

GetAuthSecretRefOk returns a tuple with the AuthSecretRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAuthSecretRef

`func (o *BridgeSiteToSiteTunnelResponse) SetAuthSecretRef(v string)`

SetAuthSecretRef sets AuthSecretRef field to given value.


### GetAllowedSubnets

`func (o *BridgeSiteToSiteTunnelResponse) GetAllowedSubnets() []string`

GetAllowedSubnets returns the AllowedSubnets field if non-nil, zero value otherwise.

### GetAllowedSubnetsOk

`func (o *BridgeSiteToSiteTunnelResponse) GetAllowedSubnetsOk() (*[]string, bool)`

GetAllowedSubnetsOk returns a tuple with the AllowedSubnets field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAllowedSubnets

`func (o *BridgeSiteToSiteTunnelResponse) SetAllowedSubnets(v []string)`

SetAllowedSubnets sets AllowedSubnets field to given value.


### GetRoutingPolicy

`func (o *BridgeSiteToSiteTunnelResponse) GetRoutingPolicy() BridgeSiteToSiteTunnelRoutingPolicy`

GetRoutingPolicy returns the RoutingPolicy field if non-nil, zero value otherwise.

### GetRoutingPolicyOk

`func (o *BridgeSiteToSiteTunnelResponse) GetRoutingPolicyOk() (*BridgeSiteToSiteTunnelRoutingPolicy, bool)`

GetRoutingPolicyOk returns a tuple with the RoutingPolicy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRoutingPolicy

`func (o *BridgeSiteToSiteTunnelResponse) SetRoutingPolicy(v BridgeSiteToSiteTunnelRoutingPolicy)`

SetRoutingPolicy sets RoutingPolicy field to given value.


### GetCreatedAt

`func (o *BridgeSiteToSiteTunnelResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *BridgeSiteToSiteTunnelResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *BridgeSiteToSiteTunnelResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *BridgeSiteToSiteTunnelResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *BridgeSiteToSiteTunnelResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *BridgeSiteToSiteTunnelResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


