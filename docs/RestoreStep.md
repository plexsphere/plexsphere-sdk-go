# RestoreStep

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Order** | **int32** | The step&#39;s position in the restore sequence; steps are contiguous ascending starting at 1.  | 
**Name** | **string** | The store or component the step restores. | 
**Action** | **string** | The action the operator takes for the step. | 
**Verify** | **string** | How the operator verifies the step succeeded. | 

## Methods

### NewRestoreStep

`func NewRestoreStep(order int32, name string, action string, verify string, ) *RestoreStep`

NewRestoreStep instantiates a new RestoreStep object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRestoreStepWithDefaults

`func NewRestoreStepWithDefaults() *RestoreStep`

NewRestoreStepWithDefaults instantiates a new RestoreStep object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetOrder

`func (o *RestoreStep) GetOrder() int32`

GetOrder returns the Order field if non-nil, zero value otherwise.

### GetOrderOk

`func (o *RestoreStep) GetOrderOk() (*int32, bool)`

GetOrderOk returns a tuple with the Order field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrder

`func (o *RestoreStep) SetOrder(v int32)`

SetOrder sets Order field to given value.


### GetName

`func (o *RestoreStep) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *RestoreStep) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *RestoreStep) SetName(v string)`

SetName sets Name field to given value.


### GetAction

`func (o *RestoreStep) GetAction() string`

GetAction returns the Action field if non-nil, zero value otherwise.

### GetActionOk

`func (o *RestoreStep) GetActionOk() (*string, bool)`

GetActionOk returns a tuple with the Action field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAction

`func (o *RestoreStep) SetAction(v string)`

SetAction sets Action field to given value.


### GetVerify

`func (o *RestoreStep) GetVerify() string`

GetVerify returns the Verify field if non-nil, zero value otherwise.

### GetVerifyOk

`func (o *RestoreStep) GetVerifyOk() (*string, bool)`

GetVerifyOk returns a tuple with the Verify field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVerify

`func (o *RestoreStep) SetVerify(v string)`

SetVerify sets Verify field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


