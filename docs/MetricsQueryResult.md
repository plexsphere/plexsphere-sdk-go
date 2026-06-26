# MetricsQueryResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StatusCode** | **int32** | HTTP status the metrics backend returned. | 
**Body** | **string** | The metrics backend&#39;s verbatim response body, carried as an opaque JSON string so the platform does not re-shape the backend&#39;s series envelope.  | 

## Methods

### NewMetricsQueryResult

`func NewMetricsQueryResult(statusCode int32, body string, ) *MetricsQueryResult`

NewMetricsQueryResult instantiates a new MetricsQueryResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewMetricsQueryResultWithDefaults

`func NewMetricsQueryResultWithDefaults() *MetricsQueryResult`

NewMetricsQueryResultWithDefaults instantiates a new MetricsQueryResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetStatusCode

`func (o *MetricsQueryResult) GetStatusCode() int32`

GetStatusCode returns the StatusCode field if non-nil, zero value otherwise.

### GetStatusCodeOk

`func (o *MetricsQueryResult) GetStatusCodeOk() (*int32, bool)`

GetStatusCodeOk returns a tuple with the StatusCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatusCode

`func (o *MetricsQueryResult) SetStatusCode(v int32)`

SetStatusCode sets StatusCode field to given value.


### GetBody

`func (o *MetricsQueryResult) GetBody() string`

GetBody returns the Body field if non-nil, zero value otherwise.

### GetBodyOk

`func (o *MetricsQueryResult) GetBodyOk() (*string, bool)`

GetBodyOk returns a tuple with the Body field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBody

`func (o *MetricsQueryResult) SetBody(v string)`

SetBody sets Body field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


