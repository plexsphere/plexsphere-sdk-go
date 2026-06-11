# DeviceApproveRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UserCode** | **string** | Short user-typed code from the device-code response. The base32 alphabet is uppercase A–Z and 2–7; an optional ASCII dash separating the two 4-character halves (e.g. &#x60;ABCD-EFGH&#x60; or &#x60;ABCDEFGH&#x60;) is accepted.  | 

## Methods

### NewDeviceApproveRequest

`func NewDeviceApproveRequest(userCode string, ) *DeviceApproveRequest`

NewDeviceApproveRequest instantiates a new DeviceApproveRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDeviceApproveRequestWithDefaults

`func NewDeviceApproveRequestWithDefaults() *DeviceApproveRequest`

NewDeviceApproveRequestWithDefaults instantiates a new DeviceApproveRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUserCode

`func (o *DeviceApproveRequest) GetUserCode() string`

GetUserCode returns the UserCode field if non-nil, zero value otherwise.

### GetUserCodeOk

`func (o *DeviceApproveRequest) GetUserCodeOk() (*string, bool)`

GetUserCodeOk returns a tuple with the UserCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUserCode

`func (o *DeviceApproveRequest) SetUserCode(v string)`

SetUserCode sets UserCode field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


