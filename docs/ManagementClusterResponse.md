# ManagementClusterResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Management cluster identifier (UUIDv7). | 
**Name** | **string** | Human-readable cluster name. | 
**Slug** | **string** | Unique human-facing shard key. Stable for the cluster&#39;s lifetime and used for deterministic region selection.  | 
**Region** | **string** | Region the cluster serves. Empty string when the fleet is a single unscoped cluster.  | 
**Status** | **string** | Last-observed lifecycle status string maintained by the reconciliation loop (for example &#x60;active&#x60;).  | 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). | 

## Methods

### NewManagementClusterResponse

`func NewManagementClusterResponse(id string, name string, slug string, region string, status string, createdAt time.Time, updatedAt time.Time, ) *ManagementClusterResponse`

NewManagementClusterResponse instantiates a new ManagementClusterResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewManagementClusterResponseWithDefaults

`func NewManagementClusterResponseWithDefaults() *ManagementClusterResponse`

NewManagementClusterResponseWithDefaults instantiates a new ManagementClusterResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *ManagementClusterResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *ManagementClusterResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *ManagementClusterResponse) SetId(v string)`

SetId sets Id field to given value.


### GetName

`func (o *ManagementClusterResponse) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *ManagementClusterResponse) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *ManagementClusterResponse) SetName(v string)`

SetName sets Name field to given value.


### GetSlug

`func (o *ManagementClusterResponse) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *ManagementClusterResponse) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *ManagementClusterResponse) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetRegion

`func (o *ManagementClusterResponse) GetRegion() string`

GetRegion returns the Region field if non-nil, zero value otherwise.

### GetRegionOk

`func (o *ManagementClusterResponse) GetRegionOk() (*string, bool)`

GetRegionOk returns a tuple with the Region field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegion

`func (o *ManagementClusterResponse) SetRegion(v string)`

SetRegion sets Region field to given value.


### GetStatus

`func (o *ManagementClusterResponse) GetStatus() string`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *ManagementClusterResponse) GetStatusOk() (*string, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *ManagementClusterResponse) SetStatus(v string)`

SetStatus sets Status field to given value.


### GetCreatedAt

`func (o *ManagementClusterResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *ManagementClusterResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *ManagementClusterResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *ManagementClusterResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *ManagementClusterResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *ManagementClusterResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


