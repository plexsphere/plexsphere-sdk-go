# AuditChainVerifyResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ok** | **bool** | &#x60;true&#x60; when every row in the inspected segment hashes correctly and chains to its predecessor; &#x60;false&#x60; when the verifier observed a divergence at &#x60;divergent_seq&#x60;.  | 
**DivergentSeq** | Pointer to **int64** | Seq of the first row whose recomputed hash did not match the stored value, or whose &#x60;prev_hash&#x60; did not match the previous row&#39;s &#x60;entry_hash&#x60;. &#x60;null&#x60; on a clean run.  | [optional] 
**ExpectedHash** | Pointer to **string** | Hash the verifier computed for &#x60;divergent_seq&#x60;, lowercase hex. &#x60;null&#x60; on a clean run.  | [optional] 
**ObservedHash** | Pointer to **string** | Hash actually stored at &#x60;divergent_seq&#x60;, lowercase hex. &#x60;null&#x60; on a clean run.  | [optional] 
**SegmentFrom** | **int64** | Inclusive lower bound the verifier actually walked. | 
**SegmentTo** | **int64** | Inclusive upper bound the verifier actually walked. | 

## Methods

### NewAuditChainVerifyResult

`func NewAuditChainVerifyResult(ok bool, segmentFrom int64, segmentTo int64, ) *AuditChainVerifyResult`

NewAuditChainVerifyResult instantiates a new AuditChainVerifyResult object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditChainVerifyResultWithDefaults

`func NewAuditChainVerifyResultWithDefaults() *AuditChainVerifyResult`

NewAuditChainVerifyResultWithDefaults instantiates a new AuditChainVerifyResult object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetOk

`func (o *AuditChainVerifyResult) GetOk() bool`

GetOk returns the Ok field if non-nil, zero value otherwise.

### GetOkOk

`func (o *AuditChainVerifyResult) GetOkOk() (*bool, bool)`

GetOkOk returns a tuple with the Ok field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOk

`func (o *AuditChainVerifyResult) SetOk(v bool)`

SetOk sets Ok field to given value.


### GetDivergentSeq

`func (o *AuditChainVerifyResult) GetDivergentSeq() int64`

GetDivergentSeq returns the DivergentSeq field if non-nil, zero value otherwise.

### GetDivergentSeqOk

`func (o *AuditChainVerifyResult) GetDivergentSeqOk() (*int64, bool)`

GetDivergentSeqOk returns a tuple with the DivergentSeq field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDivergentSeq

`func (o *AuditChainVerifyResult) SetDivergentSeq(v int64)`

SetDivergentSeq sets DivergentSeq field to given value.

### HasDivergentSeq

`func (o *AuditChainVerifyResult) HasDivergentSeq() bool`

HasDivergentSeq returns a boolean if a field has been set.

### GetExpectedHash

`func (o *AuditChainVerifyResult) GetExpectedHash() string`

GetExpectedHash returns the ExpectedHash field if non-nil, zero value otherwise.

### GetExpectedHashOk

`func (o *AuditChainVerifyResult) GetExpectedHashOk() (*string, bool)`

GetExpectedHashOk returns a tuple with the ExpectedHash field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpectedHash

`func (o *AuditChainVerifyResult) SetExpectedHash(v string)`

SetExpectedHash sets ExpectedHash field to given value.

### HasExpectedHash

`func (o *AuditChainVerifyResult) HasExpectedHash() bool`

HasExpectedHash returns a boolean if a field has been set.

### GetObservedHash

`func (o *AuditChainVerifyResult) GetObservedHash() string`

GetObservedHash returns the ObservedHash field if non-nil, zero value otherwise.

### GetObservedHashOk

`func (o *AuditChainVerifyResult) GetObservedHashOk() (*string, bool)`

GetObservedHashOk returns a tuple with the ObservedHash field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetObservedHash

`func (o *AuditChainVerifyResult) SetObservedHash(v string)`

SetObservedHash sets ObservedHash field to given value.

### HasObservedHash

`func (o *AuditChainVerifyResult) HasObservedHash() bool`

HasObservedHash returns a boolean if a field has been set.

### GetSegmentFrom

`func (o *AuditChainVerifyResult) GetSegmentFrom() int64`

GetSegmentFrom returns the SegmentFrom field if non-nil, zero value otherwise.

### GetSegmentFromOk

`func (o *AuditChainVerifyResult) GetSegmentFromOk() (*int64, bool)`

GetSegmentFromOk returns a tuple with the SegmentFrom field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSegmentFrom

`func (o *AuditChainVerifyResult) SetSegmentFrom(v int64)`

SetSegmentFrom sets SegmentFrom field to given value.


### GetSegmentTo

`func (o *AuditChainVerifyResult) GetSegmentTo() int64`

GetSegmentTo returns the SegmentTo field if non-nil, zero value otherwise.

### GetSegmentToOk

`func (o *AuditChainVerifyResult) GetSegmentToOk() (*int64, bool)`

GetSegmentToOk returns a tuple with the SegmentTo field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSegmentTo

`func (o *AuditChainVerifyResult) SetSegmentTo(v int64)`

SetSegmentTo sets SegmentTo field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


