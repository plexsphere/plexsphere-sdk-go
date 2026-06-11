# BridgeRelayConfigureRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Enabled** | **bool** | Whether the relay is active. A disabled relay keeps its configuration but programs no listener on the Node.  | 
**ListenPort** | **int32** | UDP port the relay listens on. Outside &#x60;1..65535&#x60; the write is rejected with &#x60;400 relay_port_out_of_range&#x60;.  | 

## Methods

### NewBridgeRelayConfigureRequest

`func NewBridgeRelayConfigureRequest(enabled bool, listenPort int32, ) *BridgeRelayConfigureRequest`

NewBridgeRelayConfigureRequest instantiates a new BridgeRelayConfigureRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeRelayConfigureRequestWithDefaults

`func NewBridgeRelayConfigureRequestWithDefaults() *BridgeRelayConfigureRequest`

NewBridgeRelayConfigureRequestWithDefaults instantiates a new BridgeRelayConfigureRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetEnabled

`func (o *BridgeRelayConfigureRequest) GetEnabled() bool`

GetEnabled returns the Enabled field if non-nil, zero value otherwise.

### GetEnabledOk

`func (o *BridgeRelayConfigureRequest) GetEnabledOk() (*bool, bool)`

GetEnabledOk returns a tuple with the Enabled field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnabled

`func (o *BridgeRelayConfigureRequest) SetEnabled(v bool)`

SetEnabled sets Enabled field to given value.


### GetListenPort

`func (o *BridgeRelayConfigureRequest) GetListenPort() int32`

GetListenPort returns the ListenPort field if non-nil, zero value otherwise.

### GetListenPortOk

`func (o *BridgeRelayConfigureRequest) GetListenPortOk() (*int32, bool)`

GetListenPortOk returns a tuple with the ListenPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetListenPort

`func (o *BridgeRelayConfigureRequest) SetListenPort(v int32)`

SetListenPort sets ListenPort field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


