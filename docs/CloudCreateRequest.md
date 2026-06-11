# CloudCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | **string** | Human-readable Cloud name. Whitespace-only is rejected. | 
**Slug** | **string** | Kebab-case URL handle. The aggregate&#39;s &#x60;ParseSlug&#x60; enforces the same regex; surfacing the pattern here lets the generated client validate before the round-trip.  | 
**Provider** | [**CloudProvider**](CloudProvider.md) |  | 
**Endpoint** | **map[string]interface{}** | Provider-specific connection metadata. The per-provider validator runs at decode time; field-level rejections surface as &#x60;400 invalid_cloud_endpoint&#x60;.  | 
**RegionDefaults** | **map[string]interface{}** | Provider-specific region/default metadata. The per- provider validator runs at decode time; field-level rejections surface as &#x60;400 invalid_cloud_region_defaults&#x60;.  | 
**ExternalId** | **string** | Upstream provider account identifier. Combined with &#x60;provider&#x60; must be unique across all Clouds.  | 

## Methods

### NewCloudCreateRequest

`func NewCloudCreateRequest(displayName string, slug string, provider CloudProvider, endpoint map[string]interface{}, regionDefaults map[string]interface{}, externalId string, ) *CloudCreateRequest`

NewCloudCreateRequest instantiates a new CloudCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudCreateRequestWithDefaults

`func NewCloudCreateRequestWithDefaults() *CloudCreateRequest`

NewCloudCreateRequestWithDefaults instantiates a new CloudCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDisplayName

`func (o *CloudCreateRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *CloudCreateRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *CloudCreateRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetSlug

`func (o *CloudCreateRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *CloudCreateRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *CloudCreateRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetProvider

`func (o *CloudCreateRequest) GetProvider() CloudProvider`

GetProvider returns the Provider field if non-nil, zero value otherwise.

### GetProviderOk

`func (o *CloudCreateRequest) GetProviderOk() (*CloudProvider, bool)`

GetProviderOk returns a tuple with the Provider field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProvider

`func (o *CloudCreateRequest) SetProvider(v CloudProvider)`

SetProvider sets Provider field to given value.


### GetEndpoint

`func (o *CloudCreateRequest) GetEndpoint() map[string]interface{}`

GetEndpoint returns the Endpoint field if non-nil, zero value otherwise.

### GetEndpointOk

`func (o *CloudCreateRequest) GetEndpointOk() (*map[string]interface{}, bool)`

GetEndpointOk returns a tuple with the Endpoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEndpoint

`func (o *CloudCreateRequest) SetEndpoint(v map[string]interface{})`

SetEndpoint sets Endpoint field to given value.


### GetRegionDefaults

`func (o *CloudCreateRequest) GetRegionDefaults() map[string]interface{}`

GetRegionDefaults returns the RegionDefaults field if non-nil, zero value otherwise.

### GetRegionDefaultsOk

`func (o *CloudCreateRequest) GetRegionDefaultsOk() (*map[string]interface{}, bool)`

GetRegionDefaultsOk returns a tuple with the RegionDefaults field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegionDefaults

`func (o *CloudCreateRequest) SetRegionDefaults(v map[string]interface{})`

SetRegionDefaults sets RegionDefaults field to given value.


### GetExternalId

`func (o *CloudCreateRequest) GetExternalId() string`

GetExternalId returns the ExternalId field if non-nil, zero value otherwise.

### GetExternalIdOk

`func (o *CloudCreateRequest) GetExternalIdOk() (*string, bool)`

GetExternalIdOk returns a tuple with the ExternalId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExternalId

`func (o *CloudCreateRequest) SetExternalId(v string)`

SetExternalId sets ExternalId field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


