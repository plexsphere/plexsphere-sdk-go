# SessionTargetTCP

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Host** | **string** | Target host the tunnel forwards to. | 
**Port** | **int32** | Target port the tunnel forwards to. | 

## Methods

### NewSessionTargetTCP

`func NewSessionTargetTCP(host string, port int32, ) *SessionTargetTCP`

NewSessionTargetTCP instantiates a new SessionTargetTCP object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSessionTargetTCPWithDefaults

`func NewSessionTargetTCPWithDefaults() *SessionTargetTCP`

NewSessionTargetTCPWithDefaults instantiates a new SessionTargetTCP object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetHost

`func (o *SessionTargetTCP) GetHost() string`

GetHost returns the Host field if non-nil, zero value otherwise.

### GetHostOk

`func (o *SessionTargetTCP) GetHostOk() (*string, bool)`

GetHostOk returns a tuple with the Host field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHost

`func (o *SessionTargetTCP) SetHost(v string)`

SetHost sets Host field to given value.


### GetPort

`func (o *SessionTargetTCP) GetPort() int32`

GetPort returns the Port field if non-nil, zero value otherwise.

### GetPortOk

`func (o *SessionTargetTCP) GetPortOk() (*int32, bool)`

GetPortOk returns a tuple with the Port field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPort

`func (o *SessionTargetTCP) SetPort(v int32)`

SetPort sets Port field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


