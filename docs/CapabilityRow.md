# CapabilityRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NodeId** | **string** | Node the capability row describes (UUIDv7). | 
**DomainId** | **string** | Owning Domain (UUIDv7) — the residency pivot the per-row visibility filter authorises against.  | 
**BinaryVersion** | **string** | Reported plexd agent version string of the Node&#39;s running binary.  | 
**BinaryChecksum** | Pointer to **string** | SHA-256 digest of the running binary, 32 bytes base64-encoded with standard padding. Absent when the Node has not yet reported a checksum.  | [optional] 
**Status** | [**CapabilityStatus**](CapabilityStatus.md) |  | 
**ReportedAt** | **time.Time** | Timestamp at which the capability manifest snapshot was last reported (UTC).  | 

## Methods

### NewCapabilityRow

`func NewCapabilityRow(nodeId string, domainId string, binaryVersion string, status CapabilityStatus, reportedAt time.Time, ) *CapabilityRow`

NewCapabilityRow instantiates a new CapabilityRow object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCapabilityRowWithDefaults

`func NewCapabilityRowWithDefaults() *CapabilityRow`

NewCapabilityRowWithDefaults instantiates a new CapabilityRow object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNodeId

`func (o *CapabilityRow) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *CapabilityRow) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *CapabilityRow) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetDomainId

`func (o *CapabilityRow) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *CapabilityRow) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *CapabilityRow) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetBinaryVersion

`func (o *CapabilityRow) GetBinaryVersion() string`

GetBinaryVersion returns the BinaryVersion field if non-nil, zero value otherwise.

### GetBinaryVersionOk

`func (o *CapabilityRow) GetBinaryVersionOk() (*string, bool)`

GetBinaryVersionOk returns a tuple with the BinaryVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBinaryVersion

`func (o *CapabilityRow) SetBinaryVersion(v string)`

SetBinaryVersion sets BinaryVersion field to given value.


### GetBinaryChecksum

`func (o *CapabilityRow) GetBinaryChecksum() string`

GetBinaryChecksum returns the BinaryChecksum field if non-nil, zero value otherwise.

### GetBinaryChecksumOk

`func (o *CapabilityRow) GetBinaryChecksumOk() (*string, bool)`

GetBinaryChecksumOk returns a tuple with the BinaryChecksum field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBinaryChecksum

`func (o *CapabilityRow) SetBinaryChecksum(v string)`

SetBinaryChecksum sets BinaryChecksum field to given value.

### HasBinaryChecksum

`func (o *CapabilityRow) HasBinaryChecksum() bool`

HasBinaryChecksum returns a boolean if a field has been set.

### GetStatus

`func (o *CapabilityRow) GetStatus() CapabilityStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *CapabilityRow) GetStatusOk() (*CapabilityStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *CapabilityRow) SetStatus(v CapabilityStatus)`

SetStatus sets Status field to given value.


### GetReportedAt

`func (o *CapabilityRow) GetReportedAt() time.Time`

GetReportedAt returns the ReportedAt field if non-nil, zero value otherwise.

### GetReportedAtOk

`func (o *CapabilityRow) GetReportedAtOk() (*time.Time, bool)`

GetReportedAtOk returns a tuple with the ReportedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReportedAt

`func (o *CapabilityRow) SetReportedAt(v time.Time)`

SetReportedAt sets ReportedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


