# BackupTarget

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Plane** | **string** | The plane the objectives apply to. | 
**Rpo** | **string** | Recovery-point objective for the plane. | 
**Rto** | **string** | Recovery-time objective for the plane. | 

## Methods

### NewBackupTarget

`func NewBackupTarget(plane string, rpo string, rto string, ) *BackupTarget`

NewBackupTarget instantiates a new BackupTarget object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBackupTargetWithDefaults

`func NewBackupTargetWithDefaults() *BackupTarget`

NewBackupTargetWithDefaults instantiates a new BackupTarget object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPlane

`func (o *BackupTarget) GetPlane() string`

GetPlane returns the Plane field if non-nil, zero value otherwise.

### GetPlaneOk

`func (o *BackupTarget) GetPlaneOk() (*string, bool)`

GetPlaneOk returns a tuple with the Plane field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPlane

`func (o *BackupTarget) SetPlane(v string)`

SetPlane sets Plane field to given value.


### GetRpo

`func (o *BackupTarget) GetRpo() string`

GetRpo returns the Rpo field if non-nil, zero value otherwise.

### GetRpoOk

`func (o *BackupTarget) GetRpoOk() (*string, bool)`

GetRpoOk returns a tuple with the Rpo field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRpo

`func (o *BackupTarget) SetRpo(v string)`

SetRpo sets Rpo field to given value.


### GetRto

`func (o *BackupTarget) GetRto() string`

GetRto returns the Rto field if non-nil, zero value otherwise.

### GetRtoOk

`func (o *BackupTarget) GetRtoOk() (*string, bool)`

GetRtoOk returns a tuple with the Rto field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRto

`func (o *BackupTarget) SetRto(v string)`

SetRto sets Rto field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


