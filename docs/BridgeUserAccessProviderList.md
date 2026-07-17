# BridgeUserAccessProviderList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]BridgeUserAccessProviderResponse**](BridgeUserAccessProviderResponse.md) | Providers ordered by slug ascending. | 

## Methods

### NewBridgeUserAccessProviderList

`func NewBridgeUserAccessProviderList(items []BridgeUserAccessProviderResponse, ) *BridgeUserAccessProviderList`

NewBridgeUserAccessProviderList instantiates a new BridgeUserAccessProviderList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeUserAccessProviderListWithDefaults

`func NewBridgeUserAccessProviderListWithDefaults() *BridgeUserAccessProviderList`

NewBridgeUserAccessProviderListWithDefaults instantiates a new BridgeUserAccessProviderList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *BridgeUserAccessProviderList) GetItems() []BridgeUserAccessProviderResponse`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *BridgeUserAccessProviderList) GetItemsOk() (*[]BridgeUserAccessProviderResponse, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *BridgeUserAccessProviderList) SetItems(v []BridgeUserAccessProviderResponse)`

SetItems sets Items field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


