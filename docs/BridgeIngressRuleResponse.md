# BridgeIngressRuleResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Rule identifier (UUIDv7). | 
**Slug** | **string** | Stable identity of the rule within its Resource. | 
**SniHost** | **string** | TLS SNI host the rule terminates. | 
**TargetNodeId** | **string** | Node the rule forwards to. | 
**TargetPort** | **int32** | TCP port on the target Node. | 
**AcmeAccountRef** | Pointer to **string** | Opaque reference to the ACME account used to issue the rule&#39;s certificate. &#x60;null&#x60; when the operator supplies certificates out of band.  | [optional] 
**CreatedAt** | **time.Time** | Rule creation timestamp (UTC). | 
**UpdatedAt** | **time.Time** | Last-modified timestamp (UTC). | 

## Methods

### NewBridgeIngressRuleResponse

`func NewBridgeIngressRuleResponse(id string, slug string, sniHost string, targetNodeId string, targetPort int32, createdAt time.Time, updatedAt time.Time, ) *BridgeIngressRuleResponse`

NewBridgeIngressRuleResponse instantiates a new BridgeIngressRuleResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewBridgeIngressRuleResponseWithDefaults

`func NewBridgeIngressRuleResponseWithDefaults() *BridgeIngressRuleResponse`

NewBridgeIngressRuleResponseWithDefaults instantiates a new BridgeIngressRuleResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *BridgeIngressRuleResponse) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *BridgeIngressRuleResponse) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *BridgeIngressRuleResponse) SetId(v string)`

SetId sets Id field to given value.


### GetSlug

`func (o *BridgeIngressRuleResponse) GetSlug() string`

GetSlug returns the Slug field if non-nil, zero value otherwise.

### GetSlugOk

`func (o *BridgeIngressRuleResponse) GetSlugOk() (*string, bool)`

GetSlugOk returns a tuple with the Slug field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSlug

`func (o *BridgeIngressRuleResponse) SetSlug(v string)`

SetSlug sets Slug field to given value.


### GetSniHost

`func (o *BridgeIngressRuleResponse) GetSniHost() string`

GetSniHost returns the SniHost field if non-nil, zero value otherwise.

### GetSniHostOk

`func (o *BridgeIngressRuleResponse) GetSniHostOk() (*string, bool)`

GetSniHostOk returns a tuple with the SniHost field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSniHost

`func (o *BridgeIngressRuleResponse) SetSniHost(v string)`

SetSniHost sets SniHost field to given value.


### GetTargetNodeId

`func (o *BridgeIngressRuleResponse) GetTargetNodeId() string`

GetTargetNodeId returns the TargetNodeId field if non-nil, zero value otherwise.

### GetTargetNodeIdOk

`func (o *BridgeIngressRuleResponse) GetTargetNodeIdOk() (*string, bool)`

GetTargetNodeIdOk returns a tuple with the TargetNodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetNodeId

`func (o *BridgeIngressRuleResponse) SetTargetNodeId(v string)`

SetTargetNodeId sets TargetNodeId field to given value.


### GetTargetPort

`func (o *BridgeIngressRuleResponse) GetTargetPort() int32`

GetTargetPort returns the TargetPort field if non-nil, zero value otherwise.

### GetTargetPortOk

`func (o *BridgeIngressRuleResponse) GetTargetPortOk() (*int32, bool)`

GetTargetPortOk returns a tuple with the TargetPort field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTargetPort

`func (o *BridgeIngressRuleResponse) SetTargetPort(v int32)`

SetTargetPort sets TargetPort field to given value.


### GetAcmeAccountRef

`func (o *BridgeIngressRuleResponse) GetAcmeAccountRef() string`

GetAcmeAccountRef returns the AcmeAccountRef field if non-nil, zero value otherwise.

### GetAcmeAccountRefOk

`func (o *BridgeIngressRuleResponse) GetAcmeAccountRefOk() (*string, bool)`

GetAcmeAccountRefOk returns a tuple with the AcmeAccountRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcmeAccountRef

`func (o *BridgeIngressRuleResponse) SetAcmeAccountRef(v string)`

SetAcmeAccountRef sets AcmeAccountRef field to given value.

### HasAcmeAccountRef

`func (o *BridgeIngressRuleResponse) HasAcmeAccountRef() bool`

HasAcmeAccountRef returns a boolean if a field has been set.

### GetCreatedAt

`func (o *BridgeIngressRuleResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *BridgeIngressRuleResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *BridgeIngressRuleResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.


### GetUpdatedAt

`func (o *BridgeIngressRuleResponse) GetUpdatedAt() time.Time`

GetUpdatedAt returns the UpdatedAt field if non-nil, zero value otherwise.

### GetUpdatedAtOk

`func (o *BridgeIngressRuleResponse) GetUpdatedAtOk() (*time.Time, bool)`

GetUpdatedAtOk returns a tuple with the UpdatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUpdatedAt

`func (o *BridgeIngressRuleResponse) SetUpdatedAt(v time.Time)`

SetUpdatedAt sets UpdatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


