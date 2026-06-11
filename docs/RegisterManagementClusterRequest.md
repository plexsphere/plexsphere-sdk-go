# RegisterManagementClusterRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Human-readable cluster name. | 
**Slug** | **string** | Unique human-facing shard key. Required and immutable once registered.  | 
**Region** | Pointer to **string** | Region the cluster serves. Optional; omit or send an empty string for a single unscoped cluster.  | [optional] 
**KubeconfigSecretRef** | **string** | Name of the Kubernetes Secret holding the cluster kubeconfig. This is a reference NAME only — no credential material crosses this surface.  | 
**Status** | Pointer to **string** | Initial lifecycle status string. Optional; defaults to &#x60;active&#x60; when omitted.  | [optional] 

## Methods

### NewRegisterManagementClusterRequest

`func NewRegisterManagementClusterRequest(name string, slug string, kubeconfigSecretRef string, ) *RegisterManagementClusterRequest`

NewRegisterManagementClusterRequest instantiates a new RegisterManagementClusterRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRegisterManagementClusterRequestWithDefaults

`func NewRegisterManagementClusterRequestWithDefaults() *RegisterManagementClusterRequest`

NewRegisterManagementClusterRequestWithDefaults instantiates a new RegisterManagementClusterRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *RegisterManagementClusterRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *RegisterManagementClusterRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *RegisterManagementClusterRequest) SetName(v string)`

SetName sets Name field to given value.


### GetSlug

`func (o *RegisterManagementClusterRequest) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *RegisterManagementClusterRequest) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *RegisterManagementClusterRequest) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetRegion

`func (o *RegisterManagementClusterRequest) GetRegion() string`

GetRegion returns the Region field if non-nil, zero value otherwise.

### GetRegionOk

`func (o *RegisterManagementClusterRequest) GetRegionOk() (*string, bool)`

GetRegionOk returns a tuple with the Region field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRegion

`func (o *RegisterManagementClusterRequest) SetRegion(v string)`

SetRegion sets Region field to given value.

### HasRegion

`func (o *RegisterManagementClusterRequest) HasRegion() bool`

HasRegion returns a boolean if a field has been set.

### GetKubeconfigSecretRef

`func (o *RegisterManagementClusterRequest) GetKubeconfigSecretRef() string`

GetKubeconfigSecretRef returns the KubeconfigSecretRef field if non-nil, zero value otherwise.

### GetKubeconfigSecretRefOk

`func (o *RegisterManagementClusterRequest) GetKubeconfigSecretRefOk() (*string, bool)`

GetKubeconfigSecretRefOk returns a tuple with the KubeconfigSecretRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKubeconfigSecretRef

`func (o *RegisterManagementClusterRequest) SetKubeconfigSecretRef(v string)`

SetKubeconfigSecretRef sets KubeconfigSecretRef field to given value.


### GetStatus

`func (o *RegisterManagementClusterRequest) GetStatus() string`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *RegisterManagementClusterRequest) GetStatusOk() (*string, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *RegisterManagementClusterRequest) SetStatus(v string)`

SetStatus sets Status field to given value.

### HasStatus

`func (o *RegisterManagementClusterRequest) HasStatus() bool`

HasStatus returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


