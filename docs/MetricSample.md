# MetricSample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Group** | [**MetricSampleGroup**](MetricSampleGroup.md) |  | 
**Name** | **string** | The metric name within its group (e.g. &#x60;cpu_seconds_total&#x60;). Required and non-empty.  | 
**Value** | **float32** | The numeric sample value. Required.  | 
**Labels** | Pointer to **map[string]string** | Optional dimension map carried with the sample. Keys and values are caller-supplied label dimensions; the platform adds the Domain, Project, and Node tags itself and never reads an identity subject or email from this map.  | [optional] 
**Timestamp** | **time.Time** | RFC 3339 timestamp at which the sample was observed on the Node. Required.  | 

## Methods

### NewMetricSample

`func NewMetricSample(group MetricSampleGroup, name string, value float32, timestamp time.Time, ) *MetricSample`

NewMetricSample instantiates a new MetricSample object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewMetricSampleWithDefaults

`func NewMetricSampleWithDefaults() *MetricSample`

NewMetricSampleWithDefaults instantiates a new MetricSample object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetGroup

`func (o *MetricSample) GetGroup() MetricSampleGroup`

GetGroup returns the Group field if non-nil, zero value otherwise.

### GetGroupOk

`func (o *MetricSample) GetGroupOk() (*MetricSampleGroup, bool)`

GetGroupOk returns a tuple with the Group field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroup

`func (o *MetricSample) SetGroup(v MetricSampleGroup)`

SetGroup sets Group field to given value.


### GetName

`func (o *MetricSample) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *MetricSample) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *MetricSample) SetName(v string)`

SetName sets Name field to given value.


### GetValue

`func (o *MetricSample) GetValue() float32`

GetValue returns the Value field if non-nil, zero value otherwise.

### GetValueOk

`func (o *MetricSample) GetValueOk() (*float32, bool)`

GetValueOk returns a tuple with the Value field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValue

`func (o *MetricSample) SetValue(v float32)`

SetValue sets Value field to given value.


### GetLabels

`func (o *MetricSample) GetLabels() map[string]string`

GetLabels returns the Labels field if non-nil, zero value otherwise.

### GetLabelsOk

`func (o *MetricSample) GetLabelsOk() (*map[string]string, bool)`

GetLabelsOk returns a tuple with the Labels field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLabels

`func (o *MetricSample) SetLabels(v map[string]string)`

SetLabels sets Labels field to given value.

### HasLabels

`func (o *MetricSample) HasLabels() bool`

HasLabels returns a boolean if a field has been set.

### GetTimestamp

`func (o *MetricSample) GetTimestamp() time.Time`

GetTimestamp returns the Timestamp field if non-nil, zero value otherwise.

### GetTimestampOk

`func (o *MetricSample) GetTimestampOk() (*time.Time, bool)`

GetTimestampOk returns a tuple with the Timestamp field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTimestamp

`func (o *MetricSample) SetTimestamp(v time.Time)`

SetTimestamp sets Timestamp field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


