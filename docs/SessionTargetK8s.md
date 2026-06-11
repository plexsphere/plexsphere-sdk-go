# SessionTargetK8s

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**User** | **string** | User the mediated Kubernetes session impersonates. | 
**ImpersonateGroups** | Pointer to **[]string** | Optional impersonation groups the session asserts. Bounded at 32 entries.  | [optional] 

## Methods

### NewSessionTargetK8s

`func NewSessionTargetK8s(user string, ) *SessionTargetK8s`

NewSessionTargetK8s instantiates a new SessionTargetK8s object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewSessionTargetK8sWithDefaults

`func NewSessionTargetK8sWithDefaults() *SessionTargetK8s`

NewSessionTargetK8sWithDefaults instantiates a new SessionTargetK8s object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetUser

`func (o *SessionTargetK8s) GetUser() string`

GetUser returns the User field if non-nil, zero value otherwise.

### GetUserOk

`func (o *SessionTargetK8s) GetUserOk() (*string, bool)`

GetUserOk returns a tuple with the User field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUser

`func (o *SessionTargetK8s) SetUser(v string)`

SetUser sets User field to given value.


### GetImpersonateGroups

`func (o *SessionTargetK8s) GetImpersonateGroups() []string`

GetImpersonateGroups returns the ImpersonateGroups field if non-nil, zero value otherwise.

### GetImpersonateGroupsOk

`func (o *SessionTargetK8s) GetImpersonateGroupsOk() (*[]string, bool)`

GetImpersonateGroupsOk returns a tuple with the ImpersonateGroups field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetImpersonateGroups

`func (o *SessionTargetK8s) SetImpersonateGroups(v []string)`

SetImpersonateGroups sets ImpersonateGroups field to given value.

### HasImpersonateGroups

`func (o *SessionTargetK8s) HasImpersonateGroups() bool`

HasImpersonateGroups returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


