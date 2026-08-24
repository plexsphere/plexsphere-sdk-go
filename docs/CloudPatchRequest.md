# CloudPatchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | Pointer to **string** | New human-readable Cloud name. The aggregate&#39;s &#x60;Rename&#x60; mutator validates the same constraints as &#x60;NewCloud&#x60;.  | [optional] 
**Endpoint** | Pointer to **map[string]interface{}** | New provider-specific connection metadata. Triggers a re-run of the per-provider validator on the merged next- state.  | [optional] 
**RegionDefaults** | Pointer to **map[string]interface{}** | New provider-specific region/default metadata. Triggers a re-run of the per-provider validator on the merged next- state.  | [optional] 
**ProviderPackages** | Pointer to [**[]CloudProviderPackage**](CloudProviderPackage.md) | Replacement package set. The whole set is replaced rather than merged. Omit the field to leave the current set untouched. The read surfaces render the result in canonical source-ascending order.  | [optional] 
**ProviderConfigApiVersion** | Pointer to **string** | New &#x60;&lt;group&gt;/&lt;version&gt;&#x60; every declared package serves its ProviderConfig under. Patchable independently of &#x60;provider_packages&#x60;, except on a Cloud leaving bundle mode, where both inline fields have to be stated together.  | [optional] 
**ProviderBundleId** | Pointer to **string** | Identifier (UUID) of the provider bundle the Cloud takes its provider configuration from after the patch. Forbidden alongside &#x60;provider_packages&#x60; and &#x60;provider_config_api_version&#x60;. The bundle must exist and must serve the same &#x60;provider&#x60; as the Cloud: an unknown id is rejected with &#x60;400 unknown_provider_bundle&#x60;, a bundle of another provider with &#x60;400 provider_bundle_provider_mismatch&#x60;.  DECISION: the field carries no &#x60;format: uuid&#x60;, for the reason the create request records — a format-annotated field is rejected during JSON decoding, so a malformed id would answer &#x60;400 invalid_body&#x60; before the service&#39;s admission check runs and the operator would never learn which field was wrong.  | [optional] 
**ProviderBundleVersion** | Pointer to **int64** | The content version of the referenced bundle the Cloud pins after the patch. Omitted alongside a &#x60;provider_bundle_id&#x60; that puts the Cloud into bundle mode, the write pins that bundle&#39;s latest version; on its own it promotes a Cloud already in bundle mode onto the named version.  Naming it while the Cloud neither is nor becomes a bundle reference is rejected with &#x60;400 invalid_cloud_provider_mode&#x60;. A version the bundle never published is rejected with &#x60;400 provider_bundle_version_not_found&#x60;.  | [optional] 
**ProviderPackageOverrides** | Pointer to [**[]CloudProviderPackage**](CloudProviderPackage.md) | Replacement override set. The whole set is replaced rather than merged. Omit the field to leave the current set untouched; state &#x60;[]&#x60; to clear it, which puts the Cloud back on the pinned bundle version as it stands. Each &#x60;source&#x60; may appear only once.  Stating it while the patched Cloud ends the write declaring its packages inline is rejected with &#x60;400 invalid_cloud_provider_mode&#x60;.  | [optional] 

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

### GetProviderPackages

`func (o *CloudPatchRequest) GetProviderPackages() []CloudProviderPackage`

GetProviderPackages returns the ProviderPackages field if non-nil, zero value otherwise.

### GetProviderPackagesOk

`func (o *CloudPatchRequest) GetProviderPackagesOk() (*[]CloudProviderPackage, bool)`

GetProviderPackagesOk returns a tuple with the ProviderPackages field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderPackages

`func (o *CloudPatchRequest) SetProviderPackages(v []CloudProviderPackage)`

SetProviderPackages sets ProviderPackages field to given value.

### HasProviderPackages

`func (o *CloudPatchRequest) HasProviderPackages() bool`

HasProviderPackages returns a boolean if a field has been set.

### GetProviderConfigApiVersion

`func (o *CloudPatchRequest) GetProviderConfigApiVersion() string`

GetProviderConfigApiVersion returns the ProviderConfigApiVersion field if non-nil, zero value otherwise.

### GetProviderConfigApiVersionOk

`func (o *CloudPatchRequest) GetProviderConfigApiVersionOk() (*string, bool)`

GetProviderConfigApiVersionOk returns a tuple with the ProviderConfigApiVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderConfigApiVersion

`func (o *CloudPatchRequest) SetProviderConfigApiVersion(v string)`

SetProviderConfigApiVersion sets ProviderConfigApiVersion field to given value.

### HasProviderConfigApiVersion

`func (o *CloudPatchRequest) HasProviderConfigApiVersion() bool`

HasProviderConfigApiVersion returns a boolean if a field has been set.

### GetProviderBundleId

`func (o *CloudPatchRequest) GetProviderBundleId() string`

GetProviderBundleId returns the ProviderBundleId field if non-nil, zero value otherwise.

### GetProviderBundleIdOk

`func (o *CloudPatchRequest) GetProviderBundleIdOk() (*string, bool)`

GetProviderBundleIdOk returns a tuple with the ProviderBundleId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderBundleId

`func (o *CloudPatchRequest) SetProviderBundleId(v string)`

SetProviderBundleId sets ProviderBundleId field to given value.

### HasProviderBundleId

`func (o *CloudPatchRequest) HasProviderBundleId() bool`

HasProviderBundleId returns a boolean if a field has been set.

### GetProviderBundleVersion

`func (o *CloudPatchRequest) GetProviderBundleVersion() int64`

GetProviderBundleVersion returns the ProviderBundleVersion field if non-nil, zero value otherwise.

### GetProviderBundleVersionOk

`func (o *CloudPatchRequest) GetProviderBundleVersionOk() (*int64, bool)`

GetProviderBundleVersionOk returns a tuple with the ProviderBundleVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderBundleVersion

`func (o *CloudPatchRequest) SetProviderBundleVersion(v int64)`

SetProviderBundleVersion sets ProviderBundleVersion field to given value.

### HasProviderBundleVersion

`func (o *CloudPatchRequest) HasProviderBundleVersion() bool`

HasProviderBundleVersion returns a boolean if a field has been set.

### GetProviderPackageOverrides

`func (o *CloudPatchRequest) GetProviderPackageOverrides() []CloudProviderPackage`

GetProviderPackageOverrides returns the ProviderPackageOverrides field if non-nil, zero value otherwise.

### GetProviderPackageOverridesOk

`func (o *CloudPatchRequest) GetProviderPackageOverridesOk() (*[]CloudProviderPackage, bool)`

GetProviderPackageOverridesOk returns a tuple with the ProviderPackageOverrides field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderPackageOverrides

`func (o *CloudPatchRequest) SetProviderPackageOverrides(v []CloudProviderPackage)`

SetProviderPackageOverrides sets ProviderPackageOverrides field to given value.

### HasProviderPackageOverrides

`func (o *CloudPatchRequest) HasProviderPackageOverrides() bool`

HasProviderPackageOverrides returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


