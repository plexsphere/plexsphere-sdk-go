# TrackingPolicy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Mode** | [**TrackingPolicyMode**](TrackingPolicyMode.md) |  | 
**IntervalSeconds** | Pointer to **int32** | Re-resolution interval in seconds. Required and positive for &#x60;track-tag&#x60;; absent for &#x60;pinned&#x60;.  | [optional] 

## Methods

### NewTrackingPolicy

`func NewTrackingPolicy(mode TrackingPolicyMode, ) *TrackingPolicy`

NewTrackingPolicy instantiates a new TrackingPolicy object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewTrackingPolicyWithDefaults

`func NewTrackingPolicyWithDefaults() *TrackingPolicy`

NewTrackingPolicyWithDefaults instantiates a new TrackingPolicy object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMode

`func (o *TrackingPolicy) GetMode() TrackingPolicyMode`

GetMode returns the Mode field if non-nil, zero value otherwise.

### GetModeOk

`func (o *TrackingPolicy) GetModeOk() (*TrackingPolicyMode, bool)`

GetModeOk returns a tuple with the Mode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMode

`func (o *TrackingPolicy) SetMode(v TrackingPolicyMode)`

SetMode sets Mode field to given value.


### GetIntervalSeconds

`func (o *TrackingPolicy) GetIntervalSeconds() int32`

GetIntervalSeconds returns the IntervalSeconds field if non-nil, zero value otherwise.

### GetIntervalSecondsOk

`func (o *TrackingPolicy) GetIntervalSecondsOk() (*int32, bool)`

GetIntervalSecondsOk returns a tuple with the IntervalSeconds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIntervalSeconds

`func (o *TrackingPolicy) SetIntervalSeconds(v int32)`

SetIntervalSeconds sets IntervalSeconds field to given value.

### HasIntervalSeconds

`func (o *TrackingPolicy) HasIntervalSeconds() bool`

HasIntervalSeconds returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


