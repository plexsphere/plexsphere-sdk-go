# BackupCatalog

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Entries** | [**[]BackupCatalogEntry**](BackupCatalogEntry.md) | The per-store coverage table. | 
**Targets** | [**[]BackupTarget**](BackupTarget.md) | The recovery objectives per plane. | 
**Exclusions** | [**[]BackupExclusion**](BackupExclusion.md) | What the platform deliberately does not back up. | 

## Methods

### NewBackupCatalog

`func NewBackupCatalog(entries []BackupCatalogEntry, targets []BackupTarget, exclusions []BackupExclusion, ) *BackupCatalog`

NewBackupCatalog instantiates a new BackupCatalog object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBackupCatalogWithDefaults

`func NewBackupCatalogWithDefaults() *BackupCatalog`

NewBackupCatalogWithDefaults instantiates a new BackupCatalog object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetEntries

`func (o *BackupCatalog) GetEntries() []BackupCatalogEntry`

GetEntries returns the Entries field if non-nil, zero value otherwise.

### GetEntriesOk

`func (o *BackupCatalog) GetEntriesOk() (*[]BackupCatalogEntry, bool)`

GetEntriesOk returns a tuple with the Entries field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEntries

`func (o *BackupCatalog) SetEntries(v []BackupCatalogEntry)`

SetEntries sets Entries field to given value.


### GetTargets

`func (o *BackupCatalog) GetTargets() []BackupTarget`

GetTargets returns the Targets field if non-nil, zero value otherwise.

### GetTargetsOk

`func (o *BackupCatalog) GetTargetsOk() (*[]BackupTarget, bool)`

GetTargetsOk returns a tuple with the Targets field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargets

`func (o *BackupCatalog) SetTargets(v []BackupTarget)`

SetTargets sets Targets field to given value.


### GetExclusions

`func (o *BackupCatalog) GetExclusions() []BackupExclusion`

GetExclusions returns the Exclusions field if non-nil, zero value otherwise.

### GetExclusionsOk

`func (o *BackupCatalog) GetExclusionsOk() (*[]BackupExclusion, bool)`

GetExclusionsOk returns a tuple with the Exclusions field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExclusions

`func (o *BackupCatalog) SetExclusions(v []BackupExclusion)`

SetExclusions sets Exclusions field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


