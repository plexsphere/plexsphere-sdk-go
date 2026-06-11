# IntegrityViolationAcknowledgeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Reason** | **string** | Acknowledgement rationale. Non-empty — whitespace-only is rejected with &#x60;400 invalid_acknowledge_reason&#x60;.  | 

## Methods

### NewIntegrityViolationAcknowledgeRequest

`func NewIntegrityViolationAcknowledgeRequest(reason string, ) *IntegrityViolationAcknowledgeRequest`

NewIntegrityViolationAcknowledgeRequest instantiates a new IntegrityViolationAcknowledgeRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIntegrityViolationAcknowledgeRequestWithDefaults

`func NewIntegrityViolationAcknowledgeRequestWithDefaults() *IntegrityViolationAcknowledgeRequest`

NewIntegrityViolationAcknowledgeRequestWithDefaults instantiates a new IntegrityViolationAcknowledgeRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetReason

`func (o *IntegrityViolationAcknowledgeRequest) GetReason() string`

GetReason returns the Reason field if non-nil, zero value otherwise.

### GetReasonOk

`func (o *IntegrityViolationAcknowledgeRequest) GetReasonOk() (*string, bool)`

GetReasonOk returns a tuple with the Reason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReason

`func (o *IntegrityViolationAcknowledgeRequest) SetReason(v string)`

SetReason sets Reason field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


