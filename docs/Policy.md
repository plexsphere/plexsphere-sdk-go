# Policy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Policy identifier (UUIDv7). | 
**ProjectId** | **string** | Owning Project (UUIDv7). | 
**Slug** | **string** | Stable kebab-case handle for the Policy. Unique within the owning Project — a duplicate &#x60;(project_id, slug)&#x60; rejects with &#x60;409 policy_slug_taken&#x60;.  | 
**DisplayName** | Pointer to **string** | Human-readable label. Optional — falls back to &#x60;slug&#x60; in renderings when empty.  | [optional] 
**HeadRevisionId** | **string** | Identifier of the current head revision. Advances every PATCH inside the same transaction that inserts the new revision row.  | 
**CreatedAt** | **time.Time** |  | 
**UpdatedAt** | **time.Time** | Timestamp of the last head-revision advance. Equal to &#x60;created_at&#x60; on a freshly-created Policy.  | 
**Head** | Pointer to [**PolicyRevision**](PolicyRevision.md) | Fully-hydrated head revision. Returned on &#x60;GET&#x60; of a single Policy; intentionally omitted from list entries to keep the page payload bounded — callers that need rule lists per row iterate the list and then &#x60;GET&#x60; each Policy.  | [optional] 

## Methods

### NewPolicy

`func NewPolicy(id string, projectId string, slug string, headRevisionId string, createdAt time.Time, updatedAt time.Time, ) *Policy`

NewPolicy instantiates a new Policy object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyWithDefaults

`func NewPolicyWithDefaults() *Policy`

NewPolicyWithDefaults instantiates a new Policy object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *Policy) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *Policy) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *Policy) SetId(v string)`

SetId sets Id field to given value.


### GetProjectId

`func (o *Policy) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *Policy) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *Policy) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetSlug

`func (o *Policy) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *Policy) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *Policy) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *Policy) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *Policy) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *Policy) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.

### HasDisplayName

`func (o *Policy) HasDisplayName() bool`

HasDisplayName returns a boolean if a field has been set.

### GetHeadRevisionId

`func (o *Policy) GetHeadRevisionId() string`

GetHeadRevisionId returns the HeadRevisionId field if non-nil, zero value otherwise.

### GetHeadRevisionIdOk

`func (o *Policy) GetHeadRevisionIdOk() (*string, bool)`

GetHeadRevisionIdOk returns a tuple with the HeadRevisionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHeadRevisionId

`func (o *Policy) SetHeadRevisionId(v string)`

SetHeadRevisionId sets HeadRevisionId field to given value.


### GetCreatedAt

`func (o *Policy) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *Policy) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *Policy) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *Policy) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *Policy) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *Policy) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.


### GetHead

`func (o *Policy) GetHead() PolicyRevision`

GetHead returns the Head field if non-nil, zero value otherwise.

### GetHeadOk

`func (o *Policy) GetHeadOk() (*PolicyRevision, bool)`

GetHeadOk returns a tuple with the Head field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHead

`func (o *Policy) SetHead(v PolicyRevision)`

SetHead sets Head field to given value.

### HasHead

`func (o *Policy) HasHead() bool`

HasHead returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


