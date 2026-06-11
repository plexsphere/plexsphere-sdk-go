# PolicyDryRunResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MatchedNodeIds** | **[]string** |  | 
**RuleDiff** | [**PolicyDiff**](PolicyDiff.md) |  | 
**PeerPairsAffected** | **int32** |  | 
**UnreachableNodeIds** | **[]string** |  | 

## Methods

### NewPolicyDryRunResponse

`func NewPolicyDryRunResponse(matchedNodeIds []string, ruleDiff PolicyDiff, peerPairsAffected int32, unreachableNodeIds []string, ) *PolicyDryRunResponse`

NewPolicyDryRunResponse instantiates a new PolicyDryRunResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyDryRunResponseWithDefaults

`func NewPolicyDryRunResponseWithDefaults() *PolicyDryRunResponse`

NewPolicyDryRunResponseWithDefaults instantiates a new PolicyDryRunResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetMatchedNodeIds

`func (o *PolicyDryRunResponse) GetMatchedNodeIds() []string`

GetMatchedNodeIds returns the MatchedNodeIds field if non-nil, zero value otherwise.

### GetMatchedNodeIdsOk

`func (o *PolicyDryRunResponse) GetMatchedNodeIdsOk() (*[]string, bool)`

GetMatchedNodeIdsOk returns a tuple with the MatchedNodeIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMatchedNodeIds

`func (o *PolicyDryRunResponse) SetMatchedNodeIds(v []string)`

SetMatchedNodeIds sets MatchedNodeIds field to given value.


### GetRuleDiff

`func (o *PolicyDryRunResponse) GetRuleDiff() PolicyDiff`

GetRuleDiff returns the RuleDiff field if non-nil, zero value otherwise.

### GetRuleDiffOk

`func (o *PolicyDryRunResponse) GetRuleDiffOk() (*PolicyDiff, bool)`

GetRuleDiffOk returns a tuple with the RuleDiff field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRuleDiff

`func (o *PolicyDryRunResponse) SetRuleDiff(v PolicyDiff)`

SetRuleDiff sets RuleDiff field to given value.


### GetPeerPairsAffected

`func (o *PolicyDryRunResponse) GetPeerPairsAffected() int32`

GetPeerPairsAffected returns the PeerPairsAffected field if non-nil, zero value otherwise.

### GetPeerPairsAffectedOk

`func (o *PolicyDryRunResponse) GetPeerPairsAffectedOk() (*int32, bool)`

GetPeerPairsAffectedOk returns a tuple with the PeerPairsAffected field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPeerPairsAffected

`func (o *PolicyDryRunResponse) SetPeerPairsAffected(v int32)`

SetPeerPairsAffected sets PeerPairsAffected field to given value.


### GetUnreachableNodeIds

`func (o *PolicyDryRunResponse) GetUnreachableNodeIds() []string`

GetUnreachableNodeIds returns the UnreachableNodeIds field if non-nil, zero value otherwise.

### GetUnreachableNodeIdsOk

`func (o *PolicyDryRunResponse) GetUnreachableNodeIdsOk() (*[]string, bool)`

GetUnreachableNodeIdsOk returns a tuple with the UnreachableNodeIds field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetUnreachableNodeIds

`func (o *PolicyDryRunResponse) SetUnreachableNodeIds(v []string)`

SetUnreachableNodeIds sets UnreachableNodeIds field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


