# AuditEntryProof

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Entry** | [**AuditEntry**](AuditEntry.md) |  | 
**Proof** | [**AuditEntryProofProof**](AuditEntryProofProof.md) |  | 

## Methods

### NewAuditEntryProof

`func NewAuditEntryProof(entry AuditEntry, proof AuditEntryProofProof, ) *AuditEntryProof`

NewAuditEntryProof instantiates a new AuditEntryProof object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditEntryProofWithDefaults

`func NewAuditEntryProofWithDefaults() *AuditEntryProof`

NewAuditEntryProofWithDefaults instantiates a new AuditEntryProof object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetEntry

`func (o *AuditEntryProof) GetEntry() AuditEntry`

GetEntry returns the Entry field if non-nil, zero value otherwise.

### GetEntryOk

`func (o *AuditEntryProof) GetEntryOk() (*AuditEntry, bool)`

GetEntryOk returns a tuple with the Entry field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEntry

`func (o *AuditEntryProof) SetEntry(v AuditEntry)`

SetEntry sets Entry field to given value.


### GetProof

`func (o *AuditEntryProof) GetProof() AuditEntryProofProof`

GetProof returns the Proof field if non-nil, zero value otherwise.

### GetProofOk

`func (o *AuditEntryProof) GetProofOk() (*AuditEntryProofProof, bool)`

GetProofOk returns a tuple with the Proof field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProof

`func (o *AuditEntryProof) SetProof(v AuditEntryProofProof)`

SetProof sets Proof field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


