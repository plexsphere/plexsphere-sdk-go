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
**ProviderPackages** | Pointer to [**[]CloudProviderPackage**](CloudProviderPackage.md) | The Crossplane provider packages the Cloud declares inline. Required in inline mode and forbidden alongside &#x60;provider_bundle_id&#x60;. Each &#x60;source&#x60; may appear only once. The read surfaces render the set in canonical source-ascending order, not in the order stated here.  | [optional] 
**ProviderConfigApiVersion** | Pointer to **string** | The &#x60;&lt;group&gt;/&lt;version&gt;&#x60; every inline-declared package serves its ProviderConfig under (e.g. &#x60;aws.m.upbound.io/v1beta1&#x60;). Required in inline mode and forbidden alongside &#x60;provider_bundle_id&#x60;. The Provisioning Broker stamps this value as the rendered ProviderConfig&#39;s apiVersion.  | [optional] 
**ProviderBundleId** | Pointer to **string** | Identifier (UUID) of the provider bundle this Cloud takes its provider configuration from. Naming it puts the Cloud in bundle mode, which forbids &#x60;provider_packages&#x60; and &#x60;provider_config_api_version&#x60; in the same request. The bundle must exist and must serve the same &#x60;provider&#x60; as the Cloud: an unknown id is rejected with &#x60;400 unknown_provider_bundle&#x60;, a bundle of another provider with &#x60;400 provider_bundle_provider_mismatch&#x60;.  DECISION: the field carries no &#x60;format: uuid&#x60;. A format-annotated field is rejected during JSON decoding, so a malformed id would answer &#x60;400 invalid_body&#x60; before the service&#39;s admission check runs and the operator would never learn which field was wrong. The value is a canonical UUID string and a malformed one surfaces as &#x60;400 invalid_cloud_provider_mode&#x60; naming &#x60;provider_bundle_id&#x60;.  | [optional] 
**ProviderBundleVersion** | Pointer to **int64** | The content version of the named bundle the new Cloud pins. Omit it and the write pins the bundle&#39;s latest version, which is the declaration an operator reads when they pick the bundle; name one to pin an older declaration instead.  The field belongs to bundle mode: setting it without &#x60;provider_bundle_id&#x60; is rejected with &#x60;400 invalid_cloud_provider_mode&#x60;. A version the bundle never published is rejected with &#x60;400 provider_bundle_version_not_found&#x60;.  | [optional] 
**ProviderPackageOverrides** | Pointer to [**[]CloudProviderPackage**](CloudProviderPackage.md) | Packages the new Cloud runs differently from the version it pins. Each &#x60;source&#x60; may appear only once. Omit the field, or state the empty array, and the Cloud takes the pinned version as it stands.  The field belongs to bundle mode: setting it without &#x60;provider_bundle_id&#x60; is rejected with &#x60;400 invalid_cloud_provider_mode&#x60;. An override is a deviation from a referenced declaration, and a Cloud that owns its package set runs another version by editing that set.  | [optional] 

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


### GetProviderPackages

`func (o *CloudCreateRequest) GetProviderPackages() []CloudProviderPackage`

GetProviderPackages returns the ProviderPackages field if non-nil, zero value otherwise.

### GetProviderPackagesOk

`func (o *CloudCreateRequest) GetProviderPackagesOk() (*[]CloudProviderPackage, bool)`

GetProviderPackagesOk returns a tuple with the ProviderPackages field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderPackages

`func (o *CloudCreateRequest) SetProviderPackages(v []CloudProviderPackage)`

SetProviderPackages sets ProviderPackages field to given value.

### HasProviderPackages

`func (o *CloudCreateRequest) HasProviderPackages() bool`

HasProviderPackages returns a boolean if a field has been set.

### GetProviderConfigApiVersion

`func (o *CloudCreateRequest) GetProviderConfigApiVersion() string`

GetProviderConfigApiVersion returns the ProviderConfigApiVersion field if non-nil, zero value otherwise.

### GetProviderConfigApiVersionOk

`func (o *CloudCreateRequest) GetProviderConfigApiVersionOk() (*string, bool)`

GetProviderConfigApiVersionOk returns a tuple with the ProviderConfigApiVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderConfigApiVersion

`func (o *CloudCreateRequest) SetProviderConfigApiVersion(v string)`

SetProviderConfigApiVersion sets ProviderConfigApiVersion field to given value.

### HasProviderConfigApiVersion

`func (o *CloudCreateRequest) HasProviderConfigApiVersion() bool`

HasProviderConfigApiVersion returns a boolean if a field has been set.

### GetProviderBundleId

`func (o *CloudCreateRequest) GetProviderBundleId() string`

GetProviderBundleId returns the ProviderBundleId field if non-nil, zero value otherwise.

### GetProviderBundleIdOk

`func (o *CloudCreateRequest) GetProviderBundleIdOk() (*string, bool)`

GetProviderBundleIdOk returns a tuple with the ProviderBundleId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderBundleId

`func (o *CloudCreateRequest) SetProviderBundleId(v string)`

SetProviderBundleId sets ProviderBundleId field to given value.

### HasProviderBundleId

`func (o *CloudCreateRequest) HasProviderBundleId() bool`

HasProviderBundleId returns a boolean if a field has been set.

### GetProviderBundleVersion

`func (o *CloudCreateRequest) GetProviderBundleVersion() int64`

GetProviderBundleVersion returns the ProviderBundleVersion field if non-nil, zero value otherwise.

### GetProviderBundleVersionOk

`func (o *CloudCreateRequest) GetProviderBundleVersionOk() (*int64, bool)`

GetProviderBundleVersionOk returns a tuple with the ProviderBundleVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderBundleVersion

`func (o *CloudCreateRequest) SetProviderBundleVersion(v int64)`

SetProviderBundleVersion sets ProviderBundleVersion field to given value.

### HasProviderBundleVersion

`func (o *CloudCreateRequest) HasProviderBundleVersion() bool`

HasProviderBundleVersion returns a boolean if a field has been set.

### GetProviderPackageOverrides

`func (o *CloudCreateRequest) GetProviderPackageOverrides() []CloudProviderPackage`

GetProviderPackageOverrides returns the ProviderPackageOverrides field if non-nil, zero value otherwise.

### GetProviderPackageOverridesOk

`func (o *CloudCreateRequest) GetProviderPackageOverridesOk() (*[]CloudProviderPackage, bool)`

GetProviderPackageOverridesOk returns a tuple with the ProviderPackageOverrides field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderPackageOverrides

`func (o *CloudCreateRequest) SetProviderPackageOverrides(v []CloudProviderPackage)`

SetProviderPackageOverrides sets ProviderPackageOverrides field to given value.

### HasProviderPackageOverrides

`func (o *CloudCreateRequest) HasProviderPackageOverrides() bool`

HasProviderPackageOverrides returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


