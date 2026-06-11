# AuditSubject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Pseudonym** | **string** | Per-Domain pseudonym of the subject (32 bytes, lowercase hex). Stable for the lifetime of the chain and never reversible to plaintext from the chain alone.  | 
**IdentityIdRef** | Pointer to **string** | Live Identity id the pseudonym maps to, or &#x60;null&#x60; if the mapping has been erased. Cleared by &#x60;EraseIdentityFromAudit&#x60; .  | [optional] 

## Methods

### NewAuditSubject

`func NewAuditSubject(pseudonym string, ) *AuditSubject`

NewAuditSubject instantiates a new AuditSubject object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditSubjectWithDefaults

`func NewAuditSubjectWithDefaults() *AuditSubject`

NewAuditSubjectWithDefaults instantiates a new AuditSubject object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPseudonym

`func (o *AuditSubject) GetPseudonym() string`

GetPseudonym returns the Pseudonym field if non-nil, zero value otherwise.

### GetPseudonymOk

`func (o *AuditSubject) GetPseudonymOk() (*string, bool)`

GetPseudonymOk returns a tuple with the Pseudonym field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPseudonym

`func (o *AuditSubject) SetPseudonym(v string)`

SetPseudonym sets Pseudonym field to given value.


### GetIdentityIdRef

`func (o *AuditSubject) GetIdentityIdRef() string`

GetIdentityIdRef returns the IdentityIdRef field if non-nil, zero value otherwise.

### GetIdentityIdRefOk

`func (o *AuditSubject) GetIdentityIdRefOk() (*string, bool)`

GetIdentityIdRefOk returns a tuple with the IdentityIdRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdentityIdRef

`func (o *AuditSubject) SetIdentityIdRef(v string)`

SetIdentityIdRef sets IdentityIdRef field to given value.

### HasIdentityIdRef

`func (o *AuditSubject) HasIdentityIdRef() bool`

HasIdentityIdRef returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


