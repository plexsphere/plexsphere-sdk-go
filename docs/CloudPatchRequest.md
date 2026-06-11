# CloudPatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | Pointer to **string** | New human-readable Cloud name. The aggregate&#39;s &#x60;Rename&#x60; mutator validates the same constraints as &#x60;NewCloud&#x60;.  | [optional] 
**Endpoint** | Pointer to **map[string]interface{}** | New provider-specific connection metadata. Triggers a re-run of the per-provider validator on the merged next- state.  | [optional] 
**RegionDefaults** | Pointer to **map[string]interface{}** | New provider-specific region/default metadata. Triggers a re-run of the per-provider validator on the merged next- state.  | [optional] 

## Methods

### NewCloudPatchRequest

`func NewCloudPatchRequest() *CloudPatchRequest`

NewCloudPatchRequest instantiates a new CloudPatchRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCloudPatchRequestWithDefaults

`func NewCloudPatchRequestWithDefaults() *CloudPatchRequest`

NewCloudPatchRequestWithDefaults instantiates a new CloudPatchRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDisplayName

`func (o *CloudPatchRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *CloudPatchRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *CloudPatchRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.

### HasDisplayName

`func (o *CloudPatchRequest) HasDisplayName() bool`

HasDisplayName returns a boolean if a field has been set.

### GetEndpoint

`func (o *CloudPatchRequest) GetEndpoint() map[string]interface{}`

GetEndpoint returns the Endpoint field if non-nil, zero value otherwise.

### GetEndpointOk

`func (o *CloudPatchRequest) GetEndpointOk() (*map[string]interface{}, bool)`

GetEndpointOk returns a tuple with the Endpoint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetEndpoint

`func (o *CloudPatchRequest) SetEndpoint(v map[string]interface{})`

SetEndpoint sets Endpoint field to given value.

### HasEndpoint

`func (o *CloudPatchRequest) HasEndpoint() bool`

HasEndpoint returns a boolean if a field has been set.

### GetRegionDefaults

`func (o *CloudPatchRequest) GetRegionDefaults() map[string]interface{}`

GetRegionDefaults returns the RegionDefaults field if non-nil, zero value otherwise.

### GetRegionDefaultsOk

`func (o *CloudPatchRequest) GetRegionDefaultsOk() (*map[string]interface{}, bool)`

GetRegionDefaultsOk returns a tuple with the RegionDefaults field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegionDefaults

`func (o *CloudPatchRequest) SetRegionDefaults(v map[string]interface{})`

SetRegionDefaults sets RegionDefaults field to given value.

### HasRegionDefaults

`func (o *CloudPatchRequest) HasRegionDefaults() bool`

HasRegionDefaults returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


