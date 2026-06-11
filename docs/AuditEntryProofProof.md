# AuditEntryProofProof

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PrevHash** | **string** | Same value as &#x60;entry.prev_hash&#x60; (lowercase hex). | 
**EntryHash** | **string** | Same value as &#x60;entry.entry_hash&#x60; (lowercase hex). | 
**CanonicalBytes** | **string** | Canonical-encoded chain input for this row, base64- encoded. Re-hashing &#x60;sha256(prev_hash || sha256(canonical_bytes))&#x60; reproduces &#x60;entry_hash&#x60; byte-for-byte.  | 

## Methods

### NewAuditEntryProofProof

`func NewAuditEntryProofProof(prevHash string, entryHash string, canonicalBytes string, ) *AuditEntryProofProof`

NewAuditEntryProofProof instantiates a new AuditEntryProofProof object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditEntryProofProofWithDefaults

`func NewAuditEntryProofProofWithDefaults() *AuditEntryProofProof`

NewAuditEntryProofProofWithDefaults instantiates a new AuditEntryProofProof object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPrevHash

`func (o *AuditEntryProofProof) GetPrevHash() string`

GetPrevHash returns the PrevHash field if non-nil, zero value otherwise.

### GetPrevHashOk

`func (o *AuditEntryProofProof) GetPrevHashOk() (*string, bool)`

GetPrevHashOk returns a tuple with the PrevHash field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrevHash

`func (o *AuditEntryProofProof) SetPrevHash(v string)`

SetPrevHash sets PrevHash field to given value.


### GetEntryHash

`func (o *AuditEntryProofProof) GetEntryHash() string`

GetEntryHash returns the EntryHash field if non-nil, zero value otherwise.

### GetEntryHashOk

`func (o *AuditEntryProofProof) GetEntryHashOk() (*string, bool)`

GetEntryHashOk returns a tuple with the EntryHash field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEntryHash

`func (o *AuditEntryProofProof) SetEntryHash(v string)`

SetEntryHash sets EntryHash field to given value.


### GetCanonicalBytes

`func (o *AuditEntryProofProof) GetCanonicalBytes() string`

GetCanonicalBytes returns the CanonicalBytes field if non-nil, zero value otherwise.

### GetCanonicalBytesOk

`func (o *AuditEntryProofProof) GetCanonicalBytesOk() (*string, bool)`

GetCanonicalBytesOk returns a tuple with the CanonicalBytes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCanonicalBytes

`func (o *AuditEntryProofProof) SetCanonicalBytes(v string)`

SetCanonicalBytes sets CanonicalBytes field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


