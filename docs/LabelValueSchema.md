# LabelValueSchema

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | [**ValueSchemaKind**](ValueSchemaKind.md) |  | 
**MaxLen** | Pointer to **int32** | Maximum byte length for &#x60;kind&#x3D;string&#x60; (default 256 when omitted; 0 is equivalent to the default).  | [optional] 
**Values** | Pointer to **[]string** | Permitted string values for &#x60;kind&#x3D;enum&#x60;. Non-empty, unique, non-blank.  | [optional] 
**Min** | Pointer to **int64** | Inclusive lower bound for &#x60;kind&#x3D;numeric&#x60;. Omit for an open lower bound.  | [optional] 
**Max** | Pointer to **int64** | Inclusive upper bound for &#x60;kind&#x3D;numeric&#x60;. Omit for an open upper bound.  | [optional] 
**Pattern** | Pointer to **string** | Go regexp pattern for &#x60;kind&#x3D;regex&#x60;. Compiled at aggregate build time; malformed patterns are rejected.  | [optional] 

## Methods

### NewLabelValueSchema

`func NewLabelValueSchema(kind ValueSchemaKind, ) *LabelValueSchema`

NewLabelValueSchema instantiates a new LabelValueSchema object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelValueSchemaWithDefaults

`func NewLabelValueSchemaWithDefaults() *LabelValueSchema`

NewLabelValueSchemaWithDefaults instantiates a new LabelValueSchema object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKind

`func (o *LabelValueSchema) GetKind() ValueSchemaKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *LabelValueSchema) GetKindOk() (*ValueSchemaKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *LabelValueSchema) SetKind(v ValueSchemaKind)`

SetKind sets Kind field to given value.


### GetMaxLen

`func (o *LabelValueSchema) GetMaxLen() int32`

GetMaxLen returns the MaxLen field if non-nil, zero value otherwise.

### GetMaxLenOk

`func (o *LabelValueSchema) GetMaxLenOk() (*int32, bool)`

GetMaxLenOk returns a tuple with the MaxLen field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMaxLen

`func (o *LabelValueSchema) SetMaxLen(v int32)`

SetMaxLen sets MaxLen field to given value.

### HasMaxLen

`func (o *LabelValueSchema) HasMaxLen() bool`

HasMaxLen returns a boolean if a field has been set.

### GetValues

`func (o *LabelValueSchema) GetValues() []string`

GetValues returns the Values field if non-nil, zero value otherwise.

### GetValuesOk

`func (o *LabelValueSchema) GetValuesOk() (*[]string, bool)`

GetValuesOk returns a tuple with the Values field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValues

`func (o *LabelValueSchema) SetValues(v []string)`

SetValues sets Values field to given value.

### HasValues

`func (o *LabelValueSchema) HasValues() bool`

HasValues returns a boolean if a field has been set.

### GetMin

`func (o *LabelValueSchema) GetMin() int64`

GetMin returns the Min field if non-nil, zero value otherwise.

### GetMinOk

`func (o *LabelValueSchema) GetMinOk() (*int64, bool)`

GetMinOk returns a tuple with the Min field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMin

`func (o *LabelValueSchema) SetMin(v int64)`

SetMin sets Min field to given value.

### HasMin

`func (o *LabelValueSchema) HasMin() bool`

HasMin returns a boolean if a field has been set.

### GetMax

`func (o *LabelValueSchema) GetMax() int64`

GetMax returns the Max field if non-nil, zero value otherwise.

### GetMaxOk

`func (o *LabelValueSchema) GetMaxOk() (*int64, bool)`

GetMaxOk returns a tuple with the Max field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMax

`func (o *LabelValueSchema) SetMax(v int64)`

SetMax sets Max field to given value.

### HasMax

`func (o *LabelValueSchema) HasMax() bool`

HasMax returns a boolean if a field has been set.

### GetPattern

`func (o *LabelValueSchema) GetPattern() string`

GetPattern returns the Pattern field if non-nil, zero value otherwise.

### GetPatternOk

`func (o *LabelValueSchema) GetPatternOk() (*string, bool)`

GetPatternOk returns a tuple with the Pattern field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPattern

`func (o *LabelValueSchema) SetPattern(v string)`

SetPattern sets Pattern field to given value.

### HasPattern

`func (o *LabelValueSchema) HasPattern() bool`

HasPattern returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


