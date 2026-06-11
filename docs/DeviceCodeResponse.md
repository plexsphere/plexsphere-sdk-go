# DeviceCodeResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DeviceCode** | **string** | Opaque code the client polls with. | 
**UserCode** | **string** | Short code the end user types in a browser. | 
**VerificationUri** | **string** | URL the end user visits to confirm the device. | 
**VerificationUriComplete** | **string** | URL with the user_code pre-filled; RFC 8628 recommends presenting this as a QR code.  | 
**ExpiresIn** | **int32** | Lifetime of the device_code in seconds. | 
**Interval** | **int32** | Minimum polling interval in seconds. | 

## Methods

### NewDeviceCodeResponse

`func NewDeviceCodeResponse(deviceCode string, userCode string, verificationUri string, verificationUriComplete string, expiresIn int32, interval int32, ) *DeviceCodeResponse`

NewDeviceCodeResponse instantiates a new DeviceCodeResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDeviceCodeResponseWithDefaults

`func NewDeviceCodeResponseWithDefaults() *DeviceCodeResponse`

NewDeviceCodeResponseWithDefaults instantiates a new DeviceCodeResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDeviceCode

`func (o *DeviceCodeResponse) GetDeviceCode() string`

GetDeviceCode returns the DeviceCode field if non-nil, zero value otherwise.

### GetDeviceCodeOk

`func (o *DeviceCodeResponse) GetDeviceCodeOk() (*string, bool)`

GetDeviceCodeOk returns a tuple with the DeviceCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDeviceCode

`func (o *DeviceCodeResponse) SetDeviceCode(v string)`

SetDeviceCode sets DeviceCode field to given value.


### GetUserCode

`func (o *DeviceCodeResponse) GetUserCode() string`

GetUserCode returns the UserCode field if non-nil, zero value otherwise.

### GetUserCodeOk

`func (o *DeviceCodeResponse) GetUserCodeOk() (*string, bool)`

GetUserCodeOk returns a tuple with the UserCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserCode

`func (o *DeviceCodeResponse) SetUserCode(v string)`

SetUserCode sets UserCode field to given value.


### GetVerificationUri

`func (o *DeviceCodeResponse) GetVerificationUri() string`

GetVerificationUri returns the VerificationUri field if non-nil, zero value otherwise.

### GetVerificationUriOk

`func (o *DeviceCodeResponse) GetVerificationUriOk() (*string, bool)`

GetVerificationUriOk returns a tuple with the VerificationUri field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVerificationUri

`func (o *DeviceCodeResponse) SetVerificationUri(v string)`

SetVerificationUri sets VerificationUri field to given value.


### GetVerificationUriComplete

`func (o *DeviceCodeResponse) GetVerificationUriComplete() string`

GetVerificationUriComplete returns the VerificationUriComplete field if non-nil, zero value otherwise.

### GetVerificationUriCompleteOk

`func (o *DeviceCodeResponse) GetVerificationUriCompleteOk() (*string, bool)`

GetVerificationUriCompleteOk returns a tuple with the VerificationUriComplete field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVerificationUriComplete

`func (o *DeviceCodeResponse) SetVerificationUriComplete(v string)`

SetVerificationUriComplete sets VerificationUriComplete field to given value.


### GetExpiresIn

`func (o *DeviceCodeResponse) GetExpiresIn() int32`

GetExpiresIn returns the ExpiresIn field if non-nil, zero value otherwise.

### GetExpiresInOk

`func (o *DeviceCodeResponse) GetExpiresInOk() (*int32, bool)`

GetExpiresInOk returns a tuple with the ExpiresIn field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpiresIn

`func (o *DeviceCodeResponse) SetExpiresIn(v int32)`

SetExpiresIn sets ExpiresIn field to given value.


### GetInterval

`func (o *DeviceCodeResponse) GetInterval() int32`

GetInterval returns the Interval field if non-nil, zero value otherwise.

### GetIntervalOk

`func (o *DeviceCodeResponse) GetIntervalOk() (*int32, bool)`

GetIntervalOk returns a tuple with the Interval field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInterval

`func (o *DeviceCodeResponse) SetInterval(v int32)`

SetInterval sets Interval field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


