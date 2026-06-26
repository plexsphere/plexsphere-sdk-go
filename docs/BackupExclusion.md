# BackupExclusion

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | What is not backed up. | 
**Rationale** | **string** | Why it is not backed up. | 
**RecoveryPath** | **string** | How the gap is recovered without a backup. | 

## Methods

### NewBackupExclusion

`func NewBackupExclusion(name string, rationale string, recoveryPath string, ) *BackupExclusion`

NewBackupExclusion instantiates a new BackupExclusion object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBackupExclusionWithDefaults

`func NewBackupExclusionWithDefaults() *BackupExclusion`

NewBackupExclusionWithDefaults instantiates a new BackupExclusion object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *BackupExclusion) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *BackupExclusion) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *BackupExclusion) SetName(v string)`

SetName sets Name field to given value.


### GetRationale

`func (o *BackupExclusion) GetRationale() string`

GetRationale returns the Rationale field if non-nil, zero value otherwise.

### GetRationaleOk

`func (o *BackupExclusion) GetRationaleOk() (*string, bool)`

GetRationaleOk returns a tuple with the Rationale field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRationale

`func (o *BackupExclusion) SetRationale(v string)`

SetRationale sets Rationale field to given value.


### GetRecoveryPath

`func (o *BackupExclusion) GetRecoveryPath() string`

GetRecoveryPath returns the RecoveryPath field if non-nil, zero value otherwise.

### GetRecoveryPathOk

`func (o *BackupExclusion) GetRecoveryPathOk() (*string, bool)`

GetRecoveryPathOk returns a tuple with the RecoveryPath field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRecoveryPath

`func (o *BackupExclusion) SetRecoveryPath(v string)`

SetRecoveryPath sets RecoveryPath field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


