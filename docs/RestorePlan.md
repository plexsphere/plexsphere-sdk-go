# RestorePlan

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Sequence** | [**[]RestoreStep**](RestoreStep.md) | The ordered restore steps, contiguous ascending by &#x60;order&#x60; starting at 1.  | 

## Methods

### NewRestorePlan

`func NewRestorePlan(sequence []RestoreStep, ) *RestorePlan`

NewRestorePlan instantiates a new RestorePlan object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRestorePlanWithDefaults

`func NewRestorePlanWithDefaults() *RestorePlan`

NewRestorePlanWithDefaults instantiates a new RestorePlan object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSequence

`func (o *RestorePlan) GetSequence() []RestoreStep`

GetSequence returns the Sequence field if non-nil, zero value otherwise.

### GetSequenceOk

`func (o *RestorePlan) GetSequenceOk() (*[]RestoreStep, bool)`

GetSequenceOk returns a tuple with the Sequence field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSequence

`func (o *RestorePlan) SetSequence(v []RestoreStep)`

SetSequence sets Sequence field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


