# SinkSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Dataset** | Pointer to **string** | Logical stream an &#x60;otlp&#x60; destination files the delivered telemetry under. Stated on &#x60;otlp&#x60; sinks only.  | [optional] 

## Methods

### NewSinkSettings

`func NewSinkSettings() *SinkSettings`

NewSinkSettings instantiates a new SinkSettings object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSinkSettingsWithDefaults

`func NewSinkSettingsWithDefaults() *SinkSettings`

NewSinkSettingsWithDefaults instantiates a new SinkSettings object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDataset

`func (o *SinkSettings) GetDataset() string`

GetDataset returns the Dataset field if non-nil, zero value otherwise.

### GetDatasetOk

`func (o *SinkSettings) GetDatasetOk() (*string, bool)`

GetDatasetOk returns a tuple with the Dataset field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDataset

`func (o *SinkSettings) SetDataset(v string)`

SetDataset sets Dataset field to given value.

### HasDataset

`func (o *SinkSettings) HasDataset() bool`

HasDataset returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


