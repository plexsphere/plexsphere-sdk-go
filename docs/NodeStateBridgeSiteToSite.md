# NodeStateBridgeSiteToSite

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Tunnels** | [**[]BridgeSiteToSiteTunnelResponse**](BridgeSiteToSiteTunnelResponse.md) | Site-to-site tunnels ordered by slug ascending. | 

## Methods

### NewNodeStateBridgeSiteToSite

`func NewNodeStateBridgeSiteToSite(tunnels []BridgeSiteToSiteTunnelResponse, ) *NodeStateBridgeSiteToSite`

NewNodeStateBridgeSiteToSite instantiates a new NodeStateBridgeSiteToSite object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateBridgeSiteToSiteWithDefaults

`func NewNodeStateBridgeSiteToSiteWithDefaults() *NodeStateBridgeSiteToSite`

NewNodeStateBridgeSiteToSiteWithDefaults instantiates a new NodeStateBridgeSiteToSite object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetTunnels

`func (o *NodeStateBridgeSiteToSite) GetTunnels() []BridgeSiteToSiteTunnelResponse`

GetTunnels returns the Tunnels field if non-nil, zero value otherwise.

### GetTunnelsOk

`func (o *NodeStateBridgeSiteToSite) GetTunnelsOk() (*[]BridgeSiteToSiteTunnelResponse, bool)`

GetTunnelsOk returns a tuple with the Tunnels field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTunnels

`func (o *NodeStateBridgeSiteToSite) SetTunnels(v []BridgeSiteToSiteTunnelResponse)`

SetTunnels sets Tunnels field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


