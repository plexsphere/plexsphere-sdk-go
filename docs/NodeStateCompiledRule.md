# NodeStateCompiledRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Action** | [**PolicyAction**](PolicyAction.md) |  | 
**Protocol** | [**PolicyProtocol**](PolicyProtocol.md) |  | 
**SourceCidr** | **string** | IPv4 or IPv6 prefix in CIDR notation (e.g. &#x60;10.0.0.0/8&#x60;, &#x60;2001:db8::/32&#x60;). Source and destination agree on address family by aggregate-boundary invariant.  | 
**DestinationCidr** | **string** | IPv4 or IPv6 prefix in CIDR notation. Address family matches &#x60;source_cidr&#x60;.  | 
**Ports** | Pointer to [**PolicyPortRange**](PolicyPortRange.md) |  | [optional] 

## Methods

### NewNodeStateCompiledRule

`func NewNodeStateCompiledRule(action PolicyAction, protocol PolicyProtocol, sourceCidr string, destinationCidr string, ) *NodeStateCompiledRule`

NewNodeStateCompiledRule instantiates a new NodeStateCompiledRule object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewNodeStateCompiledRuleWithDefaults

`func NewNodeStateCompiledRuleWithDefaults() *NodeStateCompiledRule`

NewNodeStateCompiledRuleWithDefaults instantiates a new NodeStateCompiledRule object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAction

`func (o *NodeStateCompiledRule) GetAction() PolicyAction`

GetAction returns the Action field if non-nil, zero value otherwise.

### GetActionOk

`func (o *NodeStateCompiledRule) GetActionOk() (*PolicyAction, bool)`

GetActionOk returns a tuple with the Action field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAction

`func (o *NodeStateCompiledRule) SetAction(v PolicyAction)`

SetAction sets Action field to given value.


### GetProtocol

`func (o *NodeStateCompiledRule) GetProtocol() PolicyProtocol`

GetProtocol returns the Protocol field if non-nil, zero value otherwise.

### GetProtocolOk

`func (o *NodeStateCompiledRule) GetProtocolOk() (*PolicyProtocol, bool)`

GetProtocolOk returns a tuple with the Protocol field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetProtocol

`func (o *NodeStateCompiledRule) SetProtocol(v PolicyProtocol)`

SetProtocol sets Protocol field to given value.


### GetSourceCidr

`func (o *NodeStateCompiledRule) GetSourceCidr() string`

GetSourceCidr returns the SourceCidr field if non-nil, zero value otherwise.

### GetSourceCidrOk

`func (o *NodeStateCompiledRule) GetSourceCidrOk() (*string, bool)`

GetSourceCidrOk returns a tuple with the SourceCidr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSourceCidr

`func (o *NodeStateCompiledRule) SetSourceCidr(v string)`

SetSourceCidr sets SourceCidr field to given value.


### GetDestinationCidr

`func (o *NodeStateCompiledRule) GetDestinationCidr() string`

GetDestinationCidr returns the DestinationCidr field if non-nil, zero value otherwise.

### GetDestinationCidrOk

`func (o *NodeStateCompiledRule) GetDestinationCidrOk() (*string, bool)`

GetDestinationCidrOk returns a tuple with the DestinationCidr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDestinationCidr

`func (o *NodeStateCompiledRule) SetDestinationCidr(v string)`

SetDestinationCidr sets DestinationCidr field to given value.


### GetPorts

`func (o *NodeStateCompiledRule) GetPorts() PolicyPortRange`

GetPorts returns the Ports field if non-nil, zero value otherwise.

### GetPortsOk

`func (o *NodeStateCompiledRule) GetPortsOk() (*PolicyPortRange, bool)`

GetPortsOk returns a tuple with the Ports field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPorts

`func (o *NodeStateCompiledRule) SetPorts(v PolicyPortRange)`

SetPorts sets Ports field to given value.

### HasPorts

`func (o *NodeStateCompiledRule) HasPorts() bool`

HasPorts returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


