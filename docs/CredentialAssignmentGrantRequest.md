# CredentialAssignmentGrantRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProjectId** | **string** | Identifier of the Project to grant. Must be a non-zero UUID — a malformed value is rejected with &#x60;400 invalid_project_id&#x60;.  | 

## Methods

### NewCredentialAssignmentGrantRequest

`func NewCredentialAssignmentGrantRequest(projectId string, ) *CredentialAssignmentGrantRequest`

NewCredentialAssignmentGrantRequest instantiates a new CredentialAssignmentGrantRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCredentialAssignmentGrantRequestWithDefaults

`func NewCredentialAssignmentGrantRequestWithDefaults() *CredentialAssignmentGrantRequest`

NewCredentialAssignmentGrantRequestWithDefaults instantiates a new CredentialAssignmentGrantRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetProjectId

`func (o *CredentialAssignmentGrantRequest) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *CredentialAssignmentGrantRequest) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *CredentialAssignmentGrantRequest) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


