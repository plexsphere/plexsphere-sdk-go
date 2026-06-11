# ExecutionEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Event identifier (UUIDv7). | 
**Status** | [**ExecutionStatus**](ExecutionStatus.md) |  | 
**OccurredAt** | **time.Time** | Timestamp the status advance occurred (UTC). | 
**Detail** | Pointer to **string** | Optional free-text detail recorded with the advance — for a failed status this carries the reported error text.  | [optional] 

## Methods

### NewExecutionEvent

`func NewExecutionEvent(id string, status ExecutionStatus, occurredAt time.Time, ) *ExecutionEvent`

NewExecutionEvent instantiates a new ExecutionEvent object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewExecutionEventWithDefaults

`func NewExecutionEventWithDefaults() *ExecutionEvent`

NewExecutionEventWithDefaults instantiates a new ExecutionEvent object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *ExecutionEvent) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *ExecutionEvent) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *ExecutionEvent) SetId(v string)`

SetId sets Id field to given value.


### GetStatus

`func (o *ExecutionEvent) GetStatus() ExecutionStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *ExecutionEvent) GetStatusOk() (*ExecutionStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *ExecutionEvent) SetStatus(v ExecutionStatus)`

SetStatus sets Status field to given value.


### GetOccurredAt

`func (o *ExecutionEvent) GetOccurredAt() time.Time`

GetOccurredAt returns the OccurredAt field if non-nil, zero value otherwise.

### GetOccurredAtOk

`func (o *ExecutionEvent) GetOccurredAtOk() (*time.Time, bool)`

GetOccurredAtOk returns a tuple with the OccurredAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOccurredAt

`func (o *ExecutionEvent) SetOccurredAt(v time.Time)`

SetOccurredAt sets OccurredAt field to given value.


### GetDetail

`func (o *ExecutionEvent) GetDetail() string`

GetDetail returns the Detail field if non-nil, zero value otherwise.

### GetDetailOk

`func (o *ExecutionEvent) GetDetailOk() (*string, bool)`

GetDetailOk returns a tuple with the Detail field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDetail

`func (o *ExecutionEvent) SetDetail(v string)`

SetDetail sets Detail field to given value.

### HasDetail

`func (o *ExecutionEvent) HasDetail() bool`

HasDetail returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


