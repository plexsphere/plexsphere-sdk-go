# AuditChainVerifyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FromSeq** | Pointer to **int64** | Inclusive lower bound on &#x60;seq&#x60;. Defaults to &#x60;1&#x60; when absent — i.e. the genesis row.  | [optional] 
**ToSeq** | Pointer to **int64** | Inclusive upper bound on &#x60;seq&#x60;. Defaults to the current chain head when absent.  | [optional] 

## Methods

### NewAuditChainVerifyRequest

`func NewAuditChainVerifyRequest() *AuditChainVerifyRequest`

NewAuditChainVerifyRequest instantiates a new AuditChainVerifyRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditChainVerifyRequestWithDefaults

`func NewAuditChainVerifyRequestWithDefaults() *AuditChainVerifyRequest`

NewAuditChainVerifyRequestWithDefaults instantiates a new AuditChainVerifyRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetFromSeq

`func (o *AuditChainVerifyRequest) GetFromSeq() int64`

GetFromSeq returns the FromSeq field if non-nil, zero value otherwise.

### GetFromSeqOk

`func (o *AuditChainVerifyRequest) GetFromSeqOk() (*int64, bool)`

GetFromSeqOk returns a tuple with the FromSeq field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFromSeq

`func (o *AuditChainVerifyRequest) SetFromSeq(v int64)`

SetFromSeq sets FromSeq field to given value.

### HasFromSeq

`func (o *AuditChainVerifyRequest) HasFromSeq() bool`

HasFromSeq returns a boolean if a field has been set.

### GetToSeq

`func (o *AuditChainVerifyRequest) GetToSeq() int64`

GetToSeq returns the ToSeq field if non-nil, zero value otherwise.

### GetToSeqOk

`func (o *AuditChainVerifyRequest) GetToSeqOk() (*int64, bool)`

GetToSeqOk returns a tuple with the ToSeq field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetToSeq

`func (o *AuditChainVerifyRequest) SetToSeq(v int64)`

SetToSeq sets ToSeq field to given value.

### HasToSeq

`func (o *AuditChainVerifyRequest) HasToSeq() bool`

HasToSeq returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


