# IntegrityViolationsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Violations** | [**[]IntegrityViolationRequest**](IntegrityViolationRequest.md) | The per-violation reports the agent observed. Empty or larger-than-128 batches are rejected with 400 &#x60;integrity_violations_empty&#x60; or &#x60;integrity_violations_too_many&#x60; respectively.  | 

## Methods

### NewIntegrityViolationsRequest

`func NewIntegrityViolationsRequest(violations []IntegrityViolationRequest, ) *IntegrityViolationsRequest`

NewIntegrityViolationsRequest instantiates a new IntegrityViolationsRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIntegrityViolationsRequestWithDefaults

`func NewIntegrityViolationsRequestWithDefaults() *IntegrityViolationsRequest`

NewIntegrityViolationsRequestWithDefaults instantiates a new IntegrityViolationsRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetViolations

`func (o *IntegrityViolationsRequest) GetViolations() []IntegrityViolationRequest`

GetViolations returns the Violations field if non-nil, zero value otherwise.

### GetViolationsOk

`func (o *IntegrityViolationsRequest) GetViolationsOk() (*[]IntegrityViolationRequest, bool)`

GetViolationsOk returns a tuple with the Violations field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetViolations

`func (o *IntegrityViolationsRequest) SetViolations(v []IntegrityViolationRequest)`

SetViolations sets Violations field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


