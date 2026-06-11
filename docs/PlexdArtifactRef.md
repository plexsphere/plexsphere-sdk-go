# PlexdArtifactRef

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Version** | **string** | Upstream plexd release tag the registry indexes. | 
**SupportStatus** | [**PlexdArtifactRefSupportStatus**](PlexdArtifactRefSupportStatus.md) |  | 
**Verdict** | [**PlexdArtifactRefVerdict**](PlexdArtifactRefVerdict.md) |  | 
**Architectures** | [**[]PlexdArtifactArch**](PlexdArtifactArch.md) | The per-architecture builds of this release with their recorded SHA-256 checksums.  | 
**CreatedAt** | Pointer to **time.Time** | Timestamp the registry first indexed this release line (UTC). Absent when the registry does not record it.  | [optional] 
**UpdatedAt** | Pointer to **time.Time** | Timestamp the registry last refreshed this release line (UTC). Absent when the registry does not record it.  | [optional] 

## Methods

### NewPlexdArtifactRef

`func NewPlexdArtifactRef(version string, supportStatus PlexdArtifactRefSupportStatus, verdict PlexdArtifactRefVerdict, architectures []PlexdArtifactArch, ) *PlexdArtifactRef`

NewPlexdArtifactRef instantiates a new PlexdArtifactRef object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPlexdArtifactRefWithDefaults

`func NewPlexdArtifactRefWithDefaults() *PlexdArtifactRef`

NewPlexdArtifactRefWithDefaults instantiates a new PlexdArtifactRef object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetVersion

`func (o *PlexdArtifactRef) GetVersion() string`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *PlexdArtifactRef) GetVersionOk() (*string, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *PlexdArtifactRef) SetVersion(v string)`

SetVersion sets Version field to given value.


### GetSupportStatus

`func (o *PlexdArtifactRef) GetSupportStatus() PlexdArtifactRefSupportStatus`

GetSupportStatus returns the SupportStatus field if non-nil, zero value otherwise.

### GetSupportStatusOk

`func (o *PlexdArtifactRef) GetSupportStatusOk() (*PlexdArtifactRefSupportStatus, bool)`

GetSupportStatusOk returns a tuple with the SupportStatus field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSupportStatus

`func (o *PlexdArtifactRef) SetSupportStatus(v PlexdArtifactRefSupportStatus)`

SetSupportStatus sets SupportStatus field to given value.


### GetVerdict

`func (o *PlexdArtifactRef) GetVerdict() PlexdArtifactRefVerdict`

GetVerdict returns the Verdict field if non-nil, zero value otherwise.

### GetVerdictOk

`func (o *PlexdArtifactRef) GetVerdictOk() (*PlexdArtifactRefVerdict, bool)`

GetVerdictOk returns a tuple with the Verdict field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVerdict

`func (o *PlexdArtifactRef) SetVerdict(v PlexdArtifactRefVerdict)`

SetVerdict sets Verdict field to given value.


### GetArchitectures

`func (o *PlexdArtifactRef) GetArchitectures() []PlexdArtifactArch`

GetArchitectures returns the Architectures field if non-nil, zero value otherwise.

### GetArchitecturesOk

`func (o *PlexdArtifactRef) GetArchitecturesOk() (*[]PlexdArtifactArch, bool)`

GetArchitecturesOk returns a tuple with the Architectures field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetArchitectures

`func (o *PlexdArtifactRef) SetArchitectures(v []PlexdArtifactArch)`

SetArchitectures sets Architectures field to given value.


### GetCreatedAt

`func (o *PlexdArtifactRef) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *PlexdArtifactRef) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *PlexdArtifactRef) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.

### HasCreatedAt

`func (o *PlexdArtifactRef) HasCreatedAt() bool`

HasCreatedAt returns a boolean if a field has been set.

### GetUpdatedAt

`func (o *PlexdArtifactRef) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *PlexdArtifactRef) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *PlexdArtifactRef) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.

### HasUpdatedAt

`func (o *PlexdArtifactRef) HasUpdatedAt() bool`

HasUpdatedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


