# IntegrityViolationRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Integrity-violation identifier (UUIDv7). | 
**NodeId** | **string** | Node that reported the violation (UUIDv7). | 
**DomainId** | **string** | Owning Domain (UUIDv7) — the residency pivot the per-row visibility filter authorises against.  | 
**Kind** | [**IntegrityViolationKind**](IntegrityViolationKind.md) |  | 
**Status** | [**IntegrityViolationStatus**](IntegrityViolationStatus.md) |  | 
**ArtifactId** | **string** | Stable identifier of the affected artifact (hook name, binary path label, or host-key file label).  | 
**DetectedAt** | **time.Time** | Timestamp the agent detected the violation (UTC). | 
**AcknowledgedAt** | Pointer to **time.Time** | Timestamp an operator acknowledged the violation (UTC). &#x60;null&#x60; or omitted while the violation is still &#x60;open&#x60;.  | [optional] 
**AcknowledgedBySubject** | Pointer to **string** | Subject string of the operator that acknowledged the violation. &#x60;null&#x60; or omitted while the violation is still &#x60;open&#x60;.  | [optional] 
**AcknowledgeReason** | Pointer to **string** | Free-text rationale recorded with the acknowledgement. &#x60;null&#x60; or omitted while the violation is still &#x60;open&#x60;.  | [optional] 

## Methods

### NewIntegrityViolationRow

`func NewIntegrityViolationRow(id string, nodeId string, domainId string, kind IntegrityViolationKind, status IntegrityViolationStatus, artifactId string, detectedAt time.Time, ) *IntegrityViolationRow`

NewIntegrityViolationRow instantiates a new IntegrityViolationRow object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIntegrityViolationRowWithDefaults

`func NewIntegrityViolationRowWithDefaults() *IntegrityViolationRow`

NewIntegrityViolationRowWithDefaults instantiates a new IntegrityViolationRow object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *IntegrityViolationRow) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *IntegrityViolationRow) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *IntegrityViolationRow) SetId(v string)`

SetId sets Id field to given value.


### GetNodeId

`func (o *IntegrityViolationRow) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *IntegrityViolationRow) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *IntegrityViolationRow) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetDomainId

`func (o *IntegrityViolationRow) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *IntegrityViolationRow) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *IntegrityViolationRow) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetKind

`func (o *IntegrityViolationRow) GetKind() IntegrityViolationKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *IntegrityViolationRow) GetKindOk() (*IntegrityViolationKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *IntegrityViolationRow) SetKind(v IntegrityViolationKind)`

SetKind sets Kind field to given value.


### GetStatus

`func (o *IntegrityViolationRow) GetStatus() IntegrityViolationStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *IntegrityViolationRow) GetStatusOk() (*IntegrityViolationStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *IntegrityViolationRow) SetStatus(v IntegrityViolationStatus)`

SetStatus sets Status field to given value.


### GetArtifactId

`func (o *IntegrityViolationRow) GetArtifactId() string`

GetArtifactId returns the ArtifactId field if non-nil, zero value otherwise.

### GetArtifactIdOk

`func (o *IntegrityViolationRow) GetArtifactIdOk() (*string, bool)`

GetArtifactIdOk returns a tuple with the ArtifactId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetArtifactId

`func (o *IntegrityViolationRow) SetArtifactId(v string)`

SetArtifactId sets ArtifactId field to given value.


### GetDetectedAt

`func (o *IntegrityViolationRow) GetDetectedAt() time.Time`

GetDetectedAt returns the DetectedAt field if non-nil, zero value otherwise.

### GetDetectedAtOk

`func (o *IntegrityViolationRow) GetDetectedAtOk() (*time.Time, bool)`

GetDetectedAtOk returns a tuple with the DetectedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDetectedAt

`func (o *IntegrityViolationRow) SetDetectedAt(v time.Time)`

SetDetectedAt sets DetectedAt field to given value.


### GetAcknowledgedAt

`func (o *IntegrityViolationRow) GetAcknowledgedAt() time.Time`

GetAcknowledgedAt returns the AcknowledgedAt field if non-nil, zero value otherwise.

### GetAcknowledgedAtOk

`func (o *IntegrityViolationRow) GetAcknowledgedAtOk() (*time.Time, bool)`

GetAcknowledgedAtOk returns a tuple with the AcknowledgedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcknowledgedAt

`func (o *IntegrityViolationRow) SetAcknowledgedAt(v time.Time)`

SetAcknowledgedAt sets AcknowledgedAt field to given value.

### HasAcknowledgedAt

`func (o *IntegrityViolationRow) HasAcknowledgedAt() bool`

HasAcknowledgedAt returns a boolean if a field has been set.

### GetAcknowledgedBySubject

`func (o *IntegrityViolationRow) GetAcknowledgedBySubject() string`

GetAcknowledgedBySubject returns the AcknowledgedBySubject field if non-nil, zero value otherwise.

### GetAcknowledgedBySubjectOk

`func (o *IntegrityViolationRow) GetAcknowledgedBySubjectOk() (*string, bool)`

GetAcknowledgedBySubjectOk returns a tuple with the AcknowledgedBySubject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcknowledgedBySubject

`func (o *IntegrityViolationRow) SetAcknowledgedBySubject(v string)`

SetAcknowledgedBySubject sets AcknowledgedBySubject field to given value.

### HasAcknowledgedBySubject

`func (o *IntegrityViolationRow) HasAcknowledgedBySubject() bool`

HasAcknowledgedBySubject returns a boolean if a field has been set.

### GetAcknowledgeReason

`func (o *IntegrityViolationRow) GetAcknowledgeReason() string`

GetAcknowledgeReason returns the AcknowledgeReason field if non-nil, zero value otherwise.

### GetAcknowledgeReasonOk

`func (o *IntegrityViolationRow) GetAcknowledgeReasonOk() (*string, bool)`

GetAcknowledgeReasonOk returns a tuple with the AcknowledgeReason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcknowledgeReason

`func (o *IntegrityViolationRow) SetAcknowledgeReason(v string)`

SetAcknowledgeReason sets AcknowledgeReason field to given value.

### HasAcknowledgeReason

`func (o *IntegrityViolationRow) HasAcknowledgeReason() bool`

HasAcknowledgeReason returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


