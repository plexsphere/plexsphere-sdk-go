# BridgeIngressRuleList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**[]BridgeIngressRuleResponse**](BridgeIngressRuleResponse.md) | Rules ordered by slug ascending. | 

## Methods

### NewBridgeIngressRuleList

`func NewBridgeIngressRuleList(items []BridgeIngressRuleResponse, ) *BridgeIngressRuleList`

NewBridgeIngressRuleList instantiates a new BridgeIngressRuleList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeIngressRuleListWithDefaults

`func NewBridgeIngressRuleListWithDefaults() *BridgeIngressRuleList`

NewBridgeIngressRuleListWithDefaults instantiates a new BridgeIngressRuleList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetItems

`func (o *BridgeIngressRuleList) GetItems() []BridgeIngressRuleResponse`

GetItems returns the Items field if non-nil, zero value otherwise.

### GetItemsOk

`func (o *BridgeIngressRuleList) GetItemsOk() (*[]BridgeIngressRuleResponse, bool)`

GetItemsOk returns a tuple with the Items field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetItems

`func (o *BridgeIngressRuleList) SetItems(v []BridgeIngressRuleResponse)`

SetItems sets Items field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


