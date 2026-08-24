# ProviderBundleCloudRef

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CloudId** | **string** | Identifier of the referencing Cloud (UUIDv7). | 
**Slug** | **string** | Kebab-case URL handle of the referencing Cloud. | 
**DisplayName** | **string** | Human-readable name of the referencing Cloud. | 
**ProviderBundleVersion** | **int64** | The content version of the bundle this Cloud pins. Rows on one roster page may name different versions: a bundle patch publishes a new version and moves no Cloud, so each Cloud keeps the declaration it was last pinned to until a Cloud write moves that pin.  | 

## Methods

### NewProviderBundleCloudRef

`func NewProviderBundleCloudRef(cloudId string, slug string, displayName string, providerBundleVersion int64, ) *ProviderBundleCloudRef`

NewProviderBundleCloudRef instantiates a new ProviderBundleCloudRef object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewProviderBundleCloudRefWithDefaults

`func NewProviderBundleCloudRefWithDefaults() *ProviderBundleCloudRef`

NewProviderBundleCloudRefWithDefaults instantiates a new ProviderBundleCloudRef object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetCloudId

`func (o *ProviderBundleCloudRef) GetCloudId() string`

GetCloudId returns the CloudId field if non-nil, zero value otherwise.

### GetCloudIdOk

`func (o *ProviderBundleCloudRef) GetCloudIdOk() (*string, bool)`

GetCloudIdOk returns a tuple with the CloudId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudId

`func (o *ProviderBundleCloudRef) SetCloudId(v string)`

SetCloudId sets CloudId field to given value.


### GetSlug

`func (o *ProviderBundleCloudRef) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *ProviderBundleCloudRef) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *ProviderBundleCloudRef) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetDisplayName

`func (o *ProviderBundleCloudRef) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *ProviderBundleCloudRef) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *ProviderBundleCloudRef) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetProviderBundleVersion

`func (o *ProviderBundleCloudRef) GetProviderBundleVersion() int64`

GetProviderBundleVersion returns the ProviderBundleVersion field if non-nil, zero value otherwise.

### GetProviderBundleVersionOk

`func (o *ProviderBundleCloudRef) GetProviderBundleVersionOk() (*int64, bool)`

GetProviderBundleVersionOk returns a tuple with the ProviderBundleVersion field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProviderBundleVersion

`func (o *ProviderBundleCloudRef) SetProviderBundleVersion(v int64)`

SetProviderBundleVersion sets ProviderBundleVersion field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


