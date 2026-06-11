# SessionActivityTCP

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Phase** | [**SessionActivityTCPPhase**](SessionActivityTCPPhase.md) |  | 
**TargetHost** | Pointer to **string** | Target host the tunnel connected to. Present on &#x60;session_started&#x60;.  | [optional] 
**TargetPort** | Pointer to **int32** | Target port the tunnel connected to. Present on &#x60;session_started&#x60;.  | [optional] 
**BytesIn** | Pointer to **int32** | Bytes forwarded from the operator to the target. Present on &#x60;session_ended&#x60;.  | [optional] 
**BytesOut** | Pointer to **int32** | Bytes forwarded from the target to the operator. Present on &#x60;session_ended&#x60;.  | [optional] 
**TerminatedBy** | Pointer to [**SessionActivityTCPTerminatedBy**](SessionActivityTCPTerminatedBy.md) |  | [optional] 

## Methods

### NewSessionActivityTCP

`func NewSessionActivityTCP(phase SessionActivityTCPPhase, ) *SessionActivityTCP`

NewSessionActivityTCP instantiates a new SessionActivityTCP object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSessionActivityTCPWithDefaults

`func NewSessionActivityTCPWithDefaults() *SessionActivityTCP`

NewSessionActivityTCPWithDefaults instantiates a new SessionActivityTCP object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPhase

`func (o *SessionActivityTCP) GetPhase() SessionActivityTCPPhase`

GetPhase returns the Phase field if non-nil, zero value otherwise.

### GetPhaseOk

`func (o *SessionActivityTCP) GetPhaseOk() (*SessionActivityTCPPhase, bool)`

GetPhaseOk returns a tuple with the Phase field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPhase

`func (o *SessionActivityTCP) SetPhase(v SessionActivityTCPPhase)`

SetPhase sets Phase field to given value.


### GetTargetHost

`func (o *SessionActivityTCP) GetTargetHost() string`

GetTargetHost returns the TargetHost field if non-nil, zero value otherwise.

### GetTargetHostOk

`func (o *SessionActivityTCP) GetTargetHostOk() (*string, bool)`

GetTargetHostOk returns a tuple with the TargetHost field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetHost

`func (o *SessionActivityTCP) SetTargetHost(v string)`

SetTargetHost sets TargetHost field to given value.

### HasTargetHost

`func (o *SessionActivityTCP) HasTargetHost() bool`

HasTargetHost returns a boolean if a field has been set.

### GetTargetPort

`func (o *SessionActivityTCP) GetTargetPort() int32`

GetTargetPort returns the TargetPort field if non-nil, zero value otherwise.

### GetTargetPortOk

`func (o *SessionActivityTCP) GetTargetPortOk() (*int32, bool)`

GetTargetPortOk returns a tuple with the TargetPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetPort

`func (o *SessionActivityTCP) SetTargetPort(v int32)`

SetTargetPort sets TargetPort field to given value.

### HasTargetPort

`func (o *SessionActivityTCP) HasTargetPort() bool`

HasTargetPort returns a boolean if a field has been set.

### GetBytesIn

`func (o *SessionActivityTCP) GetBytesIn() int32`

GetBytesIn returns the BytesIn field if non-nil, zero value otherwise.

### GetBytesInOk

`func (o *SessionActivityTCP) GetBytesInOk() (*int32, bool)`

GetBytesInOk returns a tuple with the BytesIn field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBytesIn

`func (o *SessionActivityTCP) SetBytesIn(v int32)`

SetBytesIn sets BytesIn field to given value.

### HasBytesIn

`func (o *SessionActivityTCP) HasBytesIn() bool`

HasBytesIn returns a boolean if a field has been set.

### GetBytesOut

`func (o *SessionActivityTCP) GetBytesOut() int32`

GetBytesOut returns the BytesOut field if non-nil, zero value otherwise.

### GetBytesOutOk

`func (o *SessionActivityTCP) GetBytesOutOk() (*int32, bool)`

GetBytesOutOk returns a tuple with the BytesOut field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBytesOut

`func (o *SessionActivityTCP) SetBytesOut(v int32)`

SetBytesOut sets BytesOut field to given value.

### HasBytesOut

`func (o *SessionActivityTCP) HasBytesOut() bool`

HasBytesOut returns a boolean if a field has been set.

### GetTerminatedBy

`func (o *SessionActivityTCP) GetTerminatedBy() SessionActivityTCPTerminatedBy`

GetTerminatedBy returns the TerminatedBy field if non-nil, zero value otherwise.

### GetTerminatedByOk

`func (o *SessionActivityTCP) GetTerminatedByOk() (*SessionActivityTCPTerminatedBy, bool)`

GetTerminatedByOk returns a tuple with the TerminatedBy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTerminatedBy

`func (o *SessionActivityTCP) SetTerminatedBy(v SessionActivityTCPTerminatedBy)`

SetTerminatedBy sets TerminatedBy field to given value.

### HasTerminatedBy

`func (o *SessionActivityTCP) HasTerminatedBy() bool`

HasTerminatedBy returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


