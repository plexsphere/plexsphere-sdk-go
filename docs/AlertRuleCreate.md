# AlertRuleCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Domain-unique logical name. A duplicate name in the Domain is rejected with 409.  | 
**Signal** | **string** | The metric or log series expression the rule records as its watched signal.  | 
**Comparator** | [**AlertComparator**](AlertComparator.md) |  | 
**Threshold** | **float64** | Finite value the signal is recorded against. NaN and infinity are rejected.  | 
**Severity** | [**AlertSeverity**](AlertSeverity.md) |  | 
**Enabled** | Pointer to **bool** | Whether the rule is recorded as enabled. Defaults to enabled. The flag is stored configuration only and does not cause evaluation.  | [optional] [default to true]

## Methods

### NewAlertRuleCreate

`func NewAlertRuleCreate(name string, signal string, comparator AlertComparator, threshold float64, severity AlertSeverity, ) *AlertRuleCreate`

NewAlertRuleCreate instantiates a new AlertRuleCreate object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAlertRuleCreateWithDefaults

`func NewAlertRuleCreateWithDefaults() *AlertRuleCreate`

NewAlertRuleCreateWithDefaults instantiates a new AlertRuleCreate object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *AlertRuleCreate) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *AlertRuleCreate) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *AlertRuleCreate) SetName(v string)`

SetName sets Name field to given value.


### GetSignal

`func (o *AlertRuleCreate) GetSignal() string`

GetSignal returns the Signal field if non-nil, zero value otherwise.

### GetSignalOk

`func (o *AlertRuleCreate) GetSignalOk() (*string, bool)`

GetSignalOk returns a tuple with the Signal field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSignal

`func (o *AlertRuleCreate) SetSignal(v string)`

SetSignal sets Signal field to given value.


### GetComparator

`func (o *AlertRuleCreate) GetComparator() AlertComparator`

GetComparator returns the Comparator field if non-nil, zero value otherwise.

### GetComparatorOk

`func (o *AlertRuleCreate) GetComparatorOk() (*AlertComparator, bool)`

GetComparatorOk returns a tuple with the Comparator field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetComparator

`func (o *AlertRuleCreate) SetComparator(v AlertComparator)`

SetComparator sets Comparator field to given value.


### GetThreshold

`func (o *AlertRuleCreate) GetThreshold() float64`

GetThreshold returns the Threshold field if non-nil, zero value otherwise.

### GetThresholdOk

`func (o *AlertRuleCreate) GetThresholdOk() (*float64, bool)`

GetThresholdOk returns a tuple with the Threshold field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetThreshold

`func (o *AlertRuleCreate) SetThreshold(v float64)`

SetThreshold sets Threshold field to given value.


### GetSeverity

`func (o *AlertRuleCreate) GetSeverity() AlertSeverity`

GetSeverity returns the Severity field if non-nil, zero value otherwise.

### GetSeverityOk

`func (o *AlertRuleCreate) GetSeverityOk() (*AlertSeverity, bool)`

GetSeverityOk returns a tuple with the Severity field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSeverity

`func (o *AlertRuleCreate) SetSeverity(v AlertSeverity)`

SetSeverity sets Severity field to given value.


### GetEnabled

`func (o *AlertRuleCreate) GetEnabled() bool`

GetEnabled returns the Enabled field if non-nil, zero value otherwise.

### GetEnabledOk

`func (o *AlertRuleCreate) GetEnabledOk() (*bool, bool)`

GetEnabledOk returns a tuple with the Enabled field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnabled

`func (o *AlertRuleCreate) SetEnabled(v bool)`

SetEnabled sets Enabled field to given value.

### HasEnabled

`func (o *AlertRuleCreate) HasEnabled() bool`

HasEnabled returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


