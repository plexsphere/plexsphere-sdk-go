# BridgeUserAccessProviderList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Providers** | [**[]BridgeUserAccessProviderResponse**](BridgeUserAccessProviderResponse.md) | Providers ordered by slug ascending. | 

## Methods

### NewBridgeUserAccessProviderList

`func NewBridgeUserAccessProviderList(providers []BridgeUserAccessProviderResponse, ) *BridgeUserAccessProviderList`

NewBridgeUserAccessProviderList instantiates a new BridgeUserAccessProviderList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeUserAccessProviderListWithDefaults

`func NewBridgeUserAccessProviderListWithDefaults() *BridgeUserAccessProviderList`

NewBridgeUserAccessProviderListWithDefaults instantiates a new BridgeUserAccessProviderList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetProviders

`func (o *BridgeUserAccessProviderList) GetProviders() []BridgeUserAccessProviderResponse`

GetProviders returns the Providers field if non-nil, zero value otherwise.

### GetProvidersOk

`func (o *BridgeUserAccessProviderList) GetProvidersOk() (*[]BridgeUserAccessProviderResponse, bool)`

GetProvidersOk returns a tuple with the Providers field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviders

`func (o *BridgeUserAccessProviderList) SetProviders(v []BridgeUserAccessProviderResponse)`

SetProviders sets Providers field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


