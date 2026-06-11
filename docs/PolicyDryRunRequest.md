# PolicyDryRunRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Selector** | [**PolicySelector**](PolicySelector.md) |  | 
**Rules** | [**[]PolicyRule**](PolicyRule.md) |  | 

## Methods

### NewPolicyDryRunRequest

`func NewPolicyDryRunRequest(selector PolicySelector, rules []PolicyRule, ) *PolicyDryRunRequest`

NewPolicyDryRunRequest instantiates a new PolicyDryRunRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyDryRunRequestWithDefaults

`func NewPolicyDryRunRequestWithDefaults() *PolicyDryRunRequest`

NewPolicyDryRunRequestWithDefaults instantiates a new PolicyDryRunRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSelector

`func (o *PolicyDryRunRequest) GetSelector() PolicySelector`

GetSelector returns the Selector field if non-nil, zero value otherwise.

### GetSelectorOk

`func (o *PolicyDryRunRequest) GetSelectorOk() (*PolicySelector, bool)`

GetSelectorOk returns a tuple with the Selector field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSelector

`func (o *PolicyDryRunRequest) SetSelector(v PolicySelector)`

SetSelector sets Selector field to given value.


### GetRules

`func (o *PolicyDryRunRequest) GetRules() []PolicyRule`

GetRules returns the Rules field if non-nil, zero value otherwise.

### GetRulesOk

`func (o *PolicyDryRunRequest) GetRulesOk() (*[]PolicyRule, bool)`

GetRulesOk returns a tuple with the Rules field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRules

`func (o *PolicyDryRunRequest) SetRules(v []PolicyRule)`

SetRules sets Rules field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


