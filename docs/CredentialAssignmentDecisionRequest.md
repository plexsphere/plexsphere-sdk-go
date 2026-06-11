# CredentialAssignmentDecisionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Reason** | **string** | Decision rationale. Non-empty — whitespace-only is rejected with &#x60;400 invalid_decision_reason&#x60;.  | 

## Methods

### NewCredentialAssignmentDecisionRequest

`func NewCredentialAssignmentDecisionRequest(reason string, ) *CredentialAssignmentDecisionRequest`

NewCredentialAssignmentDecisionRequest instantiates a new CredentialAssignmentDecisionRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCredentialAssignmentDecisionRequestWithDefaults

`func NewCredentialAssignmentDecisionRequestWithDefaults() *CredentialAssignmentDecisionRequest`

NewCredentialAssignmentDecisionRequestWithDefaults instantiates a new CredentialAssignmentDecisionRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetReason

`func (o *CredentialAssignmentDecisionRequest) GetReason() string`

GetReason returns the Reason field if non-nil, zero value otherwise.

### GetReasonOk

`func (o *CredentialAssignmentDecisionRequest) GetReasonOk() (*string, bool)`

GetReasonOk returns a tuple with the Reason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReason

`func (o *CredentialAssignmentDecisionRequest) SetReason(v string)`

SetReason sets Reason field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


