# DeviceTokenRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DeviceCode** | **string** | Device code returned by /v1/auth/device-code. | 
**ClientId** | Pointer to **string** | Optional OIDC client identifier override. | [optional] 

## Methods

### NewDeviceTokenRequest

`func NewDeviceTokenRequest(deviceCode string, ) *DeviceTokenRequest`

NewDeviceTokenRequest instantiates a new DeviceTokenRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDeviceTokenRequestWithDefaults

`func NewDeviceTokenRequestWithDefaults() *DeviceTokenRequest`

NewDeviceTokenRequestWithDefaults instantiates a new DeviceTokenRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDeviceCode

`func (o *DeviceTokenRequest) GetDeviceCode() string`

GetDeviceCode returns the DeviceCode field if non-nil, zero value otherwise.

### GetDeviceCodeOk

`func (o *DeviceTokenRequest) GetDeviceCodeOk() (*string, bool)`

GetDeviceCodeOk returns a tuple with the DeviceCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDeviceCode

`func (o *DeviceTokenRequest) SetDeviceCode(v string)`

SetDeviceCode sets DeviceCode field to given value.


### GetClientId

`func (o *DeviceTokenRequest) GetClientId() string`

GetClientId returns the ClientId field if non-nil, zero value otherwise.

### GetClientIdOk

`func (o *DeviceTokenRequest) GetClientIdOk() (*string, bool)`

GetClientIdOk returns a tuple with the ClientId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetClientId

`func (o *DeviceTokenRequest) SetClientId(v string)`

SetClientId sets ClientId field to given value.

### HasClientId

`func (o *DeviceTokenRequest) HasClientId() bool`

HasClientId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


