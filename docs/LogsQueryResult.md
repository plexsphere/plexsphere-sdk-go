# LogsQueryResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StatusCode** | **int32** | HTTP status the logs backend returned. | 
**Body** | **string** | The logs backend&#39;s verbatim response body, carried as an opaque JSON string so the platform does not re-shape the backend&#39;s stream envelope.  | 

## Methods

### NewLogsQueryResult

`func NewLogsQueryResult(statusCode int32, body string, ) *LogsQueryResult`

NewLogsQueryResult instantiates a new LogsQueryResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLogsQueryResultWithDefaults

`func NewLogsQueryResultWithDefaults() *LogsQueryResult`

NewLogsQueryResultWithDefaults instantiates a new LogsQueryResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetStatusCode

`func (o *LogsQueryResult) GetStatusCode() int32`

GetStatusCode returns the StatusCode field if non-nil, zero value otherwise.

### GetStatusCodeOk

`func (o *LogsQueryResult) GetStatusCodeOk() (*int32, bool)`

GetStatusCodeOk returns a tuple with the StatusCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatusCode

`func (o *LogsQueryResult) SetStatusCode(v int32)`

SetStatusCode sets StatusCode field to given value.


### GetBody

`func (o *LogsQueryResult) GetBody() string`

GetBody returns the Body field if non-nil, zero value otherwise.

### GetBodyOk

`func (o *LogsQueryResult) GetBodyOk() (*string, bool)`

GetBodyOk returns a tuple with the Body field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBody

`func (o *LogsQueryResult) SetBody(v string)`

SetBody sets Body field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


