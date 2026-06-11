# IdentitySummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable principal identifier (UUIDv7). For users this is the User aggregate id; for service identities the ServiceIdentity aggregate id.  | 
**Kind** | [**IdentityKind**](IdentityKind.md) |  | 
**DomainId** | **string** | Owning Domain identifier (UUIDv7). | 
**DisplayName** | **string** | Operator-facing display string. For users this is the IdP- sourced full name; for service identities it is the operator-supplied label.  | 
**ExternalSubjectPseudonym** | **string** | Per-Domain pseudonym of the IdP-side &#x60;external_subject&#x60; (32 bytes, lowercase hex). Always present so the listing surface is queryable without exposing plaintext PII to non-auditor callers.  | 
**LastSignInAt** | Pointer to **time.Time** | Timestamp of the most recent successful sign-in for this principal, or &#x60;null&#x60; when the principal has never signed in (typical for service identities and freshly invited users).  | [optional] 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 

## Methods

### NewIdentitySummary

`func NewIdentitySummary(id string, kind IdentityKind, domainId string, displayName string, externalSubjectPseudonym string, createdAt time.Time, ) *IdentitySummary`

NewIdentitySummary instantiates a new IdentitySummary object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIdentitySummaryWithDefaults

`func NewIdentitySummaryWithDefaults() *IdentitySummary`

NewIdentitySummaryWithDefaults instantiates a new IdentitySummary object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *IdentitySummary) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *IdentitySummary) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *IdentitySummary) SetId(v string)`

SetId sets Id field to given value.


### GetKind

`func (o *IdentitySummary) GetKind() IdentityKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *IdentitySummary) GetKindOk() (*IdentityKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *IdentitySummary) SetKind(v IdentityKind)`

SetKind sets Kind field to given value.


### GetDomainId

`func (o *IdentitySummary) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *IdentitySummary) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *IdentitySummary) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetDisplayName

`func (o *IdentitySummary) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *IdentitySummary) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *IdentitySummary) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetExternalSubjectPseudonym

`func (o *IdentitySummary) GetExternalSubjectPseudonym() string`

GetExternalSubjectPseudonym returns the ExternalSubjectPseudonym field if non-nil, zero value otherwise.

### GetExternalSubjectPseudonymOk

`func (o *IdentitySummary) GetExternalSubjectPseudonymOk() (*string, bool)`

GetExternalSubjectPseudonymOk returns a tuple with the ExternalSubjectPseudonym field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExternalSubjectPseudonym

`func (o *IdentitySummary) SetExternalSubjectPseudonym(v string)`

SetExternalSubjectPseudonym sets ExternalSubjectPseudonym field to given value.


### GetLastSignInAt

`func (o *IdentitySummary) GetLastSignInAt() time.Time`

GetLastSignInAt returns the LastSignInAt field if non-nil, zero value otherwise.

### GetLastSignInAtOk

`func (o *IdentitySummary) GetLastSignInAtOk() (*time.Time, bool)`

GetLastSignInAtOk returns a tuple with the LastSignInAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLastSignInAt

`func (o *IdentitySummary) SetLastSignInAt(v time.Time)`

SetLastSignInAt sets LastSignInAt field to given value.

### HasLastSignInAt

`func (o *IdentitySummary) HasLastSignInAt() bool`

HasLastSignInAt returns a boolean if a field has been set.

### GetCreatedAt

`func (o *IdentitySummary) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *IdentitySummary) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *IdentitySummary) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


