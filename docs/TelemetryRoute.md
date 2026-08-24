# TelemetryRoute

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable identifier of the route (UUIDv7). | 
**ProjectId** | **string** | Project the route belongs to. Immutable once the route exists.  | 
**Signal** | [**TelemetrySignal**](TelemetrySignal.md) |  | 
**SeverityFloor** | Pointer to [**TelemetrySeverity**](TelemetrySeverity.md) | Least severe log keyword the route carries. Absent means the route states no floor and carries every record on its signal. Present on a &#x60;logs&#x60; route only.  | [optional] 
**NamePrefix** | Pointer to **string** | Leading characters of the metric names the route selects. Absent means the route states no prefix. Present on a &#x60;metrics&#x60; route only.  | [optional] 
**SinkIds** | **[]string** | Sinks the route delivers to. At least one and at most sixteen, no zero id, and no sink named twice.  | 
**CreatedAt** | **time.Time** | RFC 3339 timestamp the route was created. | 
**UpdatedAt** | **time.Time** | RFC 3339 timestamp the route was last changed. | 

## Methods

### NewTelemetryRoute

`func NewTelemetryRoute(id string, projectId string, signal TelemetrySignal, sinkIds []string, createdAt time.Time, updatedAt time.Time, ) *TelemetryRoute`

NewTelemetryRoute instantiates a new TelemetryRoute object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewTelemetryRouteWithDefaults

`func NewTelemetryRouteWithDefaults() *TelemetryRoute`

NewTelemetryRouteWithDefaults instantiates a new TelemetryRoute object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *TelemetryRoute) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *TelemetryRoute) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *TelemetryRoute) SetId(v string)`

SetId sets Id field to given value.


### GetProjectId

`func (o *TelemetryRoute) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *TelemetryRoute) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *TelemetryRoute) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetSignal

`func (o *TelemetryRoute) GetSignal() TelemetrySignal`

GetSignal returns the Signal field if non-nil, zero value otherwise.

### GetSignalOk

`func (o *TelemetryRoute) GetSignalOk() (*TelemetrySignal, bool)`

GetSignalOk returns a tuple with the Signal field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSignal

`func (o *TelemetryRoute) SetSignal(v TelemetrySignal)`

SetSignal sets Signal field to given value.


### GetSeverityFloor

`func (o *TelemetryRoute) GetSeverityFloor() TelemetrySeverity`

GetSeverityFloor returns the SeverityFloor field if non-nil, zero value otherwise.

### GetSeverityFloorOk

`func (o *TelemetryRoute) GetSeverityFloorOk() (*TelemetrySeverity, bool)`

GetSeverityFloorOk returns a tuple with the SeverityFloor field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSeverityFloor

`func (o *TelemetryRoute) SetSeverityFloor(v TelemetrySeverity)`

SetSeverityFloor sets SeverityFloor field to given value.

### HasSeverityFloor

`func (o *TelemetryRoute) HasSeverityFloor() bool`

HasSeverityFloor returns a boolean if a field has been set.

### GetNamePrefix

`func (o *TelemetryRoute) GetNamePrefix() string`

GetNamePrefix returns the NamePrefix field if non-nil, zero value otherwise.

### GetNamePrefixOk

`func (o *TelemetryRoute) GetNamePrefixOk() (*string, bool)`

GetNamePrefixOk returns a tuple with the NamePrefix field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNamePrefix

`func (o *TelemetryRoute) SetNamePrefix(v string)`

SetNamePrefix sets NamePrefix field to given value.

### HasNamePrefix

`func (o *TelemetryRoute) HasNamePrefix() bool`

HasNamePrefix returns a boolean if a field has been set.

### GetSinkIds

`func (o *TelemetryRoute) GetSinkIds() []string`

GetSinkIds returns the SinkIds field if non-nil, zero value otherwise.

### GetSinkIdsOk

`func (o *TelemetryRoute) GetSinkIdsOk() (*[]string, bool)`

GetSinkIdsOk returns a tuple with the SinkIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSinkIds

`func (o *TelemetryRoute) SetSinkIds(v []string)`

SetSinkIds sets SinkIds field to given value.


### GetCreatedAt

`func (o *TelemetryRoute) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *TelemetryRoute) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *TelemetryRoute) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *TelemetryRoute) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *TelemetryRoute) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *TelemetryRoute) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


