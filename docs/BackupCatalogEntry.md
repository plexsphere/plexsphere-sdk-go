# BackupCatalogEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Store** | **string** | The store the row describes. | 
**Method** | **string** | How the store is backed up. | 
**Cadence** | **string** | How often the store is backed up. | 
**Retention** | **string** | How long the store&#39;s backups are retained. | 
**Priority** | [**BackupPriority**](BackupPriority.md) |  | 
**RestoreStep** | **int32** | The restore-plan step order this store is restored in, or &#x60;0&#x60; when the store is not part of the linear restore sequence.  | 
**Notes** | **string** | Free-form notes about backing up or restoring the store. | 

## Methods

### NewBackupCatalogEntry

`func NewBackupCatalogEntry(store string, method string, cadence string, retention string, priority BackupPriority, restoreStep int32, notes string, ) *BackupCatalogEntry`

NewBackupCatalogEntry instantiates a new BackupCatalogEntry object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBackupCatalogEntryWithDefaults

`func NewBackupCatalogEntryWithDefaults() *BackupCatalogEntry`

NewBackupCatalogEntryWithDefaults instantiates a new BackupCatalogEntry object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetStore

`func (o *BackupCatalogEntry) GetStore() string`

GetStore returns the Store field if non-nil, zero value otherwise.

### GetStoreOk

`func (o *BackupCatalogEntry) GetStoreOk() (*string, bool)`

GetStoreOk returns a tuple with the Store field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStore

`func (o *BackupCatalogEntry) SetStore(v string)`

SetStore sets Store field to given value.


### GetMethod

`func (o *BackupCatalogEntry) GetMethod() string`

GetMethod returns the Method field if non-nil, zero value otherwise.

### GetMethodOk

`func (o *BackupCatalogEntry) GetMethodOk() (*string, bool)`

GetMethodOk returns a tuple with the Method field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMethod

`func (o *BackupCatalogEntry) SetMethod(v string)`

SetMethod sets Method field to given value.


### GetCadence

`func (o *BackupCatalogEntry) GetCadence() string`

GetCadence returns the Cadence field if non-nil, zero value otherwise.

### GetCadenceOk

`func (o *BackupCatalogEntry) GetCadenceOk() (*string, bool)`

GetCadenceOk returns a tuple with the Cadence field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCadence

`func (o *BackupCatalogEntry) SetCadence(v string)`

SetCadence sets Cadence field to given value.


### GetRetention

`func (o *BackupCatalogEntry) GetRetention() string`

GetRetention returns the Retention field if non-nil, zero value otherwise.

### GetRetentionOk

`func (o *BackupCatalogEntry) GetRetentionOk() (*string, bool)`

GetRetentionOk returns a tuple with the Retention field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRetention

`func (o *BackupCatalogEntry) SetRetention(v string)`

SetRetention sets Retention field to given value.


### GetPriority

`func (o *BackupCatalogEntry) GetPriority() BackupPriority`

GetPriority returns the Priority field if non-nil, zero value otherwise.

### GetPriorityOk

`func (o *BackupCatalogEntry) GetPriorityOk() (*BackupPriority, bool)`

GetPriorityOk returns a tuple with the Priority field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPriority

`func (o *BackupCatalogEntry) SetPriority(v BackupPriority)`

SetPriority sets Priority field to given value.


### GetRestoreStep

`func (o *BackupCatalogEntry) GetRestoreStep() int32`

GetRestoreStep returns the RestoreStep field if non-nil, zero value otherwise.

### GetRestoreStepOk

`func (o *BackupCatalogEntry) GetRestoreStepOk() (*int32, bool)`

GetRestoreStepOk returns a tuple with the RestoreStep field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRestoreStep

`func (o *BackupCatalogEntry) SetRestoreStep(v int32)`

SetRestoreStep sets RestoreStep field to given value.


### GetNotes

`func (o *BackupCatalogEntry) GetNotes() string`

GetNotes returns the Notes field if non-nil, zero value otherwise.

### GetNotesOk

`func (o *BackupCatalogEntry) GetNotesOk() (*string, bool)`

GetNotesOk returns a tuple with the Notes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNotes

`func (o *BackupCatalogEntry) SetNotes(v string)`

SetNotes sets Notes field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


