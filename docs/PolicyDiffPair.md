# PolicyDiffPair

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Before** | [**PolicyRule**](PolicyRule.md) |  | 
**After** | [**PolicyRule**](PolicyRule.md) |  | 

## Methods

### NewPolicyDiffPair

`func NewPolicyDiffPair(before PolicyRule, after PolicyRule, ) *PolicyDiffPair`

NewPolicyDiffPair instantiates a new PolicyDiffPair object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyDiffPairWithDefaults

`func NewPolicyDiffPairWithDefaults() *PolicyDiffPair`

NewPolicyDiffPairWithDefaults instantiates a new PolicyDiffPair object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetBefore

`func (o *PolicyDiffPair) GetBefore() PolicyRule`

GetBefore returns the Before field if non-nil, zero value otherwise.

### GetBeforeOk

`func (o *PolicyDiffPair) GetBeforeOk() (*PolicyRule, bool)`

GetBeforeOk returns a tuple with the Before field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBefore

`func (o *PolicyDiffPair) SetBefore(v PolicyRule)`

SetBefore sets Before field to given value.


### GetAfter

`func (o *PolicyDiffPair) GetAfter() PolicyRule`

GetAfter returns the After field if non-nil, zero value otherwise.

### GetAfterOk

`func (o *PolicyDiffPair) GetAfterOk() (*PolicyRule, bool)`

GetAfterOk returns a tuple with the After field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAfter

`func (o *PolicyDiffPair) SetAfter(v PolicyRule)`

SetAfter sets After field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


