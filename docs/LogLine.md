# LogLine

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Severity** | [**LogLineSeverity**](LogLineSeverity.md) |  | 
**Unit** | Pointer to **string** | Optional originating unit (the systemd unit or file-glob source) the line was collected from.  | [optional] 
**Hostname** | Pointer to **string** | Optional hostname the line was emitted on.  | [optional] 
**Message** | **string** | The log message body. Required and non-empty. PII that a line inadvertently carries is the customer&#39;s ingest-side responsibility; an optional per-Domain redaction filter can be enabled at ingest.  | 
**Timestamp** | **time.Time** | RFC 3339 timestamp at which the line was emitted. Required.  | 

## Methods

### NewLogLine

`func NewLogLine(severity LogLineSeverity, message string, timestamp time.Time, ) *LogLine`

NewLogLine instantiates a new LogLine object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLogLineWithDefaults

`func NewLogLineWithDefaults() *LogLine`

NewLogLineWithDefaults instantiates a new LogLine object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSeverity

`func (o *LogLine) GetSeverity() LogLineSeverity`

GetSeverity returns the Severity field if non-nil, zero value otherwise.

### GetSeverityOk

`func (o *LogLine) GetSeverityOk() (*LogLineSeverity, bool)`

GetSeverityOk returns a tuple with the Severity field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSeverity

`func (o *LogLine) SetSeverity(v LogLineSeverity)`

SetSeverity sets Severity field to given value.


### GetUnit

`func (o *LogLine) GetUnit() string`

GetUnit returns the Unit field if non-nil, zero value otherwise.

### GetUnitOk

`func (o *LogLine) GetUnitOk() (*string, bool)`

GetUnitOk returns a tuple with the Unit field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUnit

`func (o *LogLine) SetUnit(v string)`

SetUnit sets Unit field to given value.

### HasUnit

`func (o *LogLine) HasUnit() bool`

HasUnit returns a boolean if a field has been set.

### GetHostname

`func (o *LogLine) GetHostname() string`

GetHostname returns the Hostname field if non-nil, zero value otherwise.

### GetHostnameOk

`func (o *LogLine) GetHostnameOk() (*string, bool)`

GetHostnameOk returns a tuple with the Hostname field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHostname

`func (o *LogLine) SetHostname(v string)`

SetHostname sets Hostname field to given value.

### HasHostname

`func (o *LogLine) HasHostname() bool`

HasHostname returns a boolean if a field has been set.

### GetMessage

`func (o *LogLine) GetMessage() string`

GetMessage returns the Message field if non-nil, zero value otherwise.

### GetMessageOk

`func (o *LogLine) GetMessageOk() (*string, bool)`

GetMessageOk returns a tuple with the Message field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessage

`func (o *LogLine) SetMessage(v string)`

SetMessage sets Message field to given value.


### GetTimestamp

`func (o *LogLine) GetTimestamp() time.Time`

GetTimestamp returns the Timestamp field if non-nil, zero value otherwise.

### GetTimestampOk

`func (o *LogLine) GetTimestampOk() (*time.Time, bool)`

GetTimestampOk returns a tuple with the Timestamp field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTimestamp

`func (o *LogLine) SetTimestamp(v time.Time)`

SetTimestamp sets Timestamp field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


