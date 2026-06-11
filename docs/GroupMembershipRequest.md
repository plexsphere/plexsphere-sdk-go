# GroupMembershipRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PrincipalId** | **string** | Principal identifier (UUIDv7). | 
**PrincipalKind** | [**GroupMembershipRequestPrincipalKind**](GroupMembershipRequestPrincipalKind.md) |  | 
**Source** | [**GroupMembershipRequestSource**](GroupMembershipRequestSource.md) |  | 

## Methods

### NewGroupMembershipRequest

`func NewGroupMembershipRequest(principalId string, principalKind GroupMembershipRequestPrincipalKind, source GroupMembershipRequestSource, ) *GroupMembershipRequest`

NewGroupMembershipRequest instantiates a new GroupMembershipRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupMembershipRequestWithDefaults

`func NewGroupMembershipRequestWithDefaults() *GroupMembershipRequest`

NewGroupMembershipRequestWithDefaults instantiates a new GroupMembershipRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPrincipalId

`func (o *GroupMembershipRequest) GetPrincipalId() string`

GetPrincipalId returns the PrincipalId field if non-nil, zero value otherwise.

### GetPrincipalIdOk

`func (o *GroupMembershipRequest) GetPrincipalIdOk() (*string, bool)`

GetPrincipalIdOk returns a tuple with the PrincipalId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrincipalId

`func (o *GroupMembershipRequest) SetPrincipalId(v string)`

SetPrincipalId sets PrincipalId field to given value.


### GetPrincipalKind

`func (o *GroupMembershipRequest) GetPrincipalKind() GroupMembershipRequestPrincipalKind`

GetPrincipalKind returns the PrincipalKind field if non-nil, zero value otherwise.

### GetPrincipalKindOk

`func (o *GroupMembershipRequest) GetPrincipalKindOk() (*GroupMembershipRequestPrincipalKind, bool)`

GetPrincipalKindOk returns a tuple with the PrincipalKind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrincipalKind

`func (o *GroupMembershipRequest) SetPrincipalKind(v GroupMembershipRequestPrincipalKind)`

SetPrincipalKind sets PrincipalKind field to given value.


### GetSource

`func (o *GroupMembershipRequest) GetSource() GroupMembershipRequestSource`

GetSource returns the Source field if non-nil, zero value otherwise.

### GetSourceOk

`func (o *GroupMembershipRequest) GetSourceOk() (*GroupMembershipRequestSource, bool)`

GetSourceOk returns a tuple with the Source field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSource

`func (o *GroupMembershipRequest) SetSource(v GroupMembershipRequestSource)`

SetSource sets Source field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


