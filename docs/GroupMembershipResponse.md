# GroupMembershipResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GroupId** | **string** | Group identifier (UUIDv7). | 
**PrincipalId** | **string** | Principal identifier (UUIDv7). | 
**PrincipalKind** | [**GroupMembershipResponsePrincipalKind**](GroupMembershipResponsePrincipalKind.md) |  | 
**Source** | [**GroupMembershipResponseSource**](GroupMembershipResponseSource.md) |  | 
**CreatedAt** | **time.Time** |  | 

## Methods

### NewGroupMembershipResponse

`func NewGroupMembershipResponse(groupId string, principalId string, principalKind GroupMembershipResponsePrincipalKind, source GroupMembershipResponseSource, createdAt time.Time, ) *GroupMembershipResponse`

NewGroupMembershipResponse instantiates a new GroupMembershipResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewGroupMembershipResponseWithDefaults

`func NewGroupMembershipResponseWithDefaults() *GroupMembershipResponse`

NewGroupMembershipResponseWithDefaults instantiates a new GroupMembershipResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetGroupId

`func (o *GroupMembershipResponse) GetGroupId() string`

GetGroupId returns the GroupId field if non-nil, zero value otherwise.

### GetGroupIdOk

`func (o *GroupMembershipResponse) GetGroupIdOk() (*string, bool)`

GetGroupIdOk returns a tuple with the GroupId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetGroupId

`func (o *GroupMembershipResponse) SetGroupId(v string)`

SetGroupId sets GroupId field to given value.


### GetPrincipalId

`func (o *GroupMembershipResponse) GetPrincipalId() string`

GetPrincipalId returns the PrincipalId field if non-nil, zero value otherwise.

### GetPrincipalIdOk

`func (o *GroupMembershipResponse) GetPrincipalIdOk() (*string, bool)`

GetPrincipalIdOk returns a tuple with the PrincipalId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrincipalId

`func (o *GroupMembershipResponse) SetPrincipalId(v string)`

SetPrincipalId sets PrincipalId field to given value.


### GetPrincipalKind

`func (o *GroupMembershipResponse) GetPrincipalKind() GroupMembershipResponsePrincipalKind`

GetPrincipalKind returns the PrincipalKind field if non-nil, zero value otherwise.

### GetPrincipalKindOk

`func (o *GroupMembershipResponse) GetPrincipalKindOk() (*GroupMembershipResponsePrincipalKind, bool)`

GetPrincipalKindOk returns a tuple with the PrincipalKind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPrincipalKind

`func (o *GroupMembershipResponse) SetPrincipalKind(v GroupMembershipResponsePrincipalKind)`

SetPrincipalKind sets PrincipalKind field to given value.


### GetSource

`func (o *GroupMembershipResponse) GetSource() GroupMembershipResponseSource`

GetSource returns the Source field if non-nil, zero value otherwise.

### GetSourceOk

`func (o *GroupMembershipResponse) GetSourceOk() (*GroupMembershipResponseSource, bool)`

GetSourceOk returns a tuple with the Source field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSource

`func (o *GroupMembershipResponse) SetSource(v GroupMembershipResponseSource)`

SetSource sets Source field to given value.


### GetCreatedAt

`func (o *GroupMembershipResponse) GetCreatedAt() time.Time`

GetCreatedAt returns the CreatedAt field if non-nil, zero value otherwise.

### GetCreatedAtOk

`func (o *GroupMembershipResponse) GetCreatedAtOk() (*time.Time, bool)`

GetCreatedAtOk returns a tuple with the CreatedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCreatedAt

`func (o *GroupMembershipResponse) SetCreatedAt(v time.Time)`

SetCreatedAt sets CreatedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


