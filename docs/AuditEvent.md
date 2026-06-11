# AuditEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Source** | [**AuditEventSource**](AuditEventSource.md) |  | 
**Action** | **string** | The audited action (e.g. the syscall name or Kubernetes verb). Required and non-empty.  | 
**Outcome** | **string** | The outcome of the audited action (e.g. &#x60;success&#x60; / &#x60;failure&#x60;). Required and non-empty.  | 
**Timestamp** | **time.Time** | RFC 3339 timestamp at which the event occurred. Required.  | 

## Methods

### NewAuditEvent

`func NewAuditEvent(source AuditEventSource, action string, outcome string, timestamp time.Time, ) *AuditEvent`

NewAuditEvent instantiates a new AuditEvent object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditEventWithDefaults

`func NewAuditEventWithDefaults() *AuditEvent`

NewAuditEventWithDefaults instantiates a new AuditEvent object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSource

`func (o *AuditEvent) GetSource() AuditEventSource`

GetSource returns the Source field if non-nil, zero value otherwise.

### GetSourceOk

`func (o *AuditEvent) GetSourceOk() (*AuditEventSource, bool)`

GetSourceOk returns a tuple with the Source field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSource

`func (o *AuditEvent) SetSource(v AuditEventSource)`

SetSource sets Source field to given value.


### GetAction

`func (o *AuditEvent) GetAction() string`

GetAction returns the Action field if non-nil, zero value otherwise.

### GetActionOk

`func (o *AuditEvent) GetActionOk() (*string, bool)`

GetActionOk returns a tuple with the Action field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAction

`func (o *AuditEvent) SetAction(v string)`

SetAction sets Action field to given value.


### GetOutcome

`func (o *AuditEvent) GetOutcome() string`

GetOutcome returns the Outcome field if non-nil, zero value otherwise.

### GetOutcomeOk

`func (o *AuditEvent) GetOutcomeOk() (*string, bool)`

GetOutcomeOk returns a tuple with the Outcome field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOutcome

`func (o *AuditEvent) SetOutcome(v string)`

SetOutcome sets Outcome field to given value.


### GetTimestamp

`func (o *AuditEvent) GetTimestamp() time.Time`

GetTimestamp returns the Timestamp field if non-nil, zero value otherwise.

### GetTimestampOk

`func (o *AuditEvent) GetTimestampOk() (*time.Time, bool)`

GetTimestampOk returns a tuple with the Timestamp field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTimestamp

`func (o *AuditEvent) SetTimestamp(v time.Time)`

SetTimestamp sets Timestamp field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


