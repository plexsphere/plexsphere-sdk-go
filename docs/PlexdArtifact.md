# PlexdArtifact

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Version** | **string** | Upstream plexd release tag the registry indexes (for example a semver tag such as &#x60;v1.4.2&#x60;).  | 
**SupportStatus** | [**PlexdArtifactSupportStatus**](PlexdArtifactSupportStatus.md) |  | 
**Verdict** | [**PlexdArtifactVerdict**](PlexdArtifactVerdict.md) |  | 
**Architectures** | [**[]PlexdArtifactArch**](PlexdArtifactArch.md) | The per-architecture builds of this release. At least one build is always present, and no two builds share an architecture.  | 

## Methods

### NewPlexdArtifact

`func NewPlexdArtifact(version string, supportStatus PlexdArtifactSupportStatus, verdict PlexdArtifactVerdict, architectures []PlexdArtifactArch, ) *PlexdArtifact`

NewPlexdArtifact instantiates a new PlexdArtifact object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPlexdArtifactWithDefaults

`func NewPlexdArtifactWithDefaults() *PlexdArtifact`

NewPlexdArtifactWithDefaults instantiates a new PlexdArtifact object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetVersion

`func (o *PlexdArtifact) GetVersion() string`

GetVersion returns the Version field if non-nil, zero value otherwise.

### GetVersionOk

`func (o *PlexdArtifact) GetVersionOk() (*string, bool)`

GetVersionOk returns a tuple with the Version field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVersion

`func (o *PlexdArtifact) SetVersion(v string)`

SetVersion sets Version field to given value.


### GetSupportStatus

`func (o *PlexdArtifact) GetSupportStatus() PlexdArtifactSupportStatus`

GetSupportStatus returns the SupportStatus field if non-nil, zero value otherwise.

### GetSupportStatusOk

`func (o *PlexdArtifact) GetSupportStatusOk() (*PlexdArtifactSupportStatus, bool)`

GetSupportStatusOk returns a tuple with the SupportStatus field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSupportStatus

`func (o *PlexdArtifact) SetSupportStatus(v PlexdArtifactSupportStatus)`

SetSupportStatus sets SupportStatus field to given value.


### GetVerdict

`func (o *PlexdArtifact) GetVerdict() PlexdArtifactVerdict`

GetVerdict returns the Verdict field if non-nil, zero value otherwise.

### GetVerdictOk

`func (o *PlexdArtifact) GetVerdictOk() (*PlexdArtifactVerdict, bool)`

GetVerdictOk returns a tuple with the Verdict field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVerdict

`func (o *PlexdArtifact) SetVerdict(v PlexdArtifactVerdict)`

SetVerdict sets Verdict field to given value.


### GetArchitectures

`func (o *PlexdArtifact) GetArchitectures() []PlexdArtifactArch`

GetArchitectures returns the Architectures field if non-nil, zero value otherwise.

### GetArchitecturesOk

`func (o *PlexdArtifact) GetArchitecturesOk() (*[]PlexdArtifactArch, bool)`

GetArchitecturesOk returns a tuple with the Architectures field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetArchitectures

`func (o *PlexdArtifact) SetArchitectures(v []PlexdArtifactArch)`

SetArchitectures sets Architectures field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


