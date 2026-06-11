# BridgeIngressRuleList

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Rules** | [**[]BridgeIngressRuleResponse**](BridgeIngressRuleResponse.md) | Rules ordered by slug ascending. | 

## Methods

### NewBridgeIngressRuleList

`func NewBridgeIngressRuleList(rules []BridgeIngressRuleResponse, ) *BridgeIngressRuleList`

NewBridgeIngressRuleList instantiates a new BridgeIngressRuleList object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeIngressRuleListWithDefaults

`func NewBridgeIngressRuleListWithDefaults() *BridgeIngressRuleList`

NewBridgeIngressRuleListWithDefaults instantiates a new BridgeIngressRuleList object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetRules

`func (o *BridgeIngressRuleList) GetRules() []BridgeIngressRuleResponse`

GetRules returns the Rules field if non-nil, zero value otherwise.

### GetRulesOk

`func (o *BridgeIngressRuleList) GetRulesOk() (*[]BridgeIngressRuleResponse, bool)`

GetRulesOk returns a tuple with the Rules field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRules

`func (o *BridgeIngressRuleList) SetRules(v []BridgeIngressRuleResponse)`

SetRules sets Rules field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


