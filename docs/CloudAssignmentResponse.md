# CloudAssignmentResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Cloud Assignment identifier (UUIDv7). | 
**ProjectId** | **string** | Identifier of the consuming Project the Cloud is assigned to.  | 
**CloudId** | **string** | Identifier of the Cloud being made usable in the Project — the residency pivot the operator ReBAC gate authorises against.  | 
**State** | **string** | Lifecycle state of a Cloud Assignment, one of &#x60;requested&#x60;, &#x60;approved&#x60;, &#x60;rejected&#x60;, or &#x60;revoked&#x60;. &#x60;requested&#x60; is the opening state of a project-initiated request; &#x60;approved&#x60; materialises the &#x60;cloud#uses&#x60; binding so the Cloud is usable in the Project; &#x60;rejected&#x60; closes an unapproved request; &#x60;revoked&#x60; tears down a previously approved binding. An operator grant creates the assignment directly in the &#x60;approved&#x60; state. The state is a stored column advanced only by the application service&#39;s transition rules.  | 
**Materialised** | **bool** | Whether the assignment&#39;s &#x60;cloud#uses&#x60; binding is currently live. &#x60;true&#x60; only while the assignment is in the &#x60;approved&#x60; state; &#x60;false&#x60; for &#x60;requested&#x60;, &#x60;rejected&#x60;, and &#x60;revoked&#x60;.  | 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). Bumped by every lifecycle transition — approve, reject, revoke.  | 

## Methods

### NewCloudAssignmentResponse

`func NewCloudAssignmentResponse(id string, projectId string, cloudId string, state string, materialised bool, createdAt time.Time, updatedAt time.Time, ) *CloudAssignmentResponse`

NewCloudAssignmentResponse instantiates a new CloudAssignmentResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudAssignmentResponseWithDefaults

`func NewCloudAssignmentResponseWithDefaults() *CloudAssignmentResponse`

NewCloudAssignmentResponseWithDefaults instantiates a new CloudAssignmentResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *CloudAssignmentResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *CloudAssignmentResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *CloudAssignmentResponse) SetId(v string)`

SetId sets Id field to given value.


### GetProjectId

`func (o *CloudAssignmentResponse) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *CloudAssignmentResponse) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *CloudAssignmentResponse) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetCloudId

`func (o *CloudAssignmentResponse) GetCloudId() string`

GetCloudId returns the CloudId field if non-nil, zero value otherwise.

### GetCloudIdOk

`func (o *CloudAssignmentResponse) GetCloudIdOk() (*string, bool)`

GetCloudIdOk returns a tuple with the CloudId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudId

`func (o *CloudAssignmentResponse) SetCloudId(v string)`

SetCloudId sets CloudId field to given value.


### GetState

`func (o *CloudAssignmentResponse) GetState() string`

GetState returns the State field if non-nil, zero value otherwise.

### GetStateOk

`func (o *CloudAssignmentResponse) GetStateOk() (*string, bool)`

GetStateOk returns a tuple with the State field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetState

`func (o *CloudAssignmentResponse) SetState(v string)`

SetState sets State field to given value.


### GetMaterialised

`func (o *CloudAssignmentResponse) GetMaterialised() bool`

GetMaterialised returns the Materialised field if non-nil, zero value otherwise.

### GetMaterialisedOk

`func (o *CloudAssignmentResponse) GetMaterialisedOk() (*bool, bool)`

GetMaterialisedOk returns a tuple with the Materialised field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMaterialised

`func (o *CloudAssignmentResponse) SetMaterialised(v bool)`

SetMaterialised sets Materialised field to given value.


### GetCreatedAt

`func (o *CloudAssignmentResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *CloudAssignmentResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *CloudAssignmentResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *CloudAssignmentResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *CloudAssignmentResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *CloudAssignmentResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


