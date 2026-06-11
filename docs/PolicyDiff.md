# PolicyDiff

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Added** | [**[]PolicyRule**](PolicyRule.md) | Rules present in the target revision but not the source. | 
**Removed** | [**[]PolicyRule**](PolicyRule.md) | Rules present in the source revision but not the target. | 
**Modified** | [**[]PolicyDiffPair**](PolicyDiffPair.md) | Rules sharing a stable key on both sides where only the &#x60;action&#x60; field differs.  | 

## Methods

### NewPolicyDiff

`func NewPolicyDiff(added []PolicyRule, removed []PolicyRule, modified []PolicyDiffPair, ) *PolicyDiff`

NewPolicyDiff instantiates a new PolicyDiff object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyDiffWithDefaults

`func NewPolicyDiffWithDefaults() *PolicyDiff`

NewPolicyDiffWithDefaults instantiates a new PolicyDiff object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAdded

`func (o *PolicyDiff) GetAdded() []PolicyRule`

GetAdded returns the Added field if non-nil, zero value otherwise.

### GetAddedOk

`func (o *PolicyDiff) GetAddedOk() (*[]PolicyRule, bool)`

GetAddedOk returns a tuple with the Added field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAdded

`func (o *PolicyDiff) SetAdded(v []PolicyRule)`

SetAdded sets Added field to given value.


### GetRemoved

`func (o *PolicyDiff) GetRemoved() []PolicyRule`

GetRemoved returns the Removed field if non-nil, zero value otherwise.

### GetRemovedOk

`func (o *PolicyDiff) GetRemovedOk() (*[]PolicyRule, bool)`

GetRemovedOk returns a tuple with the Removed field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRemoved

`func (o *PolicyDiff) SetRemoved(v []PolicyRule)`

SetRemoved sets Removed field to given value.


### GetModified

`func (o *PolicyDiff) GetModified() []PolicyDiffPair`

GetModified returns the Modified field if non-nil, zero value otherwise.

### GetModifiedOk

`func (o *PolicyDiff) GetModifiedOk() (*[]PolicyDiffPair, bool)`

GetModifiedOk returns a tuple with the Modified field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetModified

`func (o *PolicyDiff) SetModified(v []PolicyDiffPair)`

SetModified sets Modified field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


