# ApprovalPolicy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Rules** | Pointer to [**[]ApprovalPolicyRulesInner**](ApprovalPolicyRulesInner.md) | Matching rules. A nil or empty list is the empty policy and gates no action.  | [optional] 

## Methods

### NewApprovalPolicy

`func NewApprovalPolicy() *ApprovalPolicy`

NewApprovalPolicy instantiates a new ApprovalPolicy object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewApprovalPolicyWithDefaults

`func NewApprovalPolicyWithDefaults() *ApprovalPolicy`

NewApprovalPolicyWithDefaults instantiates a new ApprovalPolicy object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetRules

`func (o *ApprovalPolicy) GetRules() []ApprovalPolicyRulesInner`

GetRules returns the Rules field if non-nil, zero value otherwise.

### GetRulesOk

`func (o *ApprovalPolicy) GetRulesOk() (*[]ApprovalPolicyRulesInner, bool)`

GetRulesOk returns a tuple with the Rules field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRules

`func (o *ApprovalPolicy) SetRules(v []ApprovalPolicyRulesInner)`

SetRules sets Rules field to given value.

### HasRules

`func (o *ApprovalPolicy) HasRules() bool`

HasRules returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


