# NodeSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Node identifier (UUIDv7). | 
**Name** | Pointer to **string** | Human-readable Node name, sourced from the &#x60;Resource&#x60; aggregate the Node row references. Optional — see the schema-level note above for the deferred projection contract.  | [optional] 
**DomainId** | **string** | Parent Domain identifier (UUIDv7). | 
**Kind** | Pointer to **string** | Node kind discriminator, sourced from the &#x60;Resource&#x60; aggregate the Node row references. Today the cluster recognises &#x60;vm&#x60;, &#x60;bridge&#x60;, and &#x60;worker&#x60;; the field is intentionally modelled as an open string rather than an enum so a future kind addition does not require a contract version bump. Optional — see the schema-level note above for the deferred projection contract.  | [optional] 
**CreatedAt** | **time.Time** | Aggregate creation timestamp (UTC). | 

## Methods

### NewNodeSummary

`func NewNodeSummary(id string, domainId string, createdAt time.Time, ) *NodeSummary`

NewNodeSummary instantiates a new NodeSummary object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeSummaryWithDefaults

`func NewNodeSummaryWithDefaults() *NodeSummary`

NewNodeSummaryWithDefaults instantiates a new NodeSummary object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *NodeSummary) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *NodeSummary) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *NodeSummary) SetId(v string)`

SetId sets Id field to given value.


### GetName

`func (o *NodeSummary) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *NodeSummary) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *NodeSummary) SetName(v string)`

SetName sets Name field to given value.

### HasName

`func (o *NodeSummary) HasName() bool`

HasName returns a boolean if a field has been set.

### GetDomainId

`func (o *NodeSummary) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *NodeSummary) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *NodeSummary) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetKind

`func (o *NodeSummary) GetKind() string`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *NodeSummary) GetKindOk() (*string, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *NodeSummary) SetKind(v string)`

SetKind sets Kind field to given value.

### HasKind

`func (o *NodeSummary) HasKind() bool`

HasKind returns a boolean if a field has been set.

### GetCreatedAt

`func (o *NodeSummary) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *NodeSummary) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *NodeSummary) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


