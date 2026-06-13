# ManagedPushAttachRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**KubeconfigB64** | **string** | Base64-encoded kubeconfig for the managed-push cluster. The decoded plaintext is validated and sealed at rest; it is never echoed back in any response. Only embedded, in-band credentials are accepted (a token, or &#x60;client-certificate-data&#x60; / &#x60;client-key-data&#x60;, with &#x60;certificate-authority-data&#x60;); a kubeconfig carrying an &#x60;exec&#x60; or &#x60;auth-provider&#x60; plugin, a file-path credential (&#x60;tokenFile&#x60;, &#x60;client-certificate&#x60;, &#x60;client-key&#x60;), a &#x60;certificate-authority&#x60; file path, or a &#x60;proxy-url&#x60; is rejected with &#x60;kubeconfig_invalid&#x60;.  | 
**Enabled** | **bool** | Whether managed pushes are admitted against this target. A disabled target rejects &#x60;PushManagedHook&#x60; with &#x60;managed_push_disabled&#x60;.  | 

## Methods

### NewManagedPushAttachRequest

`func NewManagedPushAttachRequest(kubeconfigB64 string, enabled bool, ) *ManagedPushAttachRequest`

NewManagedPushAttachRequest instantiates a new ManagedPushAttachRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewManagedPushAttachRequestWithDefaults

`func NewManagedPushAttachRequestWithDefaults() *ManagedPushAttachRequest`

NewManagedPushAttachRequestWithDefaults instantiates a new ManagedPushAttachRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKubeconfigB64

`func (o *ManagedPushAttachRequest) GetKubeconfigB64() string`

GetKubeconfigB64 returns the KubeconfigB64 field if non-nil, zero value otherwise.

### GetKubeconfigB64Ok

`func (o *ManagedPushAttachRequest) GetKubeconfigB64Ok() (*string, bool)`

GetKubeconfigB64Ok returns a tuple with the KubeconfigB64 field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKubeconfigB64

`func (o *ManagedPushAttachRequest) SetKubeconfigB64(v string)`

SetKubeconfigB64 sets KubeconfigB64 field to given value.


### GetEnabled

`func (o *ManagedPushAttachRequest) GetEnabled() bool`

GetEnabled returns the Enabled field if non-nil, zero value otherwise.

### GetEnabledOk

`func (o *ManagedPushAttachRequest) GetEnabledOk() (*bool, bool)`

GetEnabledOk returns a tuple with the Enabled field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnabled

`func (o *ManagedPushAttachRequest) SetEnabled(v bool)`

SetEnabled sets Enabled field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


