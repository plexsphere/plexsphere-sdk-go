# CapabilityManifestResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AcceptedAt** | **time.Time** | Server-side timestamp at which the capability manifest snapshot was committed.  | 
**FieldsChanged** | **[]string** | Alphabetically-sorted list of manifest fields that transitioned versus the prior persisted snapshot. Possible entries: &#x60;binary_version&#x60;, &#x60;binary_checksum&#x60;, &#x60;ssh_host_key_fingerprint&#x60;, &#x60;declared_hooks&#x60;, &#x60;plexd_hooks&#x60;. Empty on an idempotent no-op PUT.  | 
**HostKeyChanged** | **bool** | &#x60;true&#x60; when the SSH host-key fingerprint transitioned versus the prior persisted snapshot (including a transition into or out of the unset state). Always present so downstream security correlators can branch on the flag without parsing &#x60;fields_changed&#x60;.  | 

## Methods

### NewCapabilityManifestResponse

`func NewCapabilityManifestResponse(acceptedAt time.Time, fieldsChanged []string, hostKeyChanged bool, ) *CapabilityManifestResponse`

NewCapabilityManifestResponse instantiates a new CapabilityManifestResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCapabilityManifestResponseWithDefaults

`func NewCapabilityManifestResponseWithDefaults() *CapabilityManifestResponse`

NewCapabilityManifestResponseWithDefaults instantiates a new CapabilityManifestResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAcceptedAt

`func (o *CapabilityManifestResponse) GetAcceptedAt() time.Time`

GetAcceptedAt returns the AcceptedAt field if non-nil, zero value otherwise.

### GetAcceptedAtOk

`func (o *CapabilityManifestResponse) GetAcceptedAtOk() (*time.Time, bool)`

GetAcceptedAtOk returns a tuple with the AcceptedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcceptedAt

`func (o *CapabilityManifestResponse) SetAcceptedAt(v time.Time)`

SetAcceptedAt sets AcceptedAt field to given value.


### GetFieldsChanged

`func (o *CapabilityManifestResponse) GetFieldsChanged() []string`

GetFieldsChanged returns the FieldsChanged field if non-nil, zero value otherwise.

### GetFieldsChangedOk

`func (o *CapabilityManifestResponse) GetFieldsChangedOk() (*[]string, bool)`

GetFieldsChangedOk returns a tuple with the FieldsChanged field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFieldsChanged

`func (o *CapabilityManifestResponse) SetFieldsChanged(v []string)`

SetFieldsChanged sets FieldsChanged field to given value.


### GetHostKeyChanged

`func (o *CapabilityManifestResponse) GetHostKeyChanged() bool`

GetHostKeyChanged returns the HostKeyChanged field if non-nil, zero value otherwise.

### GetHostKeyChangedOk

`func (o *CapabilityManifestResponse) GetHostKeyChangedOk() (*bool, bool)`

GetHostKeyChangedOk returns a tuple with the HostKeyChanged field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHostKeyChanged

`func (o *CapabilityManifestResponse) SetHostKeyChanged(v bool)`

SetHostKeyChanged sets HostKeyChanged field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


