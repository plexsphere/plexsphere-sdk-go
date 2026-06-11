# IdentityDetail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable principal identifier (UUIDv7), matching &#x60;IdentitySummary.id&#x60;.  | 
**Kind** | [**IdentityKind**](IdentityKind.md) |  | 
**DomainId** | **string** | Owning Domain identifier (UUIDv7). | 
**DisplayName** | **string** | Operator-facing display string, matching &#x60;IdentitySummary.display_name&#x60;.  | 
**ExternalSubjectPseudonym** | **string** | Per-Domain pseudonym of the IdP-side &#x60;external_subject&#x60; (32 bytes, lowercase hex), matching &#x60;IdentitySummary.external_subject_pseudonym&#x60;.  | 
**ExternalSubject** | Pointer to **string** | Plaintext IdP-side &#x60;external_subject&#x60; (the OIDC &#x60;sub&#x60; claim or service identity token name). Populated ONLY for callers who carry the &#x60;auditor&#x60; ReBAC relation on the addressed Domain; non-auditor callers see this field elided from the response body so the wire bytes never carry raw PII to a &#x60;read&#x60;-only caller.  | [optional] 
**Email** | Pointer to **string** | Plaintext IdP-side email address. Populated ONLY for callers who carry the &#x60;auditor&#x60; ReBAC relation on the addressed Domain. Service identities do not carry an &#x60;email&#x60; value and the field is omitted in that case regardless of the caller&#39;s relation.  | [optional] 
**LastSignInAt** | Pointer to **time.Time** | Timestamp of the most recent successful sign-in, matching &#x60;IdentitySummary.last_sign_in_at&#x60; semantics.  | [optional] 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). Bumped by every aggregate mutator, including &#x60;last_sign_in_at&#x60; updates from the OIDC sign-in callback.  | 

## Methods

### NewIdentityDetail

`func NewIdentityDetail(id string, kind IdentityKind, domainId string, displayName string, externalSubjectPseudonym string, createdAt time.Time, updatedAt time.Time, ) *IdentityDetail`

NewIdentityDetail instantiates a new IdentityDetail object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIdentityDetailWithDefaults

`func NewIdentityDetailWithDefaults() *IdentityDetail`

NewIdentityDetailWithDefaults instantiates a new IdentityDetail object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *IdentityDetail) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *IdentityDetail) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *IdentityDetail) SetId(v string)`

SetId sets Id field to given value.


### GetKind

`func (o *IdentityDetail) GetKind() IdentityKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *IdentityDetail) GetKindOk() (*IdentityKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *IdentityDetail) SetKind(v IdentityKind)`

SetKind sets Kind field to given value.


### GetDomainId

`func (o *IdentityDetail) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *IdentityDetail) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *IdentityDetail) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetDisplayName

`func (o *IdentityDetail) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *IdentityDetail) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *IdentityDetail) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetExternalSubjectPseudonym

`func (o *IdentityDetail) GetExternalSubjectPseudonym() string`

GetExternalSubjectPseudonym returns the ExternalSubjectPseudonym field if non-nil, zero value otherwise.

### GetExternalSubjectPseudonymOk

`func (o *IdentityDetail) GetExternalSubjectPseudonymOk() (*string, bool)`

GetExternalSubjectPseudonymOk returns a tuple with the ExternalSubjectPseudonym field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExternalSubjectPseudonym

`func (o *IdentityDetail) SetExternalSubjectPseudonym(v string)`

SetExternalSubjectPseudonym sets ExternalSubjectPseudonym field to given value.


### GetExternalSubject

`func (o *IdentityDetail) GetExternalSubject() string`

GetExternalSubject returns the ExternalSubject field if non-nil, zero value otherwise.

### GetExternalSubjectOk

`func (o *IdentityDetail) GetExternalSubjectOk() (*string, bool)`

GetExternalSubjectOk returns a tuple with the ExternalSubject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExternalSubject

`func (o *IdentityDetail) SetExternalSubject(v string)`

SetExternalSubject sets ExternalSubject field to given value.

### HasExternalSubject

`func (o *IdentityDetail) HasExternalSubject() bool`

HasExternalSubject returns a boolean if a field has been set.

### GetEmail

`func (o *IdentityDetail) GetEmail() string`

GetEmail returns the Email field if non-nil, zero value otherwise.

### GetEmailOk

`func (o *IdentityDetail) GetEmailOk() (*string, bool)`

GetEmailOk returns a tuple with the Email field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEmail

`func (o *IdentityDetail) SetEmail(v string)`

SetEmail sets Email field to given value.

### HasEmail

`func (o *IdentityDetail) HasEmail() bool`

HasEmail returns a boolean if a field has been set.

### GetLastSignInAt

`func (o *IdentityDetail) GetLastSignInAt() time.Time`

GetLastSignInAt returns the LastSignInAt field if non-nil, zero value otherwise.

### GetLastSignInAtOk

`func (o *IdentityDetail) GetLastSignInAtOk() (*time.Time, bool)`

GetLastSignInAtOk returns a tuple with the LastSignInAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLastSignInAt

`func (o *IdentityDetail) SetLastSignInAt(v time.Time)`

SetLastSignInAt sets LastSignInAt field to given value.

### HasLastSignInAt

`func (o *IdentityDetail) HasLastSignInAt() bool`

HasLastSignInAt returns a boolean if a field has been set.

### GetCreatedAt

`func (o *IdentityDetail) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *IdentityDetail) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *IdentityDetail) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *IdentityDetail) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *IdentityDetail) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *IdentityDetail) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


