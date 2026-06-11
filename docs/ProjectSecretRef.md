# ProjectSecretRef

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Secret name within the owning Project. Lower-case, starts with a letter, and is limited to letters, digits, hyphen, and underscore (1 to 63 characters).  | 
**CurrentVersion** | **int32** | The currently-served KV v2 version of the secret — a small, monotonically-increasing integer that starts at 1.  | 

## Methods

### NewProjectSecretRef

`func NewProjectSecretRef(name string, currentVersion int32, ) *ProjectSecretRef`

NewProjectSecretRef instantiates a new ProjectSecretRef object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProjectSecretRefWithDefaults

`func NewProjectSecretRefWithDefaults() *ProjectSecretRef`

NewProjectSecretRefWithDefaults instantiates a new ProjectSecretRef object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *ProjectSecretRef) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *ProjectSecretRef) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *ProjectSecretRef) SetName(v string)`

SetName sets Name field to given value.


### GetCurrentVersion

`func (o *ProjectSecretRef) GetCurrentVersion() int32`

GetCurrentVersion returns the CurrentVersion field if non-nil, zero value otherwise.

### GetCurrentVersionOk

`func (o *ProjectSecretRef) GetCurrentVersionOk() (*int32, bool)`

GetCurrentVersionOk returns a tuple with the CurrentVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCurrentVersion

`func (o *ProjectSecretRef) SetCurrentVersion(v int32)`

SetCurrentVersion sets CurrentVersion field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


