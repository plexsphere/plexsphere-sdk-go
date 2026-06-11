# Reachability

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**State** | [**ReachabilityState**](ReachabilityState.md) |  | 
**LastHeartbeatAt** | Pointer to **time.Time** | Server-side timestamp of the most recently accepted heartbeat, or &#x60;null&#x60; until the first heartbeat is accepted.  | [optional] 
**ChangedAt** | **time.Time** | Server-side timestamp of the most recent transition into the current &#x60;state&#x60;. Always present — for a Node that has never sent a heartbeat this is the timestamp at which the reachability row was first materialised.  | 

## Methods

### NewReachability

`func NewReachability(state ReachabilityState, changedAt time.Time, ) *Reachability`

NewReachability instantiates a new Reachability object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewReachabilityWithDefaults

`func NewReachabilityWithDefaults() *Reachability`

NewReachabilityWithDefaults instantiates a new Reachability object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetState

`func (o *Reachability) GetState() ReachabilityState`

GetState returns the State field if non-nil, zero value otherwise.

### GetStateOk

`func (o *Reachability) GetStateOk() (*ReachabilityState, bool)`

GetStateOk returns a tuple with the State field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetState

`func (o *Reachability) SetState(v ReachabilityState)`

SetState sets State field to given value.


### GetLastHeartbeatAt

`func (o *Reachability) GetLastHeartbeatAt() time.Time`

GetLastHeartbeatAt returns the LastHeartbeatAt field if non-nil, zero value otherwise.

### GetLastHeartbeatAtOk

`func (o *Reachability) GetLastHeartbeatAtOk() (*time.Time, bool)`

GetLastHeartbeatAtOk returns a tuple with the LastHeartbeatAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLastHeartbeatAt

`func (o *Reachability) SetLastHeartbeatAt(v time.Time)`

SetLastHeartbeatAt sets LastHeartbeatAt field to given value.

### HasLastHeartbeatAt

`func (o *Reachability) HasLastHeartbeatAt() bool`

HasLastHeartbeatAt returns a boolean if a field has been set.

### GetChangedAt

`func (o *Reachability) GetChangedAt() time.Time`

GetChangedAt returns the ChangedAt field if non-nil, zero value otherwise.

### GetChangedAtOk

`func (o *Reachability) GetChangedAtOk() (*time.Time, bool)`

GetChangedAtOk returns a tuple with the ChangedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChangedAt

`func (o *Reachability) SetChangedAt(v time.Time)`

SetChangedAt sets ChangedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


