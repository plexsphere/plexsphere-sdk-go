# TelemetryRouteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Signal** | [**TelemetrySignal**](TelemetrySignal.md) |  | 
**SeverityFloor** | Pointer to [**TelemetrySeverity**](TelemetrySeverity.md) | Least severe log keyword to carry. Stated on a &#x60;logs&#x60; route only; stating it on another signal is refused with &#x60;422 telemetry_route_invalid&#x60; rather than carried along and ignored at delivery.  | [optional] 
**NamePrefix** | Pointer to **string** | Leading characters of the metric names to select. Stated on a &#x60;metrics&#x60; route only; stating it on another signal is refused with &#x60;422 telemetry_route_invalid&#x60;.  | [optional] 
**SinkIds** | **[]string** | Sinks to deliver to. At least one and at most sixteen, no zero id, and no sink named twice. The ceiling bounds the delivery fan-out a single batch pays for, which the per-Project route limit alone does not. Each target is checked at authoring time, so a route that would deliver nowhere is refused where it is written.  | 

## Methods

### NewTelemetryRouteRequest

`func NewTelemetryRouteRequest(signal TelemetrySignal, sinkIds []string, ) *TelemetryRouteRequest`

NewTelemetryRouteRequest instantiates a new TelemetryRouteRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewTelemetryRouteRequestWithDefaults

`func NewTelemetryRouteRequestWithDefaults() *TelemetryRouteRequest`

NewTelemetryRouteRequestWithDefaults instantiates a new TelemetryRouteRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSignal

`func (o *TelemetryRouteRequest) GetSignal() TelemetrySignal`

GetSignal returns the Signal field if non-nil, zero value otherwise.

### GetSignalOk

`func (o *TelemetryRouteRequest) GetSignalOk() (*TelemetrySignal, bool)`

GetSignalOk returns a tuple with the Signal field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSignal

`func (o *TelemetryRouteRequest) SetSignal(v TelemetrySignal)`

SetSignal sets Signal field to given value.


### GetSeverityFloor

`func (o *TelemetryRouteRequest) GetSeverityFloor() TelemetrySeverity`

GetSeverityFloor returns the SeverityFloor field if non-nil, zero value otherwise.

### GetSeverityFloorOk

`func (o *TelemetryRouteRequest) GetSeverityFloorOk() (*TelemetrySeverity, bool)`

GetSeverityFloorOk returns a tuple with the SeverityFloor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSeverityFloor

`func (o *TelemetryRouteRequest) SetSeverityFloor(v TelemetrySeverity)`

SetSeverityFloor sets SeverityFloor field to given value.

### HasSeverityFloor

`func (o *TelemetryRouteRequest) HasSeverityFloor() bool`

HasSeverityFloor returns a boolean if a field has been set.

### GetNamePrefix

`func (o *TelemetryRouteRequest) GetNamePrefix() string`

GetNamePrefix returns the NamePrefix field if non-nil, zero value otherwise.

### GetNamePrefixOk

`func (o *TelemetryRouteRequest) GetNamePrefixOk() (*string, bool)`

GetNamePrefixOk returns a tuple with the NamePrefix field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNamePrefix

`func (o *TelemetryRouteRequest) SetNamePrefix(v string)`

SetNamePrefix sets NamePrefix field to given value.

### HasNamePrefix

`func (o *TelemetryRouteRequest) HasNamePrefix() bool`

HasNamePrefix returns a boolean if a field has been set.

### GetSinkIds

`func (o *TelemetryRouteRequest) GetSinkIds() []string`

GetSinkIds returns the SinkIds field if non-nil, zero value otherwise.

### GetSinkIdsOk

`func (o *TelemetryRouteRequest) GetSinkIdsOk() (*[]string, bool)`

GetSinkIdsOk returns a tuple with the SinkIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSinkIds

`func (o *TelemetryRouteRequest) SetSinkIds(v []string)`

SetSinkIds sets SinkIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


