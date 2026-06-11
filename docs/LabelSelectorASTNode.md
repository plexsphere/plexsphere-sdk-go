# LabelSelectorASTNode

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Op** | [**LabelSelectorASTNodeOp**](LabelSelectorASTNodeOp.md) |  | 
**Key** | Pointer to **string** | Label key the clause targets. Present for &#x60;eq&#x60;, &#x60;neq&#x60;, &#x60;in&#x60;, &#x60;exists&#x60;, &#x60;absent&#x60;. Absent for &#x60;and&#x60;.  | [optional] 
**Value** | Pointer to **string** | Value literal for &#x60;eq&#x60; and &#x60;neq&#x60;. | [optional] 
**Values** | Pointer to **[]string** | Value set for &#x60;in&#x60;. | [optional] 
**Children** | Pointer to [**[]LabelSelectorASTNode**](LabelSelectorASTNode.md) | AND children. | [optional] 

## Methods

### NewLabelSelectorASTNode

`func NewLabelSelectorASTNode(op LabelSelectorASTNodeOp, ) *LabelSelectorASTNode`

NewLabelSelectorASTNode instantiates a new LabelSelectorASTNode object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelSelectorASTNodeWithDefaults

`func NewLabelSelectorASTNodeWithDefaults() *LabelSelectorASTNode`

NewLabelSelectorASTNodeWithDefaults instantiates a new LabelSelectorASTNode object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetOp

`func (o *LabelSelectorASTNode) GetOp() LabelSelectorASTNodeOp`

GetOp returns the Op field if non-nil, zero value otherwise.

### GetOpOk

`func (o *LabelSelectorASTNode) GetOpOk() (*LabelSelectorASTNodeOp, bool)`

GetOpOk returns a tuple with the Op field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOp

`func (o *LabelSelectorASTNode) SetOp(v LabelSelectorASTNodeOp)`

SetOp sets Op field to given value.


### GetKey

`func (o *LabelSelectorASTNode) GetKey() string`

GetKey returns the Key field if non-nil, zero value otherwise.

### GetKeyOk

`func (o *LabelSelectorASTNode) GetKeyOk() (*string, bool)`

GetKeyOk returns a tuple with the Key field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKey

`func (o *LabelSelectorASTNode) SetKey(v string)`

SetKey sets Key field to given value.

### HasKey

`func (o *LabelSelectorASTNode) HasKey() bool`

HasKey returns a boolean if a field has been set.

### GetValue

`func (o *LabelSelectorASTNode) GetValue() string`

GetValue returns the Value field if non-nil, zero value otherwise.

### GetValueOk

`func (o *LabelSelectorASTNode) GetValueOk() (*string, bool)`

GetValueOk returns a tuple with the Value field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValue

`func (o *LabelSelectorASTNode) SetValue(v string)`

SetValue sets Value field to given value.

### HasValue

`func (o *LabelSelectorASTNode) HasValue() bool`

HasValue returns a boolean if a field has been set.

### GetValues

`func (o *LabelSelectorASTNode) GetValues() []string`

GetValues returns the Values field if non-nil, zero value otherwise.

### GetValuesOk

`func (o *LabelSelectorASTNode) GetValuesOk() (*[]string, bool)`

GetValuesOk returns a tuple with the Values field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValues

`func (o *LabelSelectorASTNode) SetValues(v []string)`

SetValues sets Values field to given value.

### HasValues

`func (o *LabelSelectorASTNode) HasValues() bool`

HasValues returns a boolean if a field has been set.

### GetChildren

`func (o *LabelSelectorASTNode) GetChildren() []LabelSelectorASTNode`

GetChildren returns the Children field if non-nil, zero value otherwise.

### GetChildrenOk

`func (o *LabelSelectorASTNode) GetChildrenOk() (*[]LabelSelectorASTNode, bool)`

GetChildrenOk returns a tuple with the Children field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetChildren

`func (o *LabelSelectorASTNode) SetChildren(v []LabelSelectorASTNode)`

SetChildren sets Children field to given value.

### HasChildren

`func (o *LabelSelectorASTNode) HasChildren() bool`

HasChildren returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


