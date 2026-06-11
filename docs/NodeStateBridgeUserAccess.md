# NodeStateBridgeUserAccess

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Providers** | [**[]BridgeUserAccessProviderResponse**](BridgeUserAccessProviderResponse.md) | User-access providers ordered by slug ascending. | 

## Methods

### NewNodeStateBridgeUserAccess

`func NewNodeStateBridgeUserAccess(providers []BridgeUserAccessProviderResponse, ) *NodeStateBridgeUserAccess`

NewNodeStateBridgeUserAccess instantiates a new NodeStateBridgeUserAccess object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateBridgeUserAccessWithDefaults

`func NewNodeStateBridgeUserAccessWithDefaults() *NodeStateBridgeUserAccess`

NewNodeStateBridgeUserAccessWithDefaults instantiates a new NodeStateBridgeUserAccess object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetProviders

`func (o *NodeStateBridgeUserAccess) GetProviders() []BridgeUserAccessProviderResponse`

GetProviders returns the Providers field if non-nil, zero value otherwise.

### GetProvidersOk

`func (o *NodeStateBridgeUserAccess) GetProvidersOk() (*[]BridgeUserAccessProviderResponse, bool)`

GetProvidersOk returns a tuple with the Providers field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviders

`func (o *NodeStateBridgeUserAccess) SetProviders(v []BridgeUserAccessProviderResponse)`

SetProviders sets Providers field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


