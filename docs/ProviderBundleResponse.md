# ProviderBundleResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Provider bundle identifier (UUIDv7). | 
**Slug** | **string** | Kebab-case URL handle. Stable for the lifetime of the bundle — see &#x60;PatchProviderBundle&#x60; for the immutability rationale.  | 
**DisplayName** | **string** | Human-readable bundle name (trimmed at the aggregate). | 
**Provider** | [**CloudProvider**](CloudProvider.md) |  | 
**ProviderPackages** | [**[]CloudProviderPackage**](CloudProviderPackage.md) | The Crossplane provider packages this bundle declares, rendered in canonical source-ascending order regardless of the order the operator stated them in.  | 
**ProviderConfigApiVersion** | **string** | The &#x60;&lt;group&gt;/&lt;version&gt;&#x60; every declared package serves its ProviderConfig under (e.g. &#x60;aws.m.upbound.io/v1beta1&#x60;). A Cloud pinned to the latest version resolves to this value.  | 
**LatestVersion** | **int64** | The newest content version the bundle has published. A content patch — one carrying &#x60;provider_packages&#x60; or &#x60;provider_config_api_version&#x60; — publishes the next one and reports it here; a rename-only patch leaves it where it is. The two content fields publish ONE version between them even when a patch names both. This is the version an attach with no explicit &#x60;provider_bundle_version&#x60; pins, and the whole history is readable at &#x60;GET /v1/provider-bundles/{id}/versions&#x60;.  | 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). Bumped by every mutator — &#x60;Rename&#x60;, &#x60;ChangeProviderPackages&#x60;, &#x60;ChangeProviderConfigAPIVersion&#x60;.  | 

## Methods

### NewProviderBundleResponse

`func NewProviderBundleResponse(id string, slug string, displayName string, provider CloudProvider, providerPackages []CloudProviderPackage, providerConfigApiVersion string, latestVersion int64, createdAt time.Time, updatedAt time.Time, ) *ProviderBundleResponse`

NewProviderBundleResponse instantiates a new ProviderBundleResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProviderBundleResponseWithDefaults

`func NewProviderBundleResponseWithDefaults() *ProviderBundleResponse`

NewProviderBundleResponseWithDefaults instantiates a new ProviderBundleResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *ProviderBundleResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *ProviderBundleResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *ProviderBundleResponse) SetId(v string)`

SetId sets Id field to given value.


### GetSlug

`func (o *ProviderBundleResponse) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *ProviderBundleResponse) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *ProviderBundleResponse) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *ProviderBundleResponse) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *ProviderBundleResponse) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *ProviderBundleResponse) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetProvider

`func (o *ProviderBundleResponse) GetProvider() CloudProvider`

GetProvider returns the Provider field if non-nil, zero value otherwise.

### GetProviderOk

`func (o *ProviderBundleResponse) GetProviderOk() (*CloudProvider, bool)`

GetProviderOk returns a tuple with the Provider field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProvider

`func (o *ProviderBundleResponse) SetProvider(v CloudProvider)`

SetProvider sets Provider field to given value.


### GetProviderPackages

`func (o *ProviderBundleResponse) GetProviderPackages() []CloudProviderPackage`

GetProviderPackages returns the ProviderPackages field if non-nil, zero value otherwise.

### GetProviderPackagesOk

`func (o *ProviderBundleResponse) GetProviderPackagesOk() (*[]CloudProviderPackage, bool)`

GetProviderPackagesOk returns a tuple with the ProviderPackages field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderPackages

`func (o *ProviderBundleResponse) SetProviderPackages(v []CloudProviderPackage)`

SetProviderPackages sets ProviderPackages field to given value.


### GetProviderConfigApiVersion

`func (o *ProviderBundleResponse) GetProviderConfigApiVersion() string`

GetProviderConfigApiVersion returns the ProviderConfigApiVersion field if non-nil, zero value otherwise.

### GetProviderConfigApiVersionOk

`func (o *ProviderBundleResponse) GetProviderConfigApiVersionOk() (*string, bool)`

GetProviderConfigApiVersionOk returns a tuple with the ProviderConfigApiVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderConfigApiVersion

`func (o *ProviderBundleResponse) SetProviderConfigApiVersion(v string)`

SetProviderConfigApiVersion sets ProviderConfigApiVersion field to given value.


### GetLatestVersion

`func (o *ProviderBundleResponse) GetLatestVersion() int64`

GetLatestVersion returns the LatestVersion field if non-nil, zero value otherwise.

### GetLatestVersionOk

`func (o *ProviderBundleResponse) GetLatestVersionOk() (*int64, bool)`

GetLatestVersionOk returns a tuple with the LatestVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLatestVersion

`func (o *ProviderBundleResponse) SetLatestVersion(v int64)`

SetLatestVersion sets LatestVersion field to given value.


### GetCreatedAt

`func (o *ProviderBundleResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *ProviderBundleResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *ProviderBundleResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *ProviderBundleResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *ProviderBundleResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *ProviderBundleResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


