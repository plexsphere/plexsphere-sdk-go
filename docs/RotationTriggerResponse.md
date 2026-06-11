# RotationTriggerResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RotationId** | **string** | Identifier of the &#x60;peer_key_rotation&#x60; row the request recorded — freshly inserted, or the in-flight row when &#x60;already_pending&#x60; is true.  | 
**PeerId** | **string** | Identifier of the live Peer whose mesh key the rotation targets.  | 
**AlreadyPending** | **bool** | True when the response reflects a pre-existing pending rotation — an idempotent re-request that surfaced the in-flight row — rather than a freshly recorded request. Operators switch on this flag to distinguish a newly dispatched &#x60;rotate_keys&#x60; command from an idempotent no-op.  | 

## Methods

### NewRotationTriggerResponse

`func NewRotationTriggerResponse(rotationId string, peerId string, alreadyPending bool, ) *RotationTriggerResponse`

NewRotationTriggerResponse instantiates a new RotationTriggerResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRotationTriggerResponseWithDefaults

`func NewRotationTriggerResponseWithDefaults() *RotationTriggerResponse`

NewRotationTriggerResponseWithDefaults instantiates a new RotationTriggerResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetRotationId

`func (o *RotationTriggerResponse) GetRotationId() string`

GetRotationId returns the RotationId field if non-nil, zero value otherwise.

### GetRotationIdOk

`func (o *RotationTriggerResponse) GetRotationIdOk() (*string, bool)`

GetRotationIdOk returns a tuple with the RotationId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRotationId

`func (o *RotationTriggerResponse) SetRotationId(v string)`

SetRotationId sets RotationId field to given value.


### GetPeerId

`func (o *RotationTriggerResponse) GetPeerId() string`

GetPeerId returns the PeerId field if non-nil, zero value otherwise.

### GetPeerIdOk

`func (o *RotationTriggerResponse) GetPeerIdOk() (*string, bool)`

GetPeerIdOk returns a tuple with the PeerId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPeerId

`func (o *RotationTriggerResponse) SetPeerId(v string)`

SetPeerId sets PeerId field to given value.


### GetAlreadyPending

`func (o *RotationTriggerResponse) GetAlreadyPending() bool`

GetAlreadyPending returns the AlreadyPending field if non-nil, zero value otherwise.

### GetAlreadyPendingOk

`func (o *RotationTriggerResponse) GetAlreadyPendingOk() (*bool, bool)`

GetAlreadyPendingOk returns a tuple with the AlreadyPending field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAlreadyPending

`func (o *RotationTriggerResponse) SetAlreadyPending(v bool)`

SetAlreadyPending sets AlreadyPending field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


