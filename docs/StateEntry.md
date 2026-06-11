# StateEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Key** | **string** | The entry&#39;s stable identity within its bucket. | 
**Value** | **string** | The entry&#39;s reported value, carried opaquely. | 
**WorkloadTag** | Pointer to **string** | Tag of the workload that produced the entry. Absent or empty when the entry is not attributed to a workload.  | [optional] 

## Methods

### NewStateEntry

`func NewStateEntry(key string, value string, ) *StateEntry`

NewStateEntry instantiates a new StateEntry object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewStateEntryWithDefaults

`func NewStateEntryWithDefaults() *StateEntry`

NewStateEntryWithDefaults instantiates a new StateEntry object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKey

`func (o *StateEntry) GetKey() string`

GetKey returns the Key field if non-nil, zero value otherwise.

### GetKeyOk

`func (o *StateEntry) GetKeyOk() (*string, bool)`

GetKeyOk returns a tuple with the Key field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKey

`func (o *StateEntry) SetKey(v string)`

SetKey sets Key field to given value.


### GetValue

`func (o *StateEntry) GetValue() string`

GetValue returns the Value field if non-nil, zero value otherwise.

### GetValueOk

`func (o *StateEntry) GetValueOk() (*string, bool)`

GetValueOk returns a tuple with the Value field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValue

`func (o *StateEntry) SetValue(v string)`

SetValue sets Value field to given value.


### GetWorkloadTag

`func (o *StateEntry) GetWorkloadTag() string`

GetWorkloadTag returns the WorkloadTag field if non-nil, zero value otherwise.

### GetWorkloadTagOk

`func (o *StateEntry) GetWorkloadTagOk() (*string, bool)`

GetWorkloadTagOk returns a tuple with the WorkloadTag field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetWorkloadTag

`func (o *StateEntry) SetWorkloadTag(v string)`

SetWorkloadTag sets WorkloadTag field to given value.

### HasWorkloadTag

`func (o *StateEntry) HasWorkloadTag() bool`

HasWorkloadTag returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


