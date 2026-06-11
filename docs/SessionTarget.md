# SessionTarget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ssh** | Pointer to [**SessionTargetSSH**](SessionTargetSSH.md) | Populated only when &#x60;kind&#x60; is &#x60;ssh&#x60;.  | [optional] 
**K8s** | Pointer to [**SessionTargetK8s**](SessionTargetK8s.md) | Populated only when &#x60;kind&#x60; is &#x60;k8s&#x60;.  | [optional] 
**Tcp** | Pointer to [**SessionTargetTCP**](SessionTargetTCP.md) | Populated only when &#x60;kind&#x60; is &#x60;tcp&#x60;.  | [optional] 

## Methods

### NewSessionTarget

`func NewSessionTarget() *SessionTarget`

NewSessionTarget instantiates a new SessionTarget object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSessionTargetWithDefaults

`func NewSessionTargetWithDefaults() *SessionTarget`

NewSessionTargetWithDefaults instantiates a new SessionTarget object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSsh

`func (o *SessionTarget) GetSsh() SessionTargetSSH`

GetSsh returns the Ssh field if non-nil, zero value otherwise.

### GetSshOk

`func (o *SessionTarget) GetSshOk() (*SessionTargetSSH, bool)`

GetSshOk returns a tuple with the Ssh field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSsh

`func (o *SessionTarget) SetSsh(v SessionTargetSSH)`

SetSsh sets Ssh field to given value.

### HasSsh

`func (o *SessionTarget) HasSsh() bool`

HasSsh returns a boolean if a field has been set.

### GetK8s

`func (o *SessionTarget) GetK8s() SessionTargetK8s`

GetK8s returns the K8s field if non-nil, zero value otherwise.

### GetK8sOk

`func (o *SessionTarget) GetK8sOk() (*SessionTargetK8s, bool)`

GetK8sOk returns a tuple with the K8s field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetK8s

`func (o *SessionTarget) SetK8s(v SessionTargetK8s)`

SetK8s sets K8s field to given value.

### HasK8s

`func (o *SessionTarget) HasK8s() bool`

HasK8s returns a boolean if a field has been set.

### GetTcp

`func (o *SessionTarget) GetTcp() SessionTargetTCP`

GetTcp returns the Tcp field if non-nil, zero value otherwise.

### GetTcpOk

`func (o *SessionTarget) GetTcpOk() (*SessionTargetTCP, bool)`

GetTcpOk returns a tuple with the Tcp field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTcp

`func (o *SessionTarget) SetTcp(v SessionTargetTCP)`

SetTcp sets Tcp field to given value.

### HasTcp

`func (o *SessionTarget) HasTcp() bool`

HasTcp returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


