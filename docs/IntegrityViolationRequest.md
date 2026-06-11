# IntegrityViolationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | [**IntegrityViolationRequestKind**](IntegrityViolationRequestKind.md) |  | 
**DetectedBy** | [**IntegrityViolationRequestDetectedBy**](IntegrityViolationRequestDetectedBy.md) |  | 
**ArtifactId** | **string** | Stable identifier of the affected artifact (hook name, binary path label, or host-key file label). Non-empty after trimming whitespace; a violation surfaces as 400 &#x60;integrity_violation_artifact_id_empty&#x60;.  | 
**ObservedChecksum** | Pointer to **string** | SHA-256 digest the agent observed for the artifact, 32 bytes base64-encoded with standard padding. REQUIRED for the &#x60;binary_checksum&#x60; and &#x60;hook_checksum&#x60; kinds; MUST be empty or absent for the &#x60;ssh_host_key&#x60; kind. Anything that does not decode to exactly 32 bytes (when expected) is rejected with 400 &#x60;integrity_violation_checksum_invalid&#x60;. A non-empty value on an &#x60;ssh_host_key&#x60; entry surfaces as 400 &#x60;integrity_violation_kind_mismatch&#x60;.  | [optional] 
**ExpectedChecksum** | Pointer to **string** | Optional SHA-256 digest the agent expected for the artifact, 32 bytes base64-encoded. Accepted only for the &#x60;binary_checksum&#x60; and &#x60;hook_checksum&#x60; kinds. When present, anything that does not decode to exactly 32 bytes is rejected with 400 &#x60;integrity_violation_checksum_invalid&#x60;.  | [optional] 
**ObservedFingerprint** | Pointer to **string** | OpenSSH SHA-256 host-key fingerprint the agent observed, rendered as &#x60;SHA256:&lt;base64&gt;&#x60;. REQUIRED for the &#x60;ssh_host_key&#x60; kind; MUST be empty or absent for the checksum kinds. A non-empty value on a checksum kind surfaces as 400 &#x60;integrity_violation_kind_mismatch&#x60;; a value that does not match the canonical form surfaces as 400 &#x60;integrity_violation_host_key_fingerprint_invalid&#x60;.  | [optional] 
**ExpectedFingerprint** | Pointer to **string** | Optional OpenSSH SHA-256 host-key fingerprint the agent expected, rendered as &#x60;SHA256:&lt;base64&gt;&#x60;. Accepted only for the &#x60;ssh_host_key&#x60; kind. A value that does not match the canonical form is rejected with 400 &#x60;integrity_violation_host_key_fingerprint_invalid&#x60;.  | [optional] 

## Methods

### NewIntegrityViolationRequest

`func NewIntegrityViolationRequest(kind IntegrityViolationRequestKind, detectedBy IntegrityViolationRequestDetectedBy, artifactId string, ) *IntegrityViolationRequest`

NewIntegrityViolationRequest instantiates a new IntegrityViolationRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIntegrityViolationRequestWithDefaults

`func NewIntegrityViolationRequestWithDefaults() *IntegrityViolationRequest`

NewIntegrityViolationRequestWithDefaults instantiates a new IntegrityViolationRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKind

`func (o *IntegrityViolationRequest) GetKind() IntegrityViolationRequestKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *IntegrityViolationRequest) GetKindOk() (*IntegrityViolationRequestKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *IntegrityViolationRequest) SetKind(v IntegrityViolationRequestKind)`

SetKind sets Kind field to given value.


### GetDetectedBy

`func (o *IntegrityViolationRequest) GetDetectedBy() IntegrityViolationRequestDetectedBy`

GetDetectedBy returns the DetectedBy field if non-nil, zero value otherwise.

### GetDetectedByOk

`func (o *IntegrityViolationRequest) GetDetectedByOk() (*IntegrityViolationRequestDetectedBy, bool)`

GetDetectedByOk returns a tuple with the DetectedBy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDetectedBy

`func (o *IntegrityViolationRequest) SetDetectedBy(v IntegrityViolationRequestDetectedBy)`

SetDetectedBy sets DetectedBy field to given value.


### GetArtifactId

`func (o *IntegrityViolationRequest) GetArtifactId() string`

GetArtifactId returns the ArtifactId field if non-nil, zero value otherwise.

### GetArtifactIdOk

`func (o *IntegrityViolationRequest) GetArtifactIdOk() (*string, bool)`

GetArtifactIdOk returns a tuple with the ArtifactId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetArtifactId

`func (o *IntegrityViolationRequest) SetArtifactId(v string)`

SetArtifactId sets ArtifactId field to given value.


### GetObservedChecksum

`func (o *IntegrityViolationRequest) GetObservedChecksum() string`

GetObservedChecksum returns the ObservedChecksum field if non-nil, zero value otherwise.

### GetObservedChecksumOk

`func (o *IntegrityViolationRequest) GetObservedChecksumOk() (*string, bool)`

GetObservedChecksumOk returns a tuple with the ObservedChecksum field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetObservedChecksum

`func (o *IntegrityViolationRequest) SetObservedChecksum(v string)`

SetObservedChecksum sets ObservedChecksum field to given value.

### HasObservedChecksum

`func (o *IntegrityViolationRequest) HasObservedChecksum() bool`

HasObservedChecksum returns a boolean if a field has been set.

### GetExpectedChecksum

`func (o *IntegrityViolationRequest) GetExpectedChecksum() string`

GetExpectedChecksum returns the ExpectedChecksum field if non-nil, zero value otherwise.

### GetExpectedChecksumOk

`func (o *IntegrityViolationRequest) GetExpectedChecksumOk() (*string, bool)`

GetExpectedChecksumOk returns a tuple with the ExpectedChecksum field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpectedChecksum

`func (o *IntegrityViolationRequest) SetExpectedChecksum(v string)`

SetExpectedChecksum sets ExpectedChecksum field to given value.

### HasExpectedChecksum

`func (o *IntegrityViolationRequest) HasExpectedChecksum() bool`

HasExpectedChecksum returns a boolean if a field has been set.

### GetObservedFingerprint

`func (o *IntegrityViolationRequest) GetObservedFingerprint() string`

GetObservedFingerprint returns the ObservedFingerprint field if non-nil, zero value otherwise.

### GetObservedFingerprintOk

`func (o *IntegrityViolationRequest) GetObservedFingerprintOk() (*string, bool)`

GetObservedFingerprintOk returns a tuple with the ObservedFingerprint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetObservedFingerprint

`func (o *IntegrityViolationRequest) SetObservedFingerprint(v string)`

SetObservedFingerprint sets ObservedFingerprint field to given value.

### HasObservedFingerprint

`func (o *IntegrityViolationRequest) HasObservedFingerprint() bool`

HasObservedFingerprint returns a boolean if a field has been set.

### GetExpectedFingerprint

`func (o *IntegrityViolationRequest) GetExpectedFingerprint() string`

GetExpectedFingerprint returns the ExpectedFingerprint field if non-nil, zero value otherwise.

### GetExpectedFingerprintOk

`func (o *IntegrityViolationRequest) GetExpectedFingerprintOk() (*string, bool)`

GetExpectedFingerprintOk returns a tuple with the ExpectedFingerprint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpectedFingerprint

`func (o *IntegrityViolationRequest) SetExpectedFingerprint(v string)`

SetExpectedFingerprint sets ExpectedFingerprint field to given value.

### HasExpectedFingerprint

`func (o *IntegrityViolationRequest) HasExpectedFingerprint() bool`

HasExpectedFingerprint returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


