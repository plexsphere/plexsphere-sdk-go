# ResourceCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Origin** | [**ResourceOrigin**](ResourceOrigin.md) |  | 
**Kind** | **string** | Resource kind discriminator. Trimmed and bounded by the tenancy aggregate&#39;s &#x60;resourceKindMaxLen&#x60;.  | 
**ExternalRef** | Pointer to **string** | Optional external-system reference for the adopted flow (URN, ARN, vendor-opaque id). Trimmed; whitespace-only is rejected. Omit on the provisioned flow.  | [optional] 
**BlueprintVersionId** | Pointer to **string** | BlueprintVersion the broker should render. REQUIRED on &#x60;origin&#x3D;provisioned&#x60;; omit on &#x60;origin&#x3D;adopted&#x60;. A missing version row surfaces as &#x60;422&#x60; with &#x60;code: blueprint_not_found&#x60;.  | [optional] 
**CloudCredentialId** | Pointer to **string** | Cloud Credential the broker uses to provision the substrate. REQUIRED on &#x60;origin&#x3D;provisioned&#x60;; omit on &#x60;origin&#x3D;adopted&#x60;. A missing credential row surfaces as &#x60;422&#x60; with &#x60;code: cloud_credential_not_found&#x60;.  | [optional] 
**Parameters** | Pointer to **map[string]interface{}** | Typed parameter values for &#x60;origin&#x3D;provisioned&#x60;, validated against the BlueprintVersion&#39;s typed &#x60;parameter_schema&#x60;. Omit on &#x60;origin&#x3D;adopted&#x60;. The wire envelope is opaque here; type-shape rejections surface at the handler.  | [optional] 

## Methods

### NewResourceCreateRequest

`func NewResourceCreateRequest(origin ResourceOrigin, kind string, ) *ResourceCreateRequest`

NewResourceCreateRequest instantiates a new ResourceCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewResourceCreateRequestWithDefaults

`func NewResourceCreateRequestWithDefaults() *ResourceCreateRequest`

NewResourceCreateRequestWithDefaults instantiates a new ResourceCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetOrigin

`func (o *ResourceCreateRequest) GetOrigin() ResourceOrigin`

GetOrigin returns the Origin field if non-nil, zero value otherwise.

### GetOriginOk

`func (o *ResourceCreateRequest) GetOriginOk() (*ResourceOrigin, bool)`

GetOriginOk returns a tuple with the Origin field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrigin

`func (o *ResourceCreateRequest) SetOrigin(v ResourceOrigin)`

SetOrigin sets Origin field to given value.


### GetKind

`func (o *ResourceCreateRequest) GetKind() string`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *ResourceCreateRequest) GetKindOk() (*string, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *ResourceCreateRequest) SetKind(v string)`

SetKind sets Kind field to given value.


### GetExternalRef

`func (o *ResourceCreateRequest) GetExternalRef() string`

GetExternalRef returns the ExternalRef field if non-nil, zero value otherwise.

### GetExternalRefOk

`func (o *ResourceCreateRequest) GetExternalRefOk() (*string, bool)`

GetExternalRefOk returns a tuple with the ExternalRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExternalRef

`func (o *ResourceCreateRequest) SetExternalRef(v string)`

SetExternalRef sets ExternalRef field to given value.

### HasExternalRef

`func (o *ResourceCreateRequest) HasExternalRef() bool`

HasExternalRef returns a boolean if a field has been set.

### GetBlueprintVersionId

`func (o *ResourceCreateRequest) GetBlueprintVersionId() string`

GetBlueprintVersionId returns the BlueprintVersionId field if non-nil, zero value otherwise.

### GetBlueprintVersionIdOk

`func (o *ResourceCreateRequest) GetBlueprintVersionIdOk() (*string, bool)`

GetBlueprintVersionIdOk returns a tuple with the BlueprintVersionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBlueprintVersionId

`func (o *ResourceCreateRequest) SetBlueprintVersionId(v string)`

SetBlueprintVersionId sets BlueprintVersionId field to given value.

### HasBlueprintVersionId

`func (o *ResourceCreateRequest) HasBlueprintVersionId() bool`

HasBlueprintVersionId returns a boolean if a field has been set.

### GetCloudCredentialId

`func (o *ResourceCreateRequest) GetCloudCredentialId() string`

GetCloudCredentialId returns the CloudCredentialId field if non-nil, zero value otherwise.

### GetCloudCredentialIdOk

`func (o *ResourceCreateRequest) GetCloudCredentialIdOk() (*string, bool)`

GetCloudCredentialIdOk returns a tuple with the CloudCredentialId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudCredentialId

`func (o *ResourceCreateRequest) SetCloudCredentialId(v string)`

SetCloudCredentialId sets CloudCredentialId field to given value.

### HasCloudCredentialId

`func (o *ResourceCreateRequest) HasCloudCredentialId() bool`

HasCloudCredentialId returns a boolean if a field has been set.

### GetParameters

`func (o *ResourceCreateRequest) GetParameters() map[string]interface{}`

GetParameters returns the Parameters field if non-nil, zero value otherwise.

### GetParametersOk

`func (o *ResourceCreateRequest) GetParametersOk() (*map[string]interface{}, bool)`

GetParametersOk returns a tuple with the Parameters field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetParameters

`func (o *ResourceCreateRequest) SetParameters(v map[string]interface{})`

SetParameters sets Parameters field to given value.

### HasParameters

`func (o *ResourceCreateRequest) HasParameters() bool`

HasParameters returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


