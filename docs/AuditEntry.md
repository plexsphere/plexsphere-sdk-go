# AuditEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Seq** | **int64** | Per-Domain monotonic sequence number assigned at append time.  | 
**DomainId** | **string** | Owning Domain. | 
**OccurredAt** | **time.Time** | Server-side timestamp the decision was reached (RFC 3339, UTC).  | 
**Reason** | [**AuditReason**](AuditReason.md) |  | 
**Subject** | [**AuditSubject**](AuditSubject.md) |  | 
**Relation** | **string** | SpiceDB relation label that was checked. | 
**Object** | [**AuditObject**](AuditObject.md) |  | 
**Decision** | [**AuditDecision**](AuditDecision.md) |  | 
**CorrelationId** | **string** | Inbound request correlation id propagated from the transport layer.  | 
**RequestContext** | [**AuditRequestContext**](AuditRequestContext.md) |  | 
**EntryHash** | **string** | &#x60;sha256(prev_hash || sha256(canonical_bytes))&#x60; for this row, lowercase hex.  | 
**PrevHash** | **string** | &#x60;entry_hash&#x60; of the preceding row, or 64 zero hex characters on the genesis row (&#x60;seq&#x3D;1&#x60;).  | 
**ArchiveEtag** | Pointer to **string** | Object-store ETag of the per-Domain mirror copy, or &#x60;null&#x60; until the drain worker has uploaded the row.  | [optional] 
**ArchivedAt** | Pointer to **time.Time** | Server-side timestamp the mirror upload completed, or &#x60;null&#x60; while the row is still in flight.  | [optional] 

## Methods

### NewAuditEntry

`func NewAuditEntry(seq int64, domainId string, occurredAt time.Time, reason AuditReason, subject AuditSubject, relation string, object AuditObject, decision AuditDecision, correlationId string, requestContext AuditRequestContext, entryHash string, prevHash string, ) *AuditEntry`

NewAuditEntry instantiates a new AuditEntry object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditEntryWithDefaults

`func NewAuditEntryWithDefaults() *AuditEntry`

NewAuditEntryWithDefaults instantiates a new AuditEntry object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSeq

`func (o *AuditEntry) GetSeq() int64`

GetSeq returns the Seq field if non-nil, zero value otherwise.

### GetSeqOk

`func (o *AuditEntry) GetSeqOk() (*int64, bool)`

GetSeqOk returns a tuple with the Seq field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSeq

`func (o *AuditEntry) SetSeq(v int64)`

SetSeq sets Seq field to given value.


### GetDomainId

