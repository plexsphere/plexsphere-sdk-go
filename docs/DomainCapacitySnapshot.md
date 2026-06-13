# DomainCapacitySnapshot

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SampledAt** | **time.Time** | RFC 3339 timestamp at which the collector last sampled the Domain&#39;s usage. The snapshot is unavailable (&#x60;503&#x60;) until the first sample completes.  | 
**Dimensions** | [**[]DomainCapacityDimensionReading**](DomainCapacityDimensionReading.md) | One reading per catalogued capacity dimension, in the canonical order used by the Dashboard capacity view.  | 

## Methods

### NewDomainCapacitySnapshot

`func NewDomainCapacitySnapshot(sampledAt time.Time, dimensions []DomainCapacityDimensionReading, ) *DomainCapacitySnapshot`

NewDomainCapacitySnapshot instantiates a new DomainCapacitySnapshot object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDomainCapacitySnapshotWithDefaults

`func NewDomainCapacitySnapshotWithDefaults() *DomainCapacitySnapshot`

NewDomainCapacitySnapshotWithDefaults instantiates a new DomainCapacitySnapshot object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSampledAt

`func (o *DomainCapacitySnapshot) GetSampledAt() time.Time`

GetSampledAt returns the SampledAt field if non-nil, zero value otherwise.

### GetSampledAtOk

`func (o *DomainCapacitySnapshot) GetSampledAtOk() (*time.Time, bool)`

GetSampledAtOk returns a tuple with the SampledAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSampledAt

`func (o *DomainCapacitySnapshot) SetSampledAt(v time.Time)`

SetSampledAt sets SampledAt field to given value.


### GetDimensions

`func (o *DomainCapacitySnapshot) GetDimensions() []DomainCapacityDimensionReading`

GetDimensions returns the Dimensions field if non-nil, zero value otherwise.

### GetDimensionsOk

`func (o *DomainCapacitySnapshot) GetDimensionsOk() (*[]DomainCapacityDimensionReading, bool)`

GetDimensionsOk returns a tuple with the Dimensions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDimensions

`func (o *DomainCapacitySnapshot) SetDimensions(v []DomainCapacityDimensionReading)`

SetDimensions sets Dimensions field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


