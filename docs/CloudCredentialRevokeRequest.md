# CloudCredentialRevokeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Reason** | **string** | Operator-supplied revocation rationale. Non-empty — whitespace-only is rejected with &#x60;400 invalid_revoke_reason&#x60;.  | 

## Methods

### NewCloudCredentialRevokeRequest

`func NewCloudCredentialRevokeRequest(reason string, ) *CloudCredentialRevokeRequest`

NewCloudCredentialRevokeRequest instantiates a new CloudCredentialRevokeRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudCredentialRevokeRequestWithDefaults

`func NewCloudCredentialRevokeRequestWithDefaults() *CloudCredentialRevokeRequest`

NewCloudCredentialRevokeRequestWithDefaults instantiates a new CloudCredentialRevokeRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetReason

`func (o *CloudCredentialRevokeRequest) GetReason() string`

GetReason returns the Reason field if non-nil, zero value otherwise.

### GetReasonOk

`func (o *CloudCredentialRevokeRequest) GetReasonOk() (*string, bool)`

GetReasonOk returns a tuple with the Reason field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetReason

`func (o *CloudCredentialRevokeRequest) SetReason(v string)`

SetReason sets Reason field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


