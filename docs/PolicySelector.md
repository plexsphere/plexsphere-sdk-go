# PolicySelector

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Source** | **string** | Raw label-selector expression matching the originating side of governed traffic (e.g. &#x60;env&#x3D;prod, role in (api, web)&#x60;).  | 
**Destination** | **string** | Raw label-selector expression matching the terminating side of governed traffic.  | 

## Methods

### NewPolicySelector

`func NewPolicySelector(source string, destination string, ) *PolicySelector`

NewPolicySelector instantiates a new PolicySelector object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewPolicySelectorWithDefaults

`func NewPolicySelectorWithDefaults() *PolicySelector`

NewPolicySelectorWithDefaults instantiates a new PolicySelector object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetSource

`func (o *PolicySelector) GetSource() string`

GetSource returns the Source field if non-nil, zero value otherwise.

### GetSourceOk

`func (o *PolicySelector) GetSourceOk() (*string, bool)`

GetSourceOk returns a tuple with the Source field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSource

`func (o *PolicySelector) SetSource(v string)`

SetSource sets Source field to given value.


### GetDestination

`func (o *PolicySelector) GetDestination() string`

GetDestination returns the Destination field if non-nil, zero value otherwise.

### GetDestinationOk

`func (o *PolicySelector) GetDestinationOk() (*string, bool)`

GetDestinationOk returns a tuple with the Destination field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDestination

`func (o *PolicySelector) SetDestination(v string)`

SetDestination sets Destination field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


