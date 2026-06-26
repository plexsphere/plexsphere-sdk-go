# AlertRuleUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | Pointer to **string** | New Domain-unique logical name. A rename onto an existing name in the Domain is rejected with 409.  | [optional] 
**Signal** | Pointer to **string** | New watched signal expression. | [optional] 
**Comparator** | Pointer to [**AlertComparator**](AlertComparator.md) |  | [optional] 
**Threshold** | Pointer to **float64** | New finite threshold value. | [optional] 
**Severity** | Pointer to [**AlertSeverity**](AlertSeverity.md) |  | [optional] 
**Enabled** | Pointer to **bool** | New enabled flag. Stored configuration only; does not cause evaluation.  | [optional] 

## Methods

### NewAlertRuleUpdate

`func NewAlertRuleUpdate() *AlertRuleUpdate`

NewAlertRuleUpdate instantiates a new AlertRuleUpdate object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAlertRuleUpdateWithDefaults

`func NewAlertRuleUpdateWithDefaults() *AlertRuleUpdate`

NewAlertRuleUpdateWithDefaults instantiates a new AlertRuleUpdate object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *AlertRuleUpdate) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *AlertRuleUpdate) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *AlertRuleUpdate) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *AlertRuleUpdate) HasName() bool`

HasName returns a boolean if a field has been set.

### GetSignal

`func (o *AlertRuleUpdate) GetSignal() string`

GetSignal returns the Signal field if non-nil, zero value otherwise.

### GetSignalOk

`func (o *AlertRuleUpdate) GetSignalOk() (*string, bool)`

GetSignalOk returns a tuple with the Signal field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSignal

`func (o *AlertRuleUpdate) SetSignal(v string)`

SetSignal sets Signal field to given value.

### HasSignal

`func (o *AlertRuleUpdate) HasSignal() bool`

HasSignal returns a boolean if a field has been set.

### GetComparator

`func (o *AlertRuleUpdate) GetComparator() AlertComparator`

GetComparator returns the Comparator field if non-nil, zero value otherwise.

### GetComparatorOk

`func (o *AlertRuleUpdate) GetComparatorOk() (*AlertComparator, bool)`

GetComparatorOk returns a tuple with the Comparator field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetComparator

`func (o *AlertRuleUpdate) SetComparator(v AlertComparator)`

SetComparator sets Comparator field to given value.

### HasComparator

`func (o *AlertRuleUpdate) HasComparator() bool`

HasComparator returns a boolean if a field has been set.

### GetThreshold

`func (o *AlertRuleUpdate) GetThreshold() float64`

GetThreshold returns the Threshold field if non-nil, zero value otherwise.

### GetThresholdOk

`func (o *AlertRuleUpdate) GetThresholdOk() (*float64, bool)`

GetThresholdOk returns a tuple with the Threshold field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetThreshold

`func (o *AlertRuleUpdate) SetThreshold(v float64)`

SetThreshold sets Threshold field to given value.

### HasThreshold

`func (o *AlertRuleUpdate) HasThreshold() bool`

HasThreshold returns a boolean if a field has been set.

### GetSeverity

`func (o *AlertRuleUpdate) GetSeverity() AlertSeverity`

GetSeverity returns the Severity field if non-nil, zero value otherwise.

### GetSeverityOk

`func (o *AlertRuleUpdate) GetSeverityOk() (*AlertSeverity, bool)`

GetSeverityOk returns a tuple with the Severity field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSeverity

`func (o *AlertRuleUpdate) SetSeverity(v AlertSeverity)`

SetSeverity sets Severity field to given value.

### HasSeverity

`func (o *AlertRuleUpdate) HasSeverity() bool`

HasSeverity returns a boolean if a field has been set.

### GetEnabled

`func (o *AlertRuleUpdate) GetEnabled() bool`

GetEnabled returns the Enabled field if non-nil, zero value otherwise.

### GetEnabledOk

`func (o *AlertRuleUpdate) GetEnabledOk() (*bool, bool)`

GetEnabledOk returns a tuple with the Enabled field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnabled

`func (o *AlertRuleUpdate) SetEnabled(v bool)`

SetEnabled sets Enabled field to given value.

### HasEnabled

`func (o *AlertRuleUpdate) HasEnabled() bool`

HasEnabled returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