`func (o *AuditEntry) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *AuditEntry) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *AuditEntry) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetOccurredAt

`func (o *AuditEntry) GetOccurredAt() time.Time`

GetOccurredAt returns the OccurredAt field if non-nil, zero value otherwise.

### GetOccurredAtOk

`func (o *AuditEntry) GetOccurredAtOk() (*time.Time, bool)`

GetOccurredAtOk returns a tuple with the OccurredAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOccurredAt

`func (o *AuditEntry) SetOccurredAt(v time.Time)`

SetOccurredAt sets OccurredAt field to given value.


### GetReason

`func (o *AuditEntry) GetReason() AuditReason`

GetReason returns the Reason field if non-nil, zero value otherwise.

### GetReasonOk

`func (o *AuditEntry) GetReasonOk() (*AuditReason, bool)`

GetReasonOk returns a tuple with the Reason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReason

`func (o *AuditEntry) SetReason(v AuditReason)`

SetReason sets Reason field to given value.


### GetSubject

`func (o *AuditEntry) GetSubject() AuditSubject`

GetSubject returns the Subject field if non-nil, zero value otherwise.

### GetSubjectOk

`func (o *AuditEntry) GetSubjectOk() (*AuditSubject, bool)`

GetSubjectOk returns a tuple with the Subject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubject

`func (o *AuditEntry) SetSubject(v AuditSubject)`

SetSubject sets Subject field to given value.


### GetRelation

`func (o *AuditEntry) GetRelation() string`

GetRelation returns the Relation field if non-nil, zero value otherwise.

### GetRelationOk

`func (o *AuditEntry) GetRelationOk() (*string, bool)`

GetRelationOk returns a tuple with the Relation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelation

`func (o *AuditEntry) SetRelation(v string)`

SetRelation sets Relation field to given value.


### GetObject

`func (o *AuditEntry) GetObject() AuditObject`

GetObject returns the Object field if non-nil, zero value otherwise.

### GetObjectOk

`func (o *AuditEntry) GetObjectOk() (*AuditObject, bool)`

GetObjectOk returns a tuple with the Object field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetObject

`func (o *AuditEntry) SetObject(v AuditObject)`

SetObject sets Object field to given value.


### GetDecision

`func (o *AuditEntry) GetDecision() AuditDecision`

GetDecision returns the Decision field if non-nil, zero value otherwise.

### GetDecisionOk

`func (o *AuditEntry) GetDecisionOk() (*AuditDecision, bool)`

GetDecisionOk returns a tuple with the Decision field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDecision

`func (o *AuditEntry) SetDecision(v AuditDecision)`

SetDecision sets Decision field to given value.


### GetCorrelationId

`func (o *AuditEntry) GetCorrelationId() string`

GetCorrelationId returns the CorrelationId field if non-nil, zero value otherwise.

### GetCorrelationIdOk

`func (o *AuditEntry) GetCorrelationIdOk() (*string, bool)`

GetCorrelationIdOk returns a tuple with the CorrelationId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCorrelationId

`func (o *AuditEntry) SetCorrelationId(v string)`

SetCorrelationId sets CorrelationId field to given value.


### GetRequestContext

`func (o *AuditEntry) GetRequestContext() AuditRequestContext`

GetRequestContext returns the RequestContext field if non-nil, zero value otherwise.

### GetRequestContextOk

`func (o *AuditEntry) GetRequestContextOk() (*AuditRequestContext, bool)`

GetRequestContextOk returns a tuple with the RequestContext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRequestContext

`func (o *AuditEntry) SetRequestContext(v AuditRequestContext)`

SetRequestContext sets RequestContext field to given value.


### GetEntryHash

`func (o *AuditEntry) GetEntryHash() string`

GetEntryHash returns the EntryHash field if non-nil, zero value otherwise.

### GetEntryHashOk

`func (o *AuditEntry) GetEntryHashOk() (*string, bool)`

GetEntryHashOk returns a tuple with the EntryHash field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEntryHash

`func (o *AuditEntry) SetEntryHash(v string)`

SetEntryHash sets EntryHash field to given value.


### GetPrevHash

`func (o *AuditEntry) GetPrevHash() string`

GetPrevHash returns the PrevHash field if non-nil, zero value otherwise.

### GetPrevHashOk

`func (o *AuditEntry) GetPrevHashOk() (*string, bool)`

GetPrevHashOk returns a tuple with the PrevHash field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrevHash

`func (o *AuditEntry) SetPrevHash(v string)`

SetPrevHash sets PrevHash field to given value.


### GetArchiveEtag

`func (o *AuditEntry) GetArchiveEtag() string`

GetArchiveEtag returns the ArchiveEtag field if non-nil, zero value otherwise.

### GetArchiveEtagOk

`func (o *AuditEntry) GetArchiveEtagOk() (*string, bool)`

GetArchiveEtagOk returns a tuple with the ArchiveEtag field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetArchiveEtag

`func (o *AuditEntry) SetArchiveEtag(v string)`

SetArchiveEtag sets ArchiveEtag field to given value.

### HasArchiveEtag

`func (o *AuditEntry) HasArchiveEtag() bool`

HasArchiveEtag returns a boolean if a field has been set.

### GetArchivedAt

`func (o *AuditEntry) GetArchivedAt() time.Time`

GetArchivedAt returns the ArchivedAt field if non-nil, zero value otherwise.

### GetArchivedAtOk

`func (o *AuditEntry) GetArchivedAtOk() (*time.Time, bool)`

GetArchivedAtOk returns a tuple with the ArchivedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetArchivedAt

`func (o *AuditEntry) SetArchivedAt(v time.Time)`

SetArchivedAt sets ArchivedAt field to given value.

### HasArchivedAt

`func (o *AuditEntry) HasArchivedAt() bool`

HasArchivedAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


