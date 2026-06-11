# AuditDecision

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Result** | [**AuditReason**](AuditReason.md) |  | 
**CaveatContext** | **map[string][]string** | Map from caveat NAME to the array of caveat-parameter NAMES referenced by the check. Values are never present on the wire — is structural: the only string content here is identifiers. &#x60;internal/audit.Entry&#x60; and &#x60;internal/audit.AppendInput&#x60; enforce the same discipline structurally on the Go side.  | 

## Methods

### NewAuditDecision

`func NewAuditDecision(result AuditReason, caveatContext map[string][]string, ) *AuditDecision`

NewAuditDecision instantiates a new AuditDecision object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewAuditDecisionWithDefaults

`func NewAuditDecisionWithDefaults() *AuditDecision`

NewAuditDecisionWithDefaults instantiates a new AuditDecision object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetResult

`func (o *AuditDecision) GetResult() AuditReason`

GetResult returns the Result field if non-nil, zero value otherwise.

### GetResultOk

`func (o *AuditDecision) GetResultOk() (*AuditReason, bool)`

GetResultOk returns a tuple with the Result field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetResult

`func (o *AuditDecision) SetResult(v AuditReason)`

SetResult sets Result field to given value.


### GetCaveatContext

`func (o *AuditDecision) GetCaveatContext() map[string][]string`

GetCaveatContext returns the CaveatContext field if non-nil, zero value otherwise.

### GetCaveatContextOk

`func (o *AuditDecision) GetCaveatContextOk() (*map[string][]string, bool)`

GetCaveatContextOk returns a tuple with the CaveatContext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaveatContext

`func (o *AuditDecision) SetCaveatContext(v map[string][]string)`

SetCaveatContext sets CaveatContext field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


