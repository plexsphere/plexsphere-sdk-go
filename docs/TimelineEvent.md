# TimelineEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable identifier of the timeline event (UUIDv7). | 
**IncidentId** | **string** | Incident the event belongs to. | 
**Kind** | [**TimelineEventKind**](TimelineEventKind.md) |  | 
**Message** | **string** | Free-form message recorded on the event. | 
**OccurredAt** | **time.Time** | RFC 3339 instant the event occurred. The timeline is ordered by this field ascending.  | 

## Methods

### NewTimelineEvent

`func NewTimelineEvent(id string, incidentId string, kind TimelineEventKind, message string, occurredAt time.Time, ) *TimelineEvent`

NewTimelineEvent instantiates a new TimelineEvent object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewTimelineEventWithDefaults

`func NewTimelineEventWithDefaults() *TimelineEvent`

NewTimelineEventWithDefaults instantiates a new TimelineEvent object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *TimelineEvent) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *TimelineEvent) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *TimelineEvent) SetId(v string)`

SetId sets Id field to given value.


### GetIncidentId

`func (o *TimelineEvent) GetIncidentId() string`

GetIncidentId returns the IncidentId field if non-nil, zero value otherwise.

### GetIncidentIdOk

`func (o *TimelineEvent) GetIncidentIdOk() (*string, bool)`

GetIncidentIdOk returns a tuple with the IncidentId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIncidentId

`func (o *TimelineEvent) SetIncidentId(v string)`

SetIncidentId sets IncidentId field to given value.


### GetKind

`func (o *TimelineEvent) GetKind() TimelineEventKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *TimelineEvent) GetKindOk() (*TimelineEventKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *TimelineEvent) SetKind(v TimelineEventKind)`

SetKind sets Kind field to given value.


### GetMessage

`func (o *TimelineEvent) GetMessage() string`

GetMessage returns the Message field if non-nil, zero value otherwise.

### GetMessageOk

`func (o *TimelineEvent) GetMessageOk() (*string, bool)`

GetMessageOk returns a tuple with the Message field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessage

`func (o *TimelineEvent) SetMessage(v string)`

SetMessage sets Message field to given value.


### GetOccurredAt

`func (o *TimelineEvent) GetOccurredAt() time.Time`

GetOccurredAt returns the OccurredAt field if non-nil, zero value otherwise.

### GetOccurredAtOk

`func (o *TimelineEvent) GetOccurredAtOk() (*time.Time, bool)`

GetOccurredAtOk returns a tuple with the OccurredAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOccurredAt

`func (o *TimelineEvent) SetOccurredAt(v time.Time)`

SetOccurredAt sets OccurredAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


