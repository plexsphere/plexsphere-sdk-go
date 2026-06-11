# CapabilityManifestRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BinaryVersion** | **string** | Human-readable plexd agent version string (e.g. &#x60;plexd-v0.4.2-ge5f3a1c&#x60;). Non-empty after trimming whitespace — the handler rejects an empty value with 400 &#x60;binary_version_empty&#x60;.  | 
**BinaryChecksum** | **string** | SHA-256 digest of the running plexd binary, 32 bytes base64-encoded with standard padding. Anything that does not decode to exactly 32 bytes is rejected with 400 &#x60;binary_checksum_invalid&#x60;.  | 
**SshHostKeyFingerprint** | Pointer to **string** | Optional OpenSSH SHA-256 host-key fingerprint of the running agent, rendered as &#x60;SHA256:&lt;base64&gt;&#x60;. Empty or absent values are accepted; a non-empty value that does not match the canonical form is rejected with 400 &#x60;ssh_host_key_fingerprint_invalid&#x60;. Downstream integrity correlators branch on &#x60;host_key_changed&#x60; in the response to detect a host-key rotation between snapshots.  | [optional] 
**DeclaredHooks** | Pointer to [**[]DeclaredHook**](DeclaredHook.md) | Optional list of hook declarations the agent advertises. Each entry pairs a hook name with the SHA-256 digest of the hook payload so the integrity correlator can detect a hook-content change without re-fetching the payload. The manifest invariants reject duplicate names (400 &#x60;declared_hook_duplicate&#x60;), more than 128 entries (400 &#x60;declared_hooks_too_many&#x60;), and any per-entry violation (400 &#x60;declared_hook_invalid&#x60;).  | [optional] 
**PlexdHooks** | Pointer to [**[]PlexdHook**](PlexdHook.md) | Optional list of Kubernetes PlexdHook custom resources the agent discovered in its cluster and advertises read-only. Distinct from &#x60;declared_hooks&#x60;: each entry carries an OCI image digest, a free-form parameter map, an execution timeout, and a sandbox flag rather than a payload checksum. Discovery is read-only — plexsphere records what plexd observed and never writes PlexdHook objects back. The manifest invariants reject duplicate names (422 &#x60;plexd_hook_duplicate&#x60;), more than 128 entries (422 &#x60;plexd_hooks_too_many&#x60;), and any per-entry violation (422 &#x60;plexd_hook_invalid&#x60;).  | [optional] 

## Methods

### NewCapabilityManifestRequest

`func NewCapabilityManifestRequest(binaryVersion string, binaryChecksum string, ) *CapabilityManifestRequest`

NewCapabilityManifestRequest instantiates a new CapabilityManifestRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCapabilityManifestRequestWithDefaults

`func NewCapabilityManifestRequestWithDefaults() *CapabilityManifestRequest`

NewCapabilityManifestRequestWithDefaults instantiates a new CapabilityManifestRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetBinaryVersion

`func (o *CapabilityManifestRequest) GetBinaryVersion() string`

GetBinaryVersion returns the BinaryVersion field if non-nil, zero value otherwise.

### GetBinaryVersionOk

`func (o *CapabilityManifestRequest) GetBinaryVersionOk() (*string, bool)`

GetBinaryVersionOk returns a tuple with the BinaryVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBinaryVersion

`func (o *CapabilityManifestRequest) SetBinaryVersion(v string)`

SetBinaryVersion sets BinaryVersion field to given value.


### GetBinaryChecksum

`func (o *CapabilityManifestRequest) GetBinaryChecksum() string`

GetBinaryChecksum returns the BinaryChecksum field if non-nil, zero value otherwise.

### GetBinaryChecksumOk

`func (o *CapabilityManifestRequest) GetBinaryChecksumOk() (*string, bool)`

GetBinaryChecksumOk returns a tuple with the BinaryChecksum field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBinaryChecksum

`func (o *CapabilityManifestRequest) SetBinaryChecksum(v string)`

SetBinaryChecksum sets BinaryChecksum field to given value.


### GetSshHostKeyFingerprint

`func (o *CapabilityManifestRequest) GetSshHostKeyFingerprint() string`

GetSshHostKeyFingerprint returns the SshHostKeyFingerprint field if non-nil, zero value otherwise.

### GetSshHostKeyFingerprintOk

`func (o *CapabilityManifestRequest) GetSshHostKeyFingerprintOk() (*string, bool)`

GetSshHostKeyFingerprintOk returns a tuple with the SshHostKeyFingerprint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSshHostKeyFingerprint

`func (o *CapabilityManifestRequest) SetSshHostKeyFingerprint(v string)`

SetSshHostKeyFingerprint sets SshHostKeyFingerprint field to given value.

### HasSshHostKeyFingerprint

`func (o *CapabilityManifestRequest) HasSshHostKeyFingerprint() bool`

HasSshHostKeyFingerprint returns a boolean if a field has been set.

### GetDeclaredHooks

`func (o *CapabilityManifestRequest) GetDeclaredHooks() []DeclaredHook`

GetDeclaredHooks returns the DeclaredHooks field if non-nil, zero value otherwise.

### GetDeclaredHooksOk

`func (o *CapabilityManifestRequest) GetDeclaredHooksOk() (*[]DeclaredHook, bool)`

GetDeclaredHooksOk returns a tuple with the DeclaredHooks field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDeclaredHooks

`func (o *CapabilityManifestRequest) SetDeclaredHooks(v []DeclaredHook)`

SetDeclaredHooks sets DeclaredHooks field to given value.

### HasDeclaredHooks

`func (o *CapabilityManifestRequest) HasDeclaredHooks() bool`

HasDeclaredHooks returns a boolean if a field has been set.

### GetPlexdHooks

`func (o *CapabilityManifestRequest) GetPlexdHooks() []PlexdHook`

GetPlexdHooks returns the PlexdHooks field if non-nil, zero value otherwise.

### GetPlexdHooksOk

`func (o *CapabilityManifestRequest) GetPlexdHooksOk() (*[]PlexdHook, bool)`

GetPlexdHooksOk returns a tuple with the PlexdHooks field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPlexdHooks

`func (o *CapabilityManifestRequest) SetPlexdHooks(v []PlexdHook)`

SetPlexdHooks sets PlexdHooks field to given value.

### HasPlexdHooks

`func (o *CapabilityManifestRequest) HasPlexdHooks() bool`

HasPlexdHooks returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


