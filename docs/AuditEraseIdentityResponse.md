# AuditEraseIdentityResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SubjectPseudonym** | **string** | Per-Domain pseudonym derived from &#x60;identity_id&#x60; (32 bytes, lowercase hex).  | 
**ErasedAt** | **time.Time** | Server-side timestamp the erasure was recorded. Reflects the time the self-audit &#x60;audit.erase-identity&#x60; entry was appended, not the wall-clock time of the original &#x60;audit_subject_pii&#x60; row&#39;s birth.  | 

## Methods

### NewAuditEraseIdentityResponse

`func NewAuditEraseIdentityResponse(subjectPseudonym string, erasedAt time.Time, ) *AuditEraseIdentityResponse`

NewAuditEraseIdentityResponse instantiates a new AuditEraseIdentityResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditEraseIdentityResponseWithDefaults

`func NewAuditEraseIdentityResponseWithDefaults() *AuditEraseIdentityResponse`

NewAuditEraseIdentityResponseWithDefaults instantiates a new AuditEraseIdentityResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSubjectPseudonym

`func (o *AuditEraseIdentityResponse) GetSubjectPseudonym() string`

GetSubjectPseudonym returns the SubjectPseudonym field if non-nil, zero value otherwise.

### GetSubjectPseudonymOk

`func (o *AuditEraseIdentityResponse) GetSubjectPseudonymOk() (*string, bool)`

GetSubjectPseudonymOk returns a tuple with the SubjectPseudonym field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubjectPseudonym

`func (o *AuditEraseIdentityResponse) SetSubjectPseudonym(v string)`

SetSubjectPseudonym sets SubjectPseudonym field to given value.


### GetErasedAt

`func (o *AuditEraseIdentityResponse) GetErasedAt() time.Time`

GetErasedAt returns the ErasedAt field if non-nil, zero value otherwise.

### GetErasedAtOk

`func (o *AuditEraseIdentityResponse) GetErasedAtOk() (*time.Time, bool)`

GetErasedAtOk returns a tuple with the ErasedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetErasedAt

`func (o *AuditEraseIdentityResponse) SetErasedAt(v time.Time)`

SetErasedAt sets ErasedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


