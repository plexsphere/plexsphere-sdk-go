# LabelDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Label Definition identifier (UUIDv7). | 
**Scope** | [**LabelDefinitionScope**](LabelDefinitionScope.md) |  | 
**ScopeId** | **string** | Tenancy identifier. Zero UUID when &#x60;scope&#x3D;platform&#x60;; non-zero Domain identifier when &#x60;scope&#x3D;domain&#x60;; non-zero Project identifier when &#x60;scope&#x3D;project&#x60;.  | 
**LocalKey** | **string** | Unqualified key token (for example &#x60;env&#x60;, &#x60;cost-center&#x60;).  | 
**QualifiedKey** | **string** | Fully namespaced key (for example &#x60;platform/env&#x60;, &#x60;acme:checkout/owner&#x60;). Unique across the platform.  | 
**ValueSchema** | [**LabelValueSchema**](LabelValueSchema.md) |  | 
**ApplicableKinds** | **[]string** | Lowercase object-kind whitelist (resource, node, project, domain, workload, network, …). Assignments whose &#x60;object.kind&#x60; is not in this set are rejected with &#x60;scope-mismatch&#x60;.  | 
**OnDelete** | [**LabelDefinitionOnDelete**](LabelDefinitionOnDelete.md) |  | 
**Cardinality** | **int32** | Declared per-object cardinality cap for Assignments of this Definition. &#x60;1&#x60; means at most one Assignment per object; &#x60;0&#x60; means unlimited (bounded only by the global 64-per-object ceiling).  | [default to 1]
**Immutable** | **bool** | When &#x60;true&#x60;, the value schema is frozen and Assignments of this Definition may not have their value replaced .  | 
**CloudTagPropagation** | **bool** | When &#x60;true&#x60;, matching cloud tags are synchronised onto cloud resources by the Provisioning Broker.  | 
**Description** | Pointer to **string** | Optional human description (at most 512 chars). | [optional] 
**CreatedBy** | [**LabelDefinitionCreatedBy**](LabelDefinitionCreatedBy.md) |  | 
**CreatedAt** | **time.Time** |  | 
**UpdatedAt** | **time.Time** |  | 

## Methods

### NewLabelDefinition

`func NewLabelDefinition(id string, scope LabelDefinitionScope, scopeId string, localKey string, qualifiedKey string, valueSchema LabelValueSchema, applicableKinds []string, onDelete LabelDefinitionOnDelete, cardinality int32, immutable bool, cloudTagPropagation bool, createdBy LabelDefinitionCreatedBy, createdAt time.Time, updatedAt time.Time, ) *LabelDefinition`

NewLabelDefinition instantiates a new LabelDefinition object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelDefinitionWithDefaults

`func NewLabelDefinitionWithDefaults() *LabelDefinition`

NewLabelDefinitionWithDefaults instantiates a new LabelDefinition object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *LabelDefinition) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *LabelDefinition) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *LabelDefinition) SetId(v string)`

SetId sets Id field to given value.


### GetScope

`func (o *LabelDefinition) GetScope() LabelDefinitionScope`

GetScope returns the Scope field if non-nil, zero value otherwise.

### GetScopeOk

`func (o *LabelDefinition) GetScopeOk() (*LabelDefinitionScope, bool)`

GetScopeOk returns a tuple with the Scope field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScope

`func (o *LabelDefinition) SetScope(v LabelDefinitionScope)`

SetScope sets Scope field to given value.


### GetScopeId

`func (o *LabelDefinition) GetScopeId() string`

GetScopeId returns the ScopeId field if non-nil, zero value otherwise.

### GetScopeIdOk

`func (o *LabelDefinition) GetScopeIdOk() (*string, bool)`

GetScopeIdOk returns a tuple with the ScopeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetScopeId

`func (o *LabelDefinition) SetScopeId(v string)`

SetScopeId sets ScopeId field to given value.


### GetLocalKey

`func (o *LabelDefinition) GetLocalKey() string`

GetLocalKey returns the LocalKey field if non-nil, zero value otherwise.

### GetLocalKeyOk

`func (o *LabelDefinition) GetLocalKeyOk() (*string, bool)`

GetLocalKeyOk returns a tuple with the LocalKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetLocalKey

`func (o *LabelDefinition) SetLocalKey(v string)`

SetLocalKey sets LocalKey field to given value.


### GetQualifiedKey

`func (o *LabelDefinition) GetQualifiedKey() string`

GetQualifiedKey returns the QualifiedKey field if non-nil, zero value otherwise.

### GetQualifiedKeyOk

`func (o *LabelDefinition) GetQualifiedKeyOk() (*string, bool)`

GetQualifiedKeyOk returns a tuple with the QualifiedKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetQualifiedKey

`func (o *LabelDefinition) SetQualifiedKey(v string)`

SetQualifiedKey sets QualifiedKey field to given value.


### GetValueSchema

`func (o *LabelDefinition) GetValueSchema() LabelValueSchema`

GetValueSchema returns the ValueSchema field if non-nil, zero value otherwise.

### GetValueSchemaOk

`func (o *LabelDefinition) GetValueSchemaOk() (*LabelValueSchema, bool)`

GetValueSchemaOk returns a tuple with the ValueSchema field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValueSchema

`func (o *LabelDefinition) SetValueSchema(v LabelValueSchema)`

SetValueSchema sets ValueSchema field to given value.


### GetApplicableKinds

`func (o *LabelDefinition) GetApplicableKinds() []string`

GetApplicableKinds returns the ApplicableKinds field if non-nil, zero value otherwise.

### GetApplicableKindsOk

`func (o *LabelDefinition) GetApplicableKindsOk() (*[]string, bool)`

GetApplicableKindsOk returns a tuple with the ApplicableKinds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetApplicableKinds

`func (o *LabelDefinition) SetApplicableKinds(v []string)`

SetApplicableKinds sets ApplicableKinds field to given value.


### GetOnDelete

`func (o *LabelDefinition) GetOnDelete() LabelDefinitionOnDelete`

GetOnDelete returns the OnDelete field if non-nil, zero value otherwise.

### GetOnDeleteOk

`func (o *LabelDefinition) GetOnDeleteOk() (*LabelDefinitionOnDelete, bool)`

GetOnDeleteOk returns a tuple with the OnDelete field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOnDelete

`func (o *LabelDefinition) SetOnDelete(v LabelDefinitionOnDelete)`

SetOnDelete sets OnDelete field to given value.


### GetCardinality

`func (o *LabelDefinition) GetCardinality() int32`

GetCardinality returns the Cardinality field if non-nil, zero value otherwise.

### GetCardinalityOk

`func (o *LabelDefinition) GetCardinalityOk() (*int32, bool)`

GetCardinalityOk returns a tuple with the Cardinality field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCardinality

`func (o *LabelDefinition) SetCardinality(v int32)`

SetCardinality sets Cardinality field to given value.


### GetImmutable

`func (o *LabelDefinition) GetImmutable() bool`

GetImmutable returns the Immutable field if non-nil, zero value otherwise.

### GetImmutableOk

`func (o *LabelDefinition) GetImmutableOk() (*bool, bool)`

GetImmutableOk returns a tuple with the Immutable field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetImmutable

`func (o *LabelDefinition) SetImmutable(v bool)`

SetImmutable sets Immutable field to given value.


### GetCloudTagPropagation

`func (o *LabelDefinition) GetCloudTagPropagation() bool`

GetCloudTagPropagation returns the CloudTagPropagation field if non-nil, zero value otherwise.

### GetCloudTagPropagationOk

`func (o *LabelDefinition) GetCloudTagPropagationOk() (*bool, bool)`

GetCloudTagPropagationOk returns a tuple with the CloudTagPropagation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCloudTagPropagation

`func (o *LabelDefinition) SetCloudTagPropagation(v bool)`

SetCloudTagPropagation sets CloudTagPropagation field to given value.


### GetDescription

`func (o *LabelDefinition) GetDescription() string`

GetDescription returns the Description field if non-nil, zero value otherwise.

### GetDescriptionOk

`func (o *LabelDefinition) GetDescriptionOk() (*string, bool)`

GetDescriptionOk returns a tuple with the Description field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDescription

`func (o *LabelDefinition) SetDescription(v string)`

SetDescription sets Description field to given value.

### HasDescription

`func (o *LabelDefinition) HasDescription() bool`

HasDescription returns a boolean if a field has been set.

### GetCreatedBy

`func (o *LabelDefinition) GetCreatedBy() LabelDefinitionCreatedBy`

GetCreatedBy returns the CreatedBy field if non-nil, zero value otherwise.

### GetCreatedByOk

`func (o *LabelDefinition) GetCreatedByOk() (*LabelDefinitionCreatedBy, bool)`

GetCreatedByOk returns a tuple with the CreatedBy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedBy

`func (o *LabelDefinition) SetCreatedBy(v LabelDefinitionCreatedBy)`

SetCreatedBy sets CreatedBy field to given value.


### GetCreatedAt

`func (o *LabelDefinition) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *LabelDefinition) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *LabelDefinition) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *LabelDefinition) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *LabelDefinition) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *LabelDefinition) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


