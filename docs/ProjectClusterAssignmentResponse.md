# ProjectClusterAssignmentResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProjectId** | **string** | Placed Project identifier (UUIDv7). | 
**ManagementClusterId** | **string** | Identifier of the management cluster the Project is placed onto.  | 
**Region** | **string** | Region the assignment landed in. | 
**NamespaceName** | **string** | Derived per-Project namespace name on the management cluster (&#x60;plexsphere-project-&lt;project-uuid&gt;&#x60;).  | 
**NamespacePhase** | [**NamespacePhase**](NamespacePhase.md) |  | 
**AssignedAt** | **time.Time** | Assignment creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC); bumped on every phase advance.  | 

## Methods

### NewProjectClusterAssignmentResponse

`func NewProjectClusterAssignmentResponse(projectId string, managementClusterId string, region string, namespaceName string, namespacePhase NamespacePhase, assignedAt time.Time, updatedAt time.Time, ) *ProjectClusterAssignmentResponse`

NewProjectClusterAssignmentResponse instantiates a new ProjectClusterAssignmentResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProjectClusterAssignmentResponseWithDefaults

`func NewProjectClusterAssignmentResponseWithDefaults() *ProjectClusterAssignmentResponse`

NewProjectClusterAssignmentResponseWithDefaults instantiates a new ProjectClusterAssignmentResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetProjectId

`func (o *ProjectClusterAssignmentResponse) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *ProjectClusterAssignmentResponse) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *ProjectClusterAssignmentResponse) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetManagementClusterId

`func (o *ProjectClusterAssignmentResponse) GetManagementClusterId() string`

GetManagementClusterId returns the ManagementClusterId field if non-nil, zero value otherwise.

### GetManagementClusterIdOk

`func (o *ProjectClusterAssignmentResponse) GetManagementClusterIdOk() (*string, bool)`

GetManagementClusterIdOk returns a tuple with the ManagementClusterId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetManagementClusterId

`func (o *ProjectClusterAssignmentResponse) SetManagementClusterId(v string)`

SetManagementClusterId sets ManagementClusterId field to given value.


### GetRegion

`func (o *ProjectClusterAssignmentResponse) GetRegion() string`

GetRegion returns the Region field if non-nil, zero value otherwise.

### GetRegionOk

`func (o *ProjectClusterAssignmentResponse) GetRegionOk() (*string, bool)`

GetRegionOk returns a tuple with the Region field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegion

`func (o *ProjectClusterAssignmentResponse) SetRegion(v string)`

SetRegion sets Region field to given value.


### GetNamespaceName

`func (o *ProjectClusterAssignmentResponse) GetNamespaceName() string`

GetNamespaceName returns the NamespaceName field if non-nil, zero value otherwise.

### GetNamespaceNameOk

`func (o *ProjectClusterAssignmentResponse) GetNamespaceNameOk() (*string, bool)`

GetNamespaceNameOk returns a tuple with the NamespaceName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNamespaceName

`func (o *ProjectClusterAssignmentResponse) SetNamespaceName(v string)`

SetNamespaceName sets NamespaceName field to given value.


### GetNamespacePhase

`func (o *ProjectClusterAssignmentResponse) GetNamespacePhase() NamespacePhase`

GetNamespacePhase returns the NamespacePhase field if non-nil, zero value otherwise.

### GetNamespacePhaseOk

`func (o *ProjectClusterAssignmentResponse) GetNamespacePhaseOk() (*NamespacePhase, bool)`

GetNamespacePhaseOk returns a tuple with the NamespacePhase field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNamespacePhase

`func (o *ProjectClusterAssignmentResponse) SetNamespacePhase(v NamespacePhase)`

SetNamespacePhase sets NamespacePhase field to given value.


### GetAssignedAt

`func (o *ProjectClusterAssignmentResponse) GetAssignedAt() time.Time`

GetAssignedAt returns the AssignedAt field if non-nil, zero value otherwise.

### GetAssignedAtOk

`func (o *ProjectClusterAssignmentResponse) GetAssignedAtOk() (*time.Time, bool)`

GetAssignedAtOk returns a tuple with the AssignedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAssignedAt

`func (o *ProjectClusterAssignmentResponse) SetAssignedAt(v time.Time)`

SetAssignedAt sets AssignedAt field to given value.


### GetUpdatedAt

`func (o *ProjectClusterAssignmentResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *ProjectClusterAssignmentResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *ProjectClusterAssignmentResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


