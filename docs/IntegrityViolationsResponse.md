# IntegrityViolationsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AcceptedAt** | **time.Time** | Server-side timestamp at which the integrity-violations batch was committed.  | 
**ViolationCount** | **int32** | Number of &#x60;IntegrityViolation&#x60; rows persisted by this request. Matches the &#x60;violations&#x60; array length on input.  | 

## Methods

### NewIntegrityViolationsResponse

`func NewIntegrityViolationsResponse(acceptedAt time.Time, violationCount int32, ) *IntegrityViolationsResponse`

NewIntegrityViolationsResponse instantiates a new IntegrityViolationsResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewIntegrityViolationsResponseWithDefaults

`func NewIntegrityViolationsResponseWithDefaults() *IntegrityViolationsResponse`

NewIntegrityViolationsResponseWithDefaults instantiates a new IntegrityViolationsResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAcceptedAt

`func (o *IntegrityViolationsResponse) GetAcceptedAt() time.Time`

GetAcceptedAt returns the AcceptedAt field if non-nil, zero value otherwise.

### GetAcceptedAtOk

`func (o *IntegrityViolationsResponse) GetAcceptedAtOk() (*time.Time, bool)`

GetAcceptedAtOk returns a tuple with the AcceptedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAcceptedAt

`func (o *IntegrityViolationsResponse) SetAcceptedAt(v time.Time)`

SetAcceptedAt sets AcceptedAt field to given value.


### GetViolationCount

`func (o *IntegrityViolationsResponse) GetViolationCount() int32`

GetViolationCount returns the ViolationCount field if non-nil, zero value otherwise.

### GetViolationCountOk

`func (o *IntegrityViolationsResponse) GetViolationCountOk() (*int32, bool)`

GetViolationCountOk returns a tuple with the ViolationCount field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetViolationCount

`func (o *IntegrityViolationsResponse) SetViolationCount(v int32)`

SetViolationCount sets ViolationCount field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


