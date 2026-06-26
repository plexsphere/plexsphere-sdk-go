# TimelineEventAppend

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | [**TimelineEventKind**](TimelineEventKind.md) |  | 
**Message** | **string** | Free-form message to record on the event. | 

## Methods

### NewTimelineEventAppend

`func NewTimelineEventAppend(kind TimelineEventKind, message string, ) *TimelineEventAppend`

NewTimelineEventAppend instantiates a new TimelineEventAppend object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewTimelineEventAppendWithDefaults

`func NewTimelineEventAppendWithDefaults() *TimelineEventAppend`

NewTimelineEventAppendWithDefaults instantiates a new TimelineEventAppend object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKind

`func (o *TimelineEventAppend) GetKind() TimelineEventKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *TimelineEventAppend) GetKindOk() (*TimelineEventKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *TimelineEventAppend) SetKind(v TimelineEventKind)`

SetKind sets Kind field to given value.


### GetMessage

`func (o *TimelineEventAppend) GetMessage() string`

GetMessage returns the Message field if non-nil, zero value otherwise.

### GetMessageOk

`func (o *TimelineEventAppend) GetMessageOk() (*string, bool)`

GetMessageOk returns a tuple with the Message field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessage

`func (o *TimelineEventAppend) SetMessage(v string)`

SetMessage sets Message field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


