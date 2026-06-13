# DomainCapacityDimensionReading

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Dimension** | [**CapacityDimension**](CapacityDimension.md) |  | 
**Unit** | [**CapacityUnit**](CapacityUnit.md) |  | 
**Used** | **float32** | Latest sampled usage for the dimension, in the dimension&#39;s &#x60;unit&#x60; (an absolute tally for &#x60;count&#x60;, a sustained rate for the &#x60;_per_second&#x60; units).  | 
**Target** | **float32** | The per-Domain target for the dimension, in the dimension&#39;s &#x60;unit&#x60;. A target of &#x60;0&#x60; means no target is configured.  | 
**Ratio** | **float32** | &#x60;used / target&#x60;, the fraction of the target currently consumed. &#x60;0&#x60; when no target is configured. A value at or above &#x60;0.8&#x60; is the threshold the collector records a crossing for.  | 

## Methods

### NewDomainCapacityDimensionReading

`func NewDomainCapacityDimensionReading(dimension CapacityDimension, unit CapacityUnit, used float32, target float32, ratio float32, ) *DomainCapacityDimensionReading`

NewDomainCapacityDimensionReading instantiates a new DomainCapacityDimensionReading object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDomainCapacityDimensionReadingWithDefaults

`func NewDomainCapacityDimensionReadingWithDefaults() *DomainCapacityDimensionReading`

NewDomainCapacityDimensionReadingWithDefaults instantiates a new DomainCapacityDimensionReading object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDimension

`func (o *DomainCapacityDimensionReading) GetDimension() CapacityDimension`

GetDimension returns the Dimension field if non-nil, zero value otherwise.

### GetDimensionOk

`func (o *DomainCapacityDimensionReading) GetDimensionOk() (*CapacityDimension, bool)`

GetDimensionOk returns a tuple with the Dimension field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDimension

`func (o *DomainCapacityDimensionReading) SetDimension(v CapacityDimension)`

SetDimension sets Dimension field to given value.


### GetUnit

`func (o *DomainCapacityDimensionReading) GetUnit() CapacityUnit`

GetUnit returns the Unit field if non-nil, zero value otherwise.

### GetUnitOk

`func (o *DomainCapacityDimensionReading) GetUnitOk() (*CapacityUnit, bool)`

GetUnitOk returns a tuple with the Unit field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUnit

`func (o *DomainCapacityDimensionReading) SetUnit(v CapacityUnit)`

SetUnit sets Unit field to given value.


### GetUsed

`func (o *DomainCapacityDimensionReading) GetUsed() float32`

GetUsed returns the Used field if non-nil, zero value otherwise.

### GetUsedOk

`func (o *DomainCapacityDimensionReading) GetUsedOk() (*float32, bool)`

GetUsedOk returns a tuple with the Used field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUsed

`func (o *DomainCapacityDimensionReading) SetUsed(v float32)`

SetUsed sets Used field to given value.


### GetTarget

`func (o *DomainCapacityDimensionReading) GetTarget() float32`

GetTarget returns the Target field if non-nil, zero value otherwise.

### GetTargetOk

`func (o *DomainCapacityDimensionReading) GetTargetOk() (*float32, bool)`

GetTargetOk returns a tuple with the Target field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTarget

`func (o *DomainCapacityDimensionReading) SetTarget(v float32)`

SetTarget sets Target field to given value.


### GetRatio

`func (o *DomainCapacityDimensionReading) GetRatio() float32`

GetRatio returns the Ratio field if non-nil, zero value otherwise.

### GetRatioOk

`func (o *DomainCapacityDimensionReading) GetRatioOk() (*float32, bool)`

GetRatioOk returns a tuple with the Ratio field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRatio

`func (o *DomainCapacityDimensionReading) SetRatio(v float32)`

SetRatio sets Ratio field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


