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
**ProviderPackages** | [**[]CloudProviderPackage**](CloudProviderPackage.md) | The EFFECTIVE Crossplane provider packages for this Cloud: the pinned provider bundle version&#39;s set with the Cloud&#39;s &#x60;provider_package_overrides&#x60; merged over it when &#x60;provider_bundle_id&#x60; is present, otherwise the set the Cloud declares inline. Rendered in canonical source-ascending order regardless of the order the operator stated them in. A &#x60;PATCH /v1/clouds/{id}&#x60; carrying &#x60;provider_packages&#x60; replaces the whole inline set.  | 
**ProviderConfigApiVersion** | **string** | The EFFECTIVE &#x60;&lt;group&gt;/&lt;version&gt;&#x60; every declared package serves its ProviderConfig under (e.g. &#x60;aws.m.upbound.io/v1beta1&#x60;): the referenced provider bundle&#39;s value when &#x60;provider_bundle_id&#x60; is present, otherwise the Cloud&#39;s own. The Provisioning Broker stamps this value as the rendered ProviderConfig&#39;s apiVersion.  | 
**ProviderBundleId** | Pointer to **string** | Identifier of the provider bundle this Cloud takes its provider configuration from. Present only for a Cloud in bundle mode; a Cloud that declares its packages inline omits the field.  | [optional] 
**ProviderBundleSlug** | Pointer to **string** | Kebab-case handle of the referenced provider bundle, carried alongside the id so a client renders the reference without a second round-trip. Present only for a Cloud in bundle mode.  | [optional] 
**ProviderBundleVersion** | Pointer to **int64** | The content version of that bundle the Cloud pins — the declaration &#x60;provider_packages&#x60; and &#x60;provider_config_api_version&#x60; above were resolved from. Present exactly when &#x60;provider_bundle_id&#x60; is; a Cloud that declares its packages inline omits all three fields. It moves only on a Cloud write, so a bundle patch that publishes a newer version leaves this value alone.  | [optional] 
**ProviderPackageOverrides** | Pointer to [**[]CloudProviderPackage**](CloudProviderPackage.md) | The packages this Cloud runs differently from the version it pins, as the operator authored them, in canonical source-ascending order. Present exactly when &#x60;provider_bundle_id&#x60; is, and an empty array for a Cloud that states none; a Cloud that declares its packages inline omits the field.  An override whose source the pinned version carries replaces that member&#39;s version, and the merged entry reports &#x60;origin: override&#x60; under &#x60;provider_packages&#x60;. An override naming a source the pinned version does not carry joins the effective set and reports &#x60;origin: addition&#x60;. Nothing is ever removed, so the effective set is never smaller than the pinned version&#39;s.  | [optional] 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). Bumped by every mutator — &#x60;Rename&#x60;, &#x60;ChangeEndpoint&#x60;, &#x60;ChangeRegionDefaults&#x60;, &#x60;ChangeProviderPackages&#x60;, &#x60;ChangeProviderConfigAPIVersion&#x60;, &#x60;ReferenceProviderBundle&#x60;, &#x60;DeclareInlinePackages&#x60;.  | 

## Methods

### NewCloudResponse

`func NewCloudResponse(id string, displayName string, slug string, provider CloudProvider, endpoint map[string]interface{}, regionDefaults map[string]interface{}, externalId string, providerPackages []CloudProviderPackage, providerConfigApiVersion string, createdAt time.Time, updatedAt time.Time, ) *CloudResponse`

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


### GetProviderPackages

`func (o *CloudResponse) GetProviderPackages() []CloudProviderPackage`

GetProviderPackages returns the ProviderPackages field if non-nil, zero value otherwise.

### GetProviderPackagesOk

`func (o *CloudResponse) GetProviderPackagesOk() (*[]CloudProviderPackage, bool)`

GetProviderPackagesOk returns a tuple with the ProviderPackages field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderPackages

`func (o *CloudResponse) SetProviderPackages(v []CloudProviderPackage)`

SetProviderPackages sets ProviderPackages field to given value.


### GetProviderConfigApiVersion

`func (o *CloudResponse) GetProviderConfigApiVersion() string`

GetProviderConfigApiVersion returns the ProviderConfigApiVersion field if non-nil, zero value otherwise.

### GetProviderConfigApiVersionOk

`func (o *CloudResponse) GetProviderConfigApiVersionOk() (*string, bool)`

GetProviderConfigApiVersionOk returns a tuple with the ProviderConfigApiVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderConfigApiVersion

`func (o *CloudResponse) SetProviderConfigApiVersion(v string)`

SetProviderConfigApiVersion sets ProviderConfigApiVersion field to given value.


### GetProviderBundleId

`func (o *CloudResponse) GetProviderBundleId() string`

GetProviderBundleId returns the ProviderBundleId field if non-nil, zero value otherwise.

### GetProviderBundleIdOk

`func (o *CloudResponse) GetProviderBundleIdOk() (*string, bool)`

GetProviderBundleIdOk returns a tuple with the ProviderBundleId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderBundleId

`func (o *CloudResponse) SetProviderBundleId(v string)`

SetProviderBundleId sets ProviderBundleId field to given value.

### HasProviderBundleId

`func (o *CloudResponse) HasProviderBundleId() bool`

HasProviderBundleId returns a boolean if a field has been set.

### GetProviderBundleSlug

`func (o *CloudResponse) GetProviderBundleSlug() string`

GetProviderBundleSlug returns the ProviderBundleSlug field if non-nil, zero value otherwise.

### GetProviderBundleSlugOk

`func (o *CloudResponse) GetProviderBundleSlugOk() (*string, bool)`

GetProviderBundleSlugOk returns a tuple with the ProviderBundleSlug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderBundleSlug

`func (o *CloudResponse) SetProviderBundleSlug(v string)`

SetProviderBundleSlug sets ProviderBundleSlug field to given value.

### HasProviderBundleSlug

`func (o *CloudResponse) HasProviderBundleSlug() bool`

HasProviderBundleSlug returns a boolean if a field has been set.

### GetProviderBundleVersion

`func (o *CloudResponse) GetProviderBundleVersion() int64`

GetProviderBundleVersion returns the ProviderBundleVersion field if non-nil, zero value otherwise.

### GetProviderBundleVersionOk

`func (o *CloudResponse) GetProviderBundleVersionOk() (*int64, bool)`

GetProviderBundleVersionOk returns a tuple with the ProviderBundleVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderBundleVersion

`func (o *CloudResponse) SetProviderBundleVersion(v int64)`

SetProviderBundleVersion sets ProviderBundleVersion field to given value.

### HasProviderBundleVersion

`func (o *CloudResponse) HasProviderBundleVersion() bool`

HasProviderBundleVersion returns a boolean if a field has been set.

### GetProviderPackageOverrides

`func (o *CloudResponse) GetProviderPackageOverrides() []CloudProviderPackage`

GetProviderPackageOverrides returns the ProviderPackageOverrides field if non-nil, zero value otherwise.

### GetProviderPackageOverridesOk

`func (o *CloudResponse) GetProviderPackageOverridesOk() (*[]CloudProviderPackage, bool)`

GetProviderPackageOverridesOk returns a tuple with the ProviderPackageOverrides field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderPackageOverrides

`func (o *CloudResponse) SetProviderPackageOverrides(v []CloudProviderPackage)`

SetProviderPackageOverrides sets ProviderPackageOverrides field to given value.

### HasProviderPackageOverrides

`func (o *CloudResponse) HasProviderPackageOverrides() bool`

HasProviderPackageOverrides returns a boolean if a field has been set.

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


