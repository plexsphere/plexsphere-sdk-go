# ManagedPushTarget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Enabled** | **bool** | Whether managed pushes are admitted against this target. | 
**ApiServerUrl** | **string** | API-server URL of the managed-push cluster, parsed from the attached kubeconfig.  | 
**KubeconfigSha256** | **string** | Hex-encoded SHA-256 fingerprint of the kubeconfig plaintext. Display-only — lets an operator confirm which kubeconfig is sealed without exposing its contents.  | 
**CreatedAt** | **time.Time** | Timestamp the target was first attached. | 
**UpdatedAt** | **time.Time** | Timestamp the target was last replaced. | 

## Methods

### NewManagedPushTarget

`func NewManagedPushTarget(enabled bool, apiServerUrl string, kubeconfigSha256 string, createdAt time.Time, updatedAt time.Time, ) *ManagedPushTarget`

NewManagedPushTarget instantiates a new ManagedPushTarget object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewManagedPushTargetWithDefaults

`func NewManagedPushTargetWithDefaults() *ManagedPushTarget`

NewManagedPushTargetWithDefaults instantiates a new ManagedPushTarget object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetEnabled

`func (o *ManagedPushTarget) GetEnabled() bool`

GetEnabled returns the Enabled field if non-nil, zero value otherwise.

### GetEnabledOk

`func (o *ManagedPushTarget) GetEnabledOk() (*bool, bool)`

GetEnabledOk returns a tuple with the Enabled field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEnabled

`func (o *ManagedPushTarget) SetEnabled(v bool)`

SetEnabled sets Enabled field to given value.


### GetApiServerUrl

`func (o *ManagedPushTarget) GetApiServerUrl() string`

GetApiServerUrl returns the ApiServerUrl field if non-nil, zero value otherwise.

### GetApiServerUrlOk

`func (o *ManagedPushTarget) GetApiServerUrlOk() (*string, bool)`

GetApiServerUrlOk returns a tuple with the ApiServerUrl field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetApiServerUrl

`func (o *ManagedPushTarget) SetApiServerUrl(v string)`

SetApiServerUrl sets ApiServerUrl field to given value.


### GetKubeconfigSha256

`func (o *ManagedPushTarget) GetKubeconfigSha256() string`

GetKubeconfigSha256 returns the KubeconfigSha256 field if non-nil, zero value otherwise.

### GetKubeconfigSha256Ok

`func (o *ManagedPushTarget) GetKubeconfigSha256Ok() (*string, bool)`

GetKubeconfigSha256Ok returns a tuple with the KubeconfigSha256 field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKubeconfigSha256

`func (o *ManagedPushTarget) SetKubeconfigSha256(v string)`

SetKubeconfigSha256 sets KubeconfigSha256 field to given value.


### GetCreatedAt

`func (o *ManagedPushTarget) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *ManagedPushTarget) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *ManagedPushTarget) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *ManagedPushTarget) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *ManagedPushTarget) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *ManagedPushTarget) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


