# NodeStatePolicy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RevisionId** | **string** | Identifier of the Policy revision the merged ruleset anchors on — drawn from the policy-id-ascending first row when the addressed Node matches multiple Policies. A Node matching a single Policy carries that Policy&#39;s revision id directly.  | 
**Fingerprint** | **string** | SHA-256 digest over the merged &#x60;rule_payload&#x60; byte stream the controller persisted in &#x60;plexsphere.policy_compiled_ruleset&#x60;. Exactly 32 bytes once decoded; on the wire the field is base64-encoded with standard padding (44 ASCII characters). For a Node matching a single Policy the digest equals &#x60;sha256.Sum256(rule_payload)&#x60;; for a Node matching multiple Policies it equals &#x60;sha256.Sum256(payload_0 || payload_1 || ...)&#x60; with &#x60;payload_i&#x60; ordered by ascending &#x60;policy_id&#x60;. The digest is an opaque comparison key — plexd compares it byte-for-byte against its locally-applied ruleset&#39;s stored digest and does not re-derive it from the &#x60;rules&#x60; array.  | 
**Rules** | [**[]NodeStateCompiledRule**](NodeStateCompiledRule.md) | Canonical, deterministically-sorted L3/L4 rule list the addressed Node MUST program. For multi-policy matches the array is the per-Policy concatenation of each row&#39;s canonical rule list in policy-id-ascending order. Empty array is a legitimate state — it means the Node matches at least one Policy&#39;s selector pair but no Policy contributed any rules (or every rule was filtered out).  | 

## Methods

### NewNodeStatePolicy

`func NewNodeStatePolicy(revisionId string, fingerprint string, rules []NodeStateCompiledRule, ) *NodeStatePolicy`

NewNodeStatePolicy instantiates a new NodeStatePolicy object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStatePolicyWithDefaults

`func NewNodeStatePolicyWithDefaults() *NodeStatePolicy`

NewNodeStatePolicyWithDefaults instantiates a new NodeStatePolicy object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetRevisionId

`func (o *NodeStatePolicy) GetRevisionId() string`

GetRevisionId returns the RevisionId field if non-nil, zero value otherwise.

### GetRevisionIdOk

`func (o *NodeStatePolicy) GetRevisionIdOk() (*string, bool)`

GetRevisionIdOk returns a tuple with the RevisionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRevisionId

`func (o *NodeStatePolicy) SetRevisionId(v string)`

SetRevisionId sets RevisionId field to given value.


### GetFingerprint

`func (o *NodeStatePolicy) GetFingerprint() string`

GetFingerprint returns the Fingerprint field if non-nil, zero value otherwise.

### GetFingerprintOk

`func (o *NodeStatePolicy) GetFingerprintOk() (*string, bool)`

GetFingerprintOk returns a tuple with the Fingerprint field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFingerprint

`func (o *NodeStatePolicy) SetFingerprint(v string)`

SetFingerprint sets Fingerprint field to given value.


### GetRules

`func (o *NodeStatePolicy) GetRules() []NodeStateCompiledRule`

GetRules returns the Rules field if non-nil, zero value otherwise.

### GetRulesOk

`func (o *NodeStatePolicy) GetRulesOk() (*[]NodeStateCompiledRule, bool)`

GetRulesOk returns a tuple with the Rules field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRules

`func (o *NodeStatePolicy) SetRules(v []NodeStateCompiledRule)`

SetRules sets Rules field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


