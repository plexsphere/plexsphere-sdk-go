# BridgeRelayResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ResourceId** | **string** | Owning bridge Resource (UUIDv7) — the relay primary key. | 
**Enabled** | **bool** | Whether the relay is active. | 
**ListenPort** | **int32** | UDP port the relay listens on. | 
**CreatedAt** | **time.Time** | Relay creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). | 

## Methods

### NewBridgeRelayResponse

`func NewBridgeRelayResponse(resourceId string, enabled bool, listenPort int32, createdAt time.Time, updatedAt time.Time, ) *BridgeRelayResponse`

NewBridgeRelayResponse instantiates a new BridgeRelayResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeRelayResponseWithDefaults

`func NewBridgeRelayResponseWithDefaults() *BridgeRelayResponse`

NewBridgeRelayResponseWithDefaults instantiates a new BridgeRelayResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetResourceId

`func (o *BridgeRelayResponse) GetResourceId() string`

GetResourceId returns the ResourceId field if non-nil, zero value otherwise.

### GetResourceIdOk

`func (o *BridgeRelayResponse) GetResourceIdOk() (*string, bool)`

GetResourceIdOk returns a tuple with the ResourceId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResourceId

`func (o *BridgeRelayResponse) SetResourceId(v string)`

SetResourceId sets ResourceId field to given value.


### GetEnabled

`func (o *BridgeRelayResponse) GetEnabled() bool`

GetEnabled returns the Enabled field if non-nil, zero value otherwise.

### GetEnabledOk

`func (o *BridgeRelayResponse) GetEnabledOk() (*bool, bool)`

GetEnabledOk returns a tuple with the Enabled field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnabled

`func (o *BridgeRelayResponse) SetEnabled(v bool)`

SetEnabled sets Enabled field to given value.


### GetListenPort

`func (o *BridgeRelayResponse) GetListenPort() int32`

GetListenPort returns the ListenPort field if non-nil, zero value otherwise.

### GetListenPortOk

`func (o *BridgeRelayResponse) GetListenPortOk() (*int32, bool)`

GetListenPortOk returns a tuple with the ListenPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetListenPort

`func (o *BridgeRelayResponse) SetListenPort(v int32)`

SetListenPort sets ListenPort field to given value.


### GetCreatedAt

`func (o *BridgeRelayResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *BridgeRelayResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *BridgeRelayResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *BridgeRelayResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *BridgeRelayResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *BridgeRelayResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


