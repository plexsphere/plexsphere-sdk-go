# CredentialAssignmentResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Credential Assignment identifier (UUIDv7). | 
**ProjectId** | **string** | Identifier of the owning Project — the residency pivot the ReBAC gate authorises against.  | 
**CloudCredentialId** | **string** | Identifier of the Cloud Credential bound to the Project by this assignment.  | 
**State** | [**CredentialAssignmentState**](CredentialAssignmentState.md) |  | 
**Materialised** | **bool** | Whether the assignment&#39;s binding is currently live. &#x60;true&#x60; only while the assignment is in the &#x60;approved&#x60; state; &#x60;false&#x60; for &#x60;requested&#x60;, &#x60;rejected&#x60;, and &#x60;revoked&#x60;.  | 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). Bumped by every lifecycle transition — approve, reject, revoke.  | 

## Methods

### NewCredentialAssignmentResponse

`func NewCredentialAssignmentResponse(id string, projectId string, cloudCredentialId string, state CredentialAssignmentState, materialised bool, createdAt time.Time, updatedAt time.Time, ) *CredentialAssignmentResponse`

NewCredentialAssignmentResponse instantiates a new CredentialAssignmentResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCredentialAssignmentResponseWithDefaults

`func NewCredentialAssignmentResponseWithDefaults() *CredentialAssignmentResponse`

NewCredentialAssignmentResponseWithDefaults instantiates a new CredentialAssignmentResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *CredentialAssignmentResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *CredentialAssignmentResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *CredentialAssignmentResponse) SetId(v string)`

SetId sets Id field to given value.


### GetProjectId

`func (o *CredentialAssignmentResponse) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *CredentialAssignmentResponse) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *CredentialAssignmentResponse) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetCloudCredentialId

`func (o *CredentialAssignmentResponse) GetCloudCredentialId() string`

GetCloudCredentialId returns the CloudCredentialId field if non-nil, zero value otherwise.

### GetCloudCredentialIdOk

`func (o *CredentialAssignmentResponse) GetCloudCredentialIdOk() (*string, bool)`

GetCloudCredentialIdOk returns a tuple with the CloudCredentialId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudCredentialId

`func (o *CredentialAssignmentResponse) SetCloudCredentialId(v string)`

SetCloudCredentialId sets CloudCredentialId field to given value.


### GetState

`func (o *CredentialAssignmentResponse) GetState() CredentialAssignmentState`

GetState returns the State field if non-nil, zero value otherwise.

### GetStateOk

`func (o *CredentialAssignmentResponse) GetStateOk() (*CredentialAssignmentState, bool)`

GetStateOk returns a tuple with the State field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetState

`func (o *CredentialAssignmentResponse) SetState(v CredentialAssignmentState)`

SetState sets State field to given value.


### GetMaterialised

`func (o *CredentialAssignmentResponse) GetMaterialised() bool`

GetMaterialised returns the Materialised field if non-nil, zero value otherwise.

### GetMaterialisedOk

`func (o *CredentialAssignmentResponse) GetMaterialisedOk() (*bool, bool)`

GetMaterialisedOk returns a tuple with the Materialised field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMaterialised

`func (o *CredentialAssignmentResponse) SetMaterialised(v bool)`

SetMaterialised sets Materialised field to given value.


### GetCreatedAt

`func (o *CredentialAssignmentResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *CredentialAssignmentResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *CredentialAssignmentResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *CredentialAssignmentResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *CredentialAssignmentResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *CredentialAssignmentResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


