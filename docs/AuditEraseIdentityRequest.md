# AuditEraseIdentityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IdentityId** | **string** | Identity whose &#x60;audit_subject_pii&#x60; mapping must be purged from the addressed Domain. The pseudonym is derived server-side from &#x60;(domain_id, identity_id)&#x60; and the per-Domain pepper; clients never compute it themselves .  | 

## Methods

### NewAuditEraseIdentityRequest

`func NewAuditEraseIdentityRequest(identityId string, ) *AuditEraseIdentityRequest`

NewAuditEraseIdentityRequest instantiates a new AuditEraseIdentityRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditEraseIdentityRequestWithDefaults

`func NewAuditEraseIdentityRequestWithDefaults() *AuditEraseIdentityRequest`

NewAuditEraseIdentityRequestWithDefaults instantiates a new AuditEraseIdentityRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetIdentityId

`func (o *AuditEraseIdentityRequest) GetIdentityId() string`

GetIdentityId returns the IdentityId field if non-nil, zero value otherwise.

### GetIdentityIdOk

`func (o *AuditEraseIdentityRequest) GetIdentityIdOk() (*string, bool)`

GetIdentityIdOk returns a tuple with the IdentityId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetIdentityId

`func (o *AuditEraseIdentityRequest) SetIdentityId(v string)`

SetIdentityId sets IdentityId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


