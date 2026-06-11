# SessionTargetSSH

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**User** | **string** | Login user the mediated SSH session connects as. | 
**AllowedCommands** | Pointer to **[]string** | Optional allowlist of commands the session may run. An empty or omitted list grants an unconstrained interactive session; bounded at 64 entries.  | [optional] 

## Methods

### NewSessionTargetSSH

`func NewSessionTargetSSH(user string, ) *SessionTargetSSH`

NewSessionTargetSSH instantiates a new SessionTargetSSH object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSessionTargetSSHWithDefaults

`func NewSessionTargetSSHWithDefaults() *SessionTargetSSH`

NewSessionTargetSSHWithDefaults instantiates a new SessionTargetSSH object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUser

`func (o *SessionTargetSSH) GetUser() string`

GetUser returns the User field if non-nil, zero value otherwise.

### GetUserOk

`func (o *SessionTargetSSH) GetUserOk() (*string, bool)`

GetUserOk returns a tuple with the User field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUser

`func (o *SessionTargetSSH) SetUser(v string)`

SetUser sets User field to given value.


### GetAllowedCommands

`func (o *SessionTargetSSH) GetAllowedCommands() []string`

GetAllowedCommands returns the AllowedCommands field if non-nil, zero value otherwise.

### GetAllowedCommandsOk

`func (o *SessionTargetSSH) GetAllowedCommandsOk() (*[]string, bool)`

GetAllowedCommandsOk returns a tuple with the AllowedCommands field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAllowedCommands

`func (o *SessionTargetSSH) SetAllowedCommands(v []string)`

SetAllowedCommands sets AllowedCommands field to given value.

### HasAllowedCommands

`func (o *SessionTargetSSH) HasAllowedCommands() bool`

HasAllowedCommands returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


