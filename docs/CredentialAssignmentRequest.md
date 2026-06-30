# CredentialAssignmentRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CloudCredentialId** | Pointer to **string** | Identifier of the Cloud Credential to bind directly. Must be a non-zero UUID — a malformed value is rejected with &#x60;400 invalid_cloud_credential_id&#x60;. Mutually exclusive with &#x60;cloud_id&#x60;.  | [optional] 
**CloudId** | Pointer to **string** | Identifier of the Cloud whose newest eligible credential the system auto-selects and binds. Must be a non-zero UUID — a malformed value is rejected with &#x60;400 invalid_cloud_id&#x60;. Mutually exclusive with &#x60;cloud_credential_id&#x60;.  | [optional] 

## Methods

### NewCredentialAssignmentRequest

`func NewCredentialAssignmentRequest() *CredentialAssignmentRequest`

NewCredentialAssignmentRequest instantiates a new CredentialAssignmentRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCredentialAssignmentRequestWithDefaults

`func NewCredentialAssignmentRequestWithDefaults() *CredentialAssignmentRequest`

NewCredentialAssignmentRequestWithDefaults instantiates a new CredentialAssignmentRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCloudCredentialId

`func (o *CredentialAssignmentRequest) GetCloudCredentialId() string`

GetCloudCredentialId returns the CloudCredentialId field if non-nil, zero value otherwise.

### GetCloudCredentialIdOk

`func (o *CredentialAssignmentRequest) GetCloudCredentialIdOk() (*string, bool)`

GetCloudCredentialIdOk returns a tuple with the CloudCredentialId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudCredentialId

`func (o *CredentialAssignmentRequest) SetCloudCredentialId(v string)`

SetCloudCredentialId sets CloudCredentialId field to given value.

### HasCloudCredentialId

`func (o *CredentialAssignmentRequest) HasCloudCredentialId() bool`

HasCloudCredentialId returns a boolean if a field has been set.

### GetCloudId

`func (o *CredentialAssignmentRequest) GetCloudId() string`

GetCloudId returns the CloudId field if non-nil, zero value otherwise.

### GetCloudIdOk

`func (o *CredentialAssignmentRequest) GetCloudIdOk() (*string, bool)`

GetCloudIdOk returns a tuple with the CloudId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudId

`func (o *CredentialAssignmentRequest) SetCloudId(v string)`

SetCloudId sets CloudId field to given value.

### HasCloudId

`func (o *CredentialAssignmentRequest) HasCloudId() bool`

HasCloudId returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


