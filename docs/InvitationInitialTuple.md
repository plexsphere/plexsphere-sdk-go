# InvitationInitialTuple

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Relation** | **string** | SpiceDB relation the tuple grants on &#x60;object&#x60; (e.g. &#x60;member&#x60;, &#x60;viewer&#x60;). Whitespace-only is rejected by the aggregate.  | 
**Object** | **string** | SpiceDB object reference the tuple targets. Allowed prefix set is closed: &#x60;domain:&lt;this-domain-id&gt;&#x60;, &#x60;project:&lt;uuid&gt;&#x60;, or &#x60;group:&lt;uuid&gt;&#x60;. The handler validates the prefix BEFORE the aggregate constructor so an out-of- scope object surfaces as &#x60;422 invitation_object_out_of_scope&#x60; rather than a generic &#x60;invalid_body&#x60;.  | 
**CaveatContext** | Pointer to **map[string]interface{}** | Optional CEL caveat context forwarded verbatim to SpiceDB on accept. The aggregate enforces JSON-encodable lossless round-trip — a value that fails the round-trip surfaces as &#x60;422 invalid_caveat_context&#x60;.  | [optional] 

## Methods

### NewInvitationInitialTuple

`func NewInvitationInitialTuple(relation string, object string, ) *InvitationInitialTuple`

NewInvitationInitialTuple instantiates a new InvitationInitialTuple object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewInvitationInitialTupleWithDefaults

`func NewInvitationInitialTupleWithDefaults() *InvitationInitialTuple`

NewInvitationInitialTupleWithDefaults instantiates a new InvitationInitialTuple object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetRelation

`func (o *InvitationInitialTuple) GetRelation() string`

GetRelation returns the Relation field if non-nil, zero value otherwise.

### GetRelationOk

`func (o *InvitationInitialTuple) GetRelationOk() (*string, bool)`

GetRelationOk returns a tuple with the Relation field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRelation

`func (o *InvitationInitialTuple) SetRelation(v string)`

SetRelation sets Relation field to given value.


### GetObject

`func (o *InvitationInitialTuple) GetObject() string`

GetObject returns the Object field if non-nil, zero value otherwise.

### GetObjectOk

`func (o *InvitationInitialTuple) GetObjectOk() (*string, bool)`

GetObjectOk returns a tuple with the Object field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetObject

`func (o *InvitationInitialTuple) SetObject(v string)`

SetObject sets Object field to given value.


### GetCaveatContext

`func (o *InvitationInitialTuple) GetCaveatContext() map[string]interface{}`

GetCaveatContext returns the CaveatContext field if non-nil, zero value otherwise.

### GetCaveatContextOk

`func (o *InvitationInitialTuple) GetCaveatContextOk() (*map[string]interface{}, bool)`

GetCaveatContextOk returns a tuple with the CaveatContext field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCaveatContext

`func (o *InvitationInitialTuple) SetCaveatContext(v map[string]interface{})`

SetCaveatContext sets CaveatContext field to given value.

### HasCaveatContext

`func (o *InvitationInitialTuple) HasCaveatContext() bool`

HasCaveatContext returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


