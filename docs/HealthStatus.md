# HealthStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Status** | [**HealthStatusStatus**](HealthStatusStatus.md) |  | 
**Checks** | [**[]HealthCheck**](HealthCheck.md) | Per-dependency health checks. | 

## Methods

### NewHealthStatus

`func NewHealthStatus(status HealthStatusStatus, checks []HealthCheck, ) *HealthStatus`

NewHealthStatus instantiates a new HealthStatus object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewHealthStatusWithDefaults

`func NewHealthStatusWithDefaults() *HealthStatus`

NewHealthStatusWithDefaults instantiates a new HealthStatus object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetStatus

`func (o *HealthStatus) GetStatus() HealthStatusStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *HealthStatus) GetStatusOk() (*HealthStatusStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *HealthStatus) SetStatus(v HealthStatusStatus)`

SetStatus sets Status field to given value.


### GetChecks

`func (o *HealthStatus) GetChecks() []HealthCheck`

GetChecks returns the Checks field if non-nil, zero value otherwise.

### GetChecksOk

`func (o *HealthStatus) GetChecksOk() (*[]HealthCheck, bool)`

GetChecksOk returns a tuple with the Checks field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChecks

`func (o *HealthStatus) SetChecks(v []HealthCheck)`

SetChecks sets Checks field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


