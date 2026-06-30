# CloudAssignmentGrantRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProjectId** | **string** | Identifier of the Project to grant. Must be a non-zero UUID — a malformed value is rejected with &#x60;400 invalid_project_id&#x60;.  | 

## Methods

### NewCloudAssignmentGrantRequest

`func NewCloudAssignmentGrantRequest(projectId string, ) *CloudAssignmentGrantRequest`

NewCloudAssignmentGrantRequest instantiates a new CloudAssignmentGrantRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudAssignmentGrantRequestWithDefaults

`func NewCloudAssignmentGrantRequestWithDefaults() *CloudAssignmentGrantRequest`

NewCloudAssignmentGrantRequestWithDefaults instantiates a new CloudAssignmentGrantRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetProjectId

`func (o *CloudAssignmentGrantRequest) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *CloudAssignmentGrantRequest) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *CloudAssignmentGrantRequest) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


