# ApprovalPolicyRulesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ActionKind** | **string** | Action kind the rule matches. Must be non-empty for the rule to be valid.  | 
**TargetResource** | Pointer to **string** | Optional resource the rule narrows to. An empty value is a wildcard that matches any target for the given action kind.  | [optional] 
**ApproversRequired** | **int32** | Number of distinct approvers the matched action requires. Must be at least one.  | 

## Methods

### NewApprovalPolicyRulesInner

`func NewApprovalPolicyRulesInner(actionKind string, approversRequired int32, ) *ApprovalPolicyRulesInner`

NewApprovalPolicyRulesInner instantiates a new ApprovalPolicyRulesInner object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewApprovalPolicyRulesInnerWithDefaults

`func NewApprovalPolicyRulesInnerWithDefaults() *ApprovalPolicyRulesInner`

NewApprovalPolicyRulesInnerWithDefaults instantiates a new ApprovalPolicyRulesInner object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetActionKind

`func (o *ApprovalPolicyRulesInner) GetActionKind() string`

GetActionKind returns the ActionKind field if non-nil, zero value otherwise.

### GetActionKindOk

`func (o *ApprovalPolicyRulesInner) GetActionKindOk() (*string, bool)`

GetActionKindOk returns a tuple with the ActionKind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetActionKind

`func (o *ApprovalPolicyRulesInner) SetActionKind(v string)`

SetActionKind sets ActionKind field to given value.


### GetTargetResource

`func (o *ApprovalPolicyRulesInner) GetTargetResource() string`

GetTargetResource returns the TargetResource field if non-nil, zero value otherwise.

### GetTargetResourceOk

`func (o *ApprovalPolicyRulesInner) GetTargetResourceOk() (*string, bool)`

GetTargetResourceOk returns a tuple with the TargetResource field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetResource

`func (o *ApprovalPolicyRulesInner) SetTargetResource(v string)`

SetTargetResource sets TargetResource field to given value.

### HasTargetResource

`func (o *ApprovalPolicyRulesInner) HasTargetResource() bool`

HasTargetResource returns a boolean if a field has been set.

### GetApproversRequired

`func (o *ApprovalPolicyRulesInner) GetApproversRequired() int32`

GetApproversRequired returns the ApproversRequired field if non-nil, zero value otherwise.

### GetApproversRequiredOk

`func (o *ApprovalPolicyRulesInner) GetApproversRequiredOk() (*int32, bool)`

GetApproversRequiredOk returns a tuple with the ApproversRequired field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetApproversRequired

`func (o *ApprovalPolicyRulesInner) SetApproversRequired(v int32)`

SetApproversRequired sets ApproversRequired field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


