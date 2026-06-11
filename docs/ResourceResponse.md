# ResourceResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Resource identifier (UUIDv7). | 
**ProjectId** | **string** | Owning Project (UUIDv7) — exactly-one-parent rule.  | 
**DomainId** | **string** | Owning Domain (UUIDv7). Denormalised from the parent Project so cross-Domain checks do not have to reload the Project on every Resource read.  | 
**Kind** | **string** | Resource kind discriminator. | 
**ExternalRef** | Pointer to **string** | Optional external-system reference. &#x60;null&#x60; when the Resource declared none.  | [optional] 
**Origin** | [**ResourceOrigin**](ResourceOrigin.md) |  | 
**CreatedAt** | **time.Time** | Resource creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). | 
**Provisioning** | Pointer to [**ResourceProvisioning**](ResourceProvisioning.md) | Broker provisioning state. Present only on &#x60;Origin&#x3D;Provisioned&#x60; Resources; omitted on &#x60;Origin&#x3D;Adopted&#x60; Resources.  | [optional] 

## Methods

### NewResourceResponse

`func NewResourceResponse(id string, projectId string, domainId string, kind string, origin ResourceOrigin, createdAt time.Time, updatedAt time.Time, ) *ResourceResponse`

NewResourceResponse instantiates a new ResourceResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewResourceResponseWithDefaults

`func NewResourceResponseWithDefaults() *ResourceResponse`

NewResourceResponseWithDefaults instantiates a new ResourceResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *ResourceResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *ResourceResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *ResourceResponse) SetId(v string)`

SetId sets Id field to given value.


### GetProjectId

`func (o *ResourceResponse) GetProjectId() string`

GetProjectId returns the ProjectId field if non-nil, zero value otherwise.

### GetProjectIdOk

`func (o *ResourceResponse) GetProjectIdOk() (*string, bool)`

GetProjectIdOk returns a tuple with the ProjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProjectId

`func (o *ResourceResponse) SetProjectId(v string)`

SetProjectId sets ProjectId field to given value.


### GetDomainId

`func (o *ResourceResponse) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *ResourceResponse) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *ResourceResponse) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetKind

`func (o *ResourceResponse) GetKind() string`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *ResourceResponse) GetKindOk() (*string, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *ResourceResponse) SetKind(v string)`

SetKind sets Kind field to given value.


### GetExternalRef

`func (o *ResourceResponse) GetExternalRef() string`

GetExternalRef returns the ExternalRef field if non-nil, zero value otherwise.

### GetExternalRefOk

`func (o *ResourceResponse) GetExternalRefOk() (*string, bool)`

GetExternalRefOk returns a tuple with the ExternalRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExternalRef

`func (o *ResourceResponse) SetExternalRef(v string)`

SetExternalRef sets ExternalRef field to given value.

### HasExternalRef

`func (o *ResourceResponse) HasExternalRef() bool`

HasExternalRef returns a boolean if a field has been set.

### GetOrigin

`func (o *ResourceResponse) GetOrigin() ResourceOrigin`

GetOrigin returns the Origin field if non-nil, zero value otherwise.

### GetOriginOk

`func (o *ResourceResponse) GetOriginOk() (*ResourceOrigin, bool)`

GetOriginOk returns a tuple with the Origin field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOrigin

`func (o *ResourceResponse) SetOrigin(v ResourceOrigin)`

SetOrigin sets Origin field to given value.


### GetCreatedAt

`func (o *ResourceResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *ResourceResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *ResourceResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *ResourceResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *ResourceResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *ResourceResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.


### GetProvisioning

`func (o *ResourceResponse) GetProvisioning() ResourceProvisioning`

GetProvisioning returns the Provisioning field if non-nil, zero value otherwise.

### GetProvisioningOk

`func (o *ResourceResponse) GetProvisioningOk() (*ResourceProvisioning, bool)`

GetProvisioningOk returns a tuple with the Provisioning field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProvisioning

`func (o *ResourceResponse) SetProvisioning(v ResourceProvisioning)`

SetProvisioning sets Provisioning field to given value.

### HasProvisioning

`func (o *ResourceResponse) HasProvisioning() bool`

HasProvisioning returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


