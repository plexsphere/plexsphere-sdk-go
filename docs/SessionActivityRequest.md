# SessionActivityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ssh** | Pointer to [**SessionActivitySSH**](SessionActivitySSH.md) | Populated only for an &#x60;ssh&#x60; session. | [optional] 
**K8s** | Pointer to [**SessionActivityK8s**](SessionActivityK8s.md) | Populated only for a &#x60;k8s&#x60; session. | [optional] 
**Tcp** | Pointer to [**SessionActivityTCP**](SessionActivityTCP.md) | Populated only for a &#x60;tcp&#x60; session. | [optional] 

## Methods

### NewSessionActivityRequest

`func NewSessionActivityRequest() *SessionActivityRequest`

NewSessionActivityRequest instantiates a new SessionActivityRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSessionActivityRequestWithDefaults

`func NewSessionActivityRequestWithDefaults() *SessionActivityRequest`

NewSessionActivityRequestWithDefaults instantiates a new SessionActivityRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSsh

`func (o *SessionActivityRequest) GetSsh() SessionActivitySSH`

GetSsh returns the Ssh field if non-nil, zero value otherwise.

### GetSshOk

`func (o *SessionActivityRequest) GetSshOk() (*SessionActivitySSH, bool)`

GetSshOk returns a tuple with the Ssh field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSsh

`func (o *SessionActivityRequest) SetSsh(v SessionActivitySSH)`

SetSsh sets Ssh field to given value.

### HasSsh

`func (o *SessionActivityRequest) HasSsh() bool`

HasSsh returns a boolean if a field has been set.

### GetK8s

`func (o *SessionActivityRequest) GetK8s() SessionActivityK8s`

GetK8s returns the K8s field if non-nil, zero value otherwise.

### GetK8sOk

`func (o *SessionActivityRequest) GetK8sOk() (*SessionActivityK8s, bool)`

GetK8sOk returns a tuple with the K8s field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetK8s

`func (o *SessionActivityRequest) SetK8s(v SessionActivityK8s)`

SetK8s sets K8s field to given value.

### HasK8s

`func (o *SessionActivityRequest) HasK8s() bool`

HasK8s returns a boolean if a field has been set.

### GetTcp

`func (o *SessionActivityRequest) GetTcp() SessionActivityTCP`

GetTcp returns the Tcp field if non-nil, zero value otherwise.

### GetTcpOk

`func (o *SessionActivityRequest) GetTcpOk() (*SessionActivityTCP, bool)`

GetTcpOk returns a tuple with the Tcp field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTcp

`func (o *SessionActivityRequest) SetTcp(v SessionActivityTCP)`

SetTcp sets Tcp field to given value.

### HasTcp

`func (o *SessionActivityRequest) HasTcp() bool`

HasTcp returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


