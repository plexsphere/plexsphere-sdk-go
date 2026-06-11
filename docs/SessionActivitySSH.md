# SessionActivitySSH

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Command** | **string** | The command the session executed, captured as raw text bounded at 1 KiB.  | 
**ExitCode** | Pointer to **int32** | Process exit code the command reported, when settled. | [optional] 
**StartedAt** | Pointer to **time.Time** | Timestamp the command started (UTC). | [optional] 
**CompletedAt** | Pointer to **time.Time** | Timestamp the command completed (UTC), when settled. | [optional] 

## Methods

### NewSessionActivitySSH

`func NewSessionActivitySSH(command string, ) *SessionActivitySSH`

NewSessionActivitySSH instantiates a new SessionActivitySSH object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSessionActivitySSHWithDefaults

`func NewSessionActivitySSHWithDefaults() *SessionActivitySSH`

NewSessionActivitySSHWithDefaults instantiates a new SessionActivitySSH object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCommand

`func (o *SessionActivitySSH) GetCommand() string`

GetCommand returns the Command field if non-nil, zero value otherwise.

### GetCommandOk

`func (o *SessionActivitySSH) GetCommandOk() (*string, bool)`

GetCommandOk returns a tuple with the Command field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCommand

`func (o *SessionActivitySSH) SetCommand(v string)`

SetCommand sets Command field to given value.


### GetExitCode

`func (o *SessionActivitySSH) GetExitCode() int32`

GetExitCode returns the ExitCode field if non-nil, zero value otherwise.

### GetExitCodeOk

`func (o *SessionActivitySSH) GetExitCodeOk() (*int32, bool)`

GetExitCodeOk returns a tuple with the ExitCode field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExitCode

`func (o *SessionActivitySSH) SetExitCode(v int32)`

SetExitCode sets ExitCode field to given value.

### HasExitCode

`func (o *SessionActivitySSH) HasExitCode() bool`

HasExitCode returns a boolean if a field has been set.

### GetStartedAt

`func (o *SessionActivitySSH) GetStartedAt() time.Time`

GetStartedAt returns the StartedAt field if non-nil, zero value otherwise.

### GetStartedAtOk

`func (o *SessionActivitySSH) GetStartedAtOk() (*time.Time, bool)`

GetStartedAtOk returns a tuple with the StartedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStartedAt

`func (o *SessionActivitySSH) SetStartedAt(v time.Time)`

SetStartedAt sets StartedAt field to given value.

### HasStartedAt

`func (o *SessionActivitySSH) HasStartedAt() bool`

HasStartedAt returns a boolean if a field has been set.

### GetCompletedAt

`func (o *SessionActivitySSH) GetCompletedAt() time.Time`

GetCompletedAt returns the CompletedAt field if non-nil, zero value otherwise.

### GetCompletedAtOk

`func (o *SessionActivitySSH) GetCompletedAtOk() (*time.Time, bool)`

GetCompletedAtOk returns a tuple with the CompletedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCompletedAt

`func (o *SessionActivitySSH) SetCompletedAt(v time.Time)`

SetCompletedAt sets CompletedAt field to given value.

### HasCompletedAt

`func (o *SessionActivitySSH) HasCompletedAt() bool`

HasCompletedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


