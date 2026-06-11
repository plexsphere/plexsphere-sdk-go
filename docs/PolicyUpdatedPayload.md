# PolicyUpdatedPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NodeId** | **string** | Addressed Node the compiled-ruleset projection targets. Equals the &#x60;{id}&#x60; path parameter of the SSE subscription the envelope is delivered on.  | 
**PolicyId** | **string** | Identifier of the Policy aggregate the compiled-ruleset row was projected from. Two Policies addressing the same Node produce two envelopes carrying distinct &#x60;policy_id&#x60; values; the consumer merges them by sorting on &#x60;policy_id&#x60; ascending.  | 
**RevisionId** | **string** | Identifier of the Policy revision the compiled ruleset anchors on. Equals the head revision id at compile time; re-emission for the same revision is idempotent under the publisher&#39;s deduplication window.  | 
**Fingerprint** | **string** | SHA-256 digest over the canonical &#x60;rule_payload&#x60; byte stream the controller persisted. Exactly 32 bytes once decoded; on the wire the field is base64-encoded with standard padding (44 ASCII characters). The digest is an opaque comparison key — plexd compares it byte-for-byte against its locally-applied ruleset&#39;s stored digest and does not re-derive it from the &#x60;rules&#x60; array.  | 
**Rules** | [**[]NodeStateCompiledRule**](NodeStateCompiledRule.md) | Canonical, deterministically-sorted L3/L4 rule list the addressed Node MUST program for the named Policy. An empty array is a legitimate state — it means the Node no longer matches the Policy (e.g. the Policy was deleted or its selector no longer captures the Node).  | 

## Methods

### NewPolicyUpdatedPayload

`func NewPolicyUpdatedPayload(nodeId string, policyId string, revisionId string, fingerprint string, rules []NodeStateCompiledRule, ) *PolicyUpdatedPayload`

NewPolicyUpdatedPayload instantiates a new PolicyUpdatedPayload object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicyUpdatedPayloadWithDefaults

`func NewPolicyUpdatedPayloadWithDefaults() *PolicyUpdatedPayload`

NewPolicyUpdatedPayloadWithDefaults instantiates a new PolicyUpdatedPayload object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNodeId

`func (o *PolicyUpdatedPayload) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *PolicyUpdatedPayload) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *PolicyUpdatedPayload) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetPolicyId

`func (o *PolicyUpdatedPayload) GetPolicyId() string`

GetPolicyId returns the PolicyId field if non-nil, zero value otherwise.

### GetPolicyIdOk

`func (o *PolicyUpdatedPayload) GetPolicyIdOk() (*string, bool)`

GetPolicyIdOk returns a tuple with the PolicyId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPolicyId

`func (o *PolicyUpdatedPayload) SetPolicyId(v string)`

SetPolicyId sets PolicyId field to given value.


### GetRevisionId

`func (o *PolicyUpdatedPayload) GetRevisionId() string`

GetRevisionId returns the RevisionId field if non-nil, zero value otherwise.

### GetRevisionIdOk

`func (o *PolicyUpdatedPayload) GetRevisionIdOk() (*string, bool)`

GetRevisionIdOk returns a tuple with the RevisionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevisionId

`func (o *PolicyUpdatedPayload) SetRevisionId(v string)`

SetRevisionId sets RevisionId field to given value.


### GetFingerprint

`func (o *PolicyUpdatedPayload) GetFingerprint() string`

GetFingerprint returns the Fingerprint field if non-nil, zero value otherwise.

### GetFingerprintOk

`func (o *PolicyUpdatedPayload) GetFingerprintOk() (*string, bool)`

GetFingerprintOk returns a tuple with the Fingerprint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFingerprint

`func (o *PolicyUpdatedPayload) SetFingerprint(v string)`

SetFingerprint sets Fingerprint field to given value.


### GetRules

`func (o *PolicyUpdatedPayload) GetRules() []NodeStateCompiledRule`

GetRules returns the Rules field if non-nil, zero value otherwise.

### GetRulesOk

`func (o *PolicyUpdatedPayload) GetRulesOk() (*[]NodeStateCompiledRule, bool)`

GetRulesOk returns a tuple with the Rules field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRules

`func (o *PolicyUpdatedPayload) SetRules(v []NodeStateCompiledRule)`

SetRules sets Rules field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


