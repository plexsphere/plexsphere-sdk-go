# PlexdArtifactArch

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Architecture** | **string** | Target CPU architecture of the build (for example &#x60;amd64&#x60; or &#x60;arm64&#x60;). The set is owned by the upstream release pipeline, not by plexsphere, so it is not constrained to a closed enum.  | 
**Checksum** | **string** | Recorded SHA-256 checksum of the build&#39;s plexd binary — the raw 32-byte digest, hex-encoded as 64 lowercase hex characters.  | 

## Methods

### NewPlexdArtifactArch

`func NewPlexdArtifactArch(architecture string, checksum string, ) *PlexdArtifactArch`

NewPlexdArtifactArch instantiates a new PlexdArtifactArch object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPlexdArtifactArchWithDefaults

`func NewPlexdArtifactArchWithDefaults() *PlexdArtifactArch`

NewPlexdArtifactArchWithDefaults instantiates a new PlexdArtifactArch object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetArchitecture

`func (o *PlexdArtifactArch) GetArchitecture() string`

GetArchitecture returns the Architecture field if non-nil, zero value otherwise.

### GetArchitectureOk

`func (o *PlexdArtifactArch) GetArchitectureOk() (*string, bool)`

GetArchitectureOk returns a tuple with the Architecture field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetArchitecture

`func (o *PlexdArtifactArch) SetArchitecture(v string)`

SetArchitecture sets Architecture field to given value.


### GetChecksum

`func (o *PlexdArtifactArch) GetChecksum() string`

GetChecksum returns the Checksum field if non-nil, zero value otherwise.

### GetChecksumOk

`func (o *PlexdArtifactArch) GetChecksumOk() (*string, bool)`

GetChecksumOk returns a tuple with the Checksum field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChecksum

`func (o *PlexdArtifactArch) SetChecksum(v string)`

SetChecksum sets Checksum field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


