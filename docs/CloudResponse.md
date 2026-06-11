# CloudResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Cloud identifier (UUIDv7). | 
**DisplayName** | **string** | Human-readable Cloud name (trimmed at the aggregate). | 
**Slug** | **string** | Kebab-case URL handle. Stable for the lifetime of the Cloud — see the &#x60;cloud&#x60; tag description for the immutability rationale.  | 
**Provider** | [**CloudProvider**](CloudProvider.md) |  | 
**Endpoint** | **map[string]interface{}** | Provider-specific connection metadata stored as a JSONB blob. The per-provider validator owns the field-shape contract; this schema only declares the wire envelope.  | 
**RegionDefaults** | **map[string]interface{}** | Provider-specific region/default metadata stored as a JSONB blob. The per-provider validator owns the field- shape contract.  | 
**ExternalId** | **string** | Upstream provider account identifier (e.g. AWS account id, Azure tenant id). Combined with &#x60;provider&#x60; it must be unique across all Clouds.  | 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). Bumped by every mutator — &#x60;Rename&#x60;, &#x60;ChangeEndpoint&#x60;, &#x60;ChangeRegionDefaults&#x60;.  | 

## Methods

### NewCloudResponse

`func NewCloudResponse(id string, displayName string, slug string, provider CloudProvider, endpoint map[string]interface{}, regionDefaults map[string]interface{}, externalId string, createdAt time.Time, updatedAt time.Time, ) *CloudResponse`

NewCloudResponse instantiates a new CloudResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudResponseWithDefaults

`func NewCloudResponseWithDefaults() *CloudResponse`

NewCloudResponseWithDefaults instantiates a new CloudResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *CloudResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *CloudResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *CloudResponse) SetId(v string)`

SetId sets Id field to given value.


### GetDisplayName

`func (o *CloudResponse) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *CloudResponse) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *CloudResponse) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetSlug

`func (o *CloudResponse) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *CloudResponse) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *CloudResponse) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetProvider

`func (o *CloudResponse) GetProvider() CloudProvider`

GetProvider returns the Provider field if non-nil, zero value otherwise.

### GetProviderOk

`func (o *CloudResponse) GetProviderOk() (*CloudProvider, bool)`

GetProviderOk returns a tuple with the Provider field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProvider

`func (o *CloudResponse) SetProvider(v CloudProvider)`

SetProvider sets Provider field to given value.


### GetEndpoint

`func (o *CloudResponse) GetEndpoint() map[string]interface{}`

GetEndpoint returns the Endpoint field if non-nil, zero value otherwise.

### GetEndpointOk

`func (o *CloudResponse) GetEndpointOk() (*map[string]interface{}, bool)`

GetEndpointOk returns a tuple with the Endpoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEndpoint

`func (o *CloudResponse) SetEndpoint(v map[string]interface{})`

SetEndpoint sets Endpoint field to given value.


### GetRegionDefaults

`func (o *CloudResponse) GetRegionDefaults() map[string]interface{}`

GetRegionDefaults returns the RegionDefaults field if non-nil, zero value otherwise.

### GetRegionDefaultsOk

`func (o *CloudResponse) GetRegionDefaultsOk() (*map[string]interface{}, bool)`

GetRegionDefaultsOk returns a tuple with the RegionDefaults field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegionDefaults

`func (o *CloudResponse) SetRegionDefaults(v map[string]interface{})`

SetRegionDefaults sets RegionDefaults field to given value.


### GetExternalId

`func (o *CloudResponse) GetExternalId() string`

GetExternalId returns the ExternalId field if non-nil, zero value otherwise.

### GetExternalIdOk

`func (o *CloudResponse) GetExternalIdOk() (*string, bool)`

GetExternalIdOk returns a tuple with the ExternalId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExternalId

`func (o *CloudResponse) SetExternalId(v string)`

SetExternalId sets ExternalId field to given value.


### GetCreatedAt

`func (o *CloudResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *CloudResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *CloudResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *CloudResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *CloudResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *CloudResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


