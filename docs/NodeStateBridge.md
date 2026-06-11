# NodeStateBridge

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Relay** | Pointer to [**NodeStateBridgeRelay**](NodeStateBridgeRelay.md) | Relay configuration the Node must program. &#x60;null&#x60; when no relay is configured on the owning bridge Resource.  | [optional] 
**UserAccess** | Pointer to [**NodeStateBridgeUserAccess**](NodeStateBridgeUserAccess.md) | User-access providers the Node must program. &#x60;null&#x60; when the owning bridge Resource defines none.  | [optional] 
**Ingress** | Pointer to [**NodeStateBridgeIngress**](NodeStateBridgeIngress.md) | Public-ingress rules the Node must program. &#x60;null&#x60; when the owning bridge Resource defines none.  | [optional] 
**SiteToSite** | Pointer to [**NodeStateBridgeSiteToSite**](NodeStateBridgeSiteToSite.md) | Site-to-site tunnels the Node must program. &#x60;null&#x60; when the owning bridge Resource defines none.  | [optional] 

## Methods

### NewNodeStateBridge

`func NewNodeStateBridge() *NodeStateBridge`

NewNodeStateBridge instantiates a new NodeStateBridge object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateBridgeWithDefaults

`func NewNodeStateBridgeWithDefaults() *NodeStateBridge`

NewNodeStateBridgeWithDefaults instantiates a new NodeStateBridge object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetRelay

`func (o *NodeStateBridge) GetRelay() NodeStateBridgeRelay`

GetRelay returns the Relay field if non-nil, zero value otherwise.

### GetRelayOk

`func (o *NodeStateBridge) GetRelayOk() (*NodeStateBridgeRelay, bool)`

GetRelayOk returns a tuple with the Relay field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelay

`func (o *NodeStateBridge) SetRelay(v NodeStateBridgeRelay)`

SetRelay sets Relay field to given value.

### HasRelay

`func (o *NodeStateBridge) HasRelay() bool`

HasRelay returns a boolean if a field has been set.

### GetUserAccess

`func (o *NodeStateBridge) GetUserAccess() NodeStateBridgeUserAccess`

GetUserAccess returns the UserAccess field if non-nil, zero value otherwise.

### GetUserAccessOk

`func (o *NodeStateBridge) GetUserAccessOk() (*NodeStateBridgeUserAccess, bool)`

GetUserAccessOk returns a tuple with the UserAccess field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserAccess

`func (o *NodeStateBridge) SetUserAccess(v NodeStateBridgeUserAccess)`

SetUserAccess sets UserAccess field to given value.

### HasUserAccess

`func (o *NodeStateBridge) HasUserAccess() bool`

HasUserAccess returns a boolean if a field has been set.

### GetIngress

`func (o *NodeStateBridge) GetIngress() NodeStateBridgeIngress`

GetIngress returns the Ingress field if non-nil, zero value otherwise.

### GetIngressOk

`func (o *NodeStateBridge) GetIngressOk() (*NodeStateBridgeIngress, bool)`

GetIngressOk returns a tuple with the Ingress field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIngress

`func (o *NodeStateBridge) SetIngress(v NodeStateBridgeIngress)`

SetIngress sets Ingress field to given value.

### HasIngress

`func (o *NodeStateBridge) HasIngress() bool`

HasIngress returns a boolean if a field has been set.

### GetSiteToSite

`func (o *NodeStateBridge) GetSiteToSite() NodeStateBridgeSiteToSite`

GetSiteToSite returns the SiteToSite field if non-nil, zero value otherwise.

### GetSiteToSiteOk

`func (o *NodeStateBridge) GetSiteToSiteOk() (*NodeStateBridgeSiteToSite, bool)`

GetSiteToSiteOk returns a tuple with the SiteToSite field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSiteToSite

`func (o *NodeStateBridge) SetSiteToSite(v NodeStateBridgeSiteToSite)`

SetSiteToSite sets SiteToSite field to given value.

### HasSiteToSite

`func (o *NodeStateBridge) HasSiteToSite() bool`

HasSiteToSite returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


