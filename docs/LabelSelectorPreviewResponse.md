# LabelSelectorPreviewResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ast** | Pointer to [**LabelSelectorASTNode**](LabelSelectorASTNode.md) | Parsed AST root, when parsing succeeded. | [optional] 
**Errors** | Pointer to [**[]LabelSelectorError**](LabelSelectorError.md) | Parse errors, when parsing failed. | [optional] 

## Methods

### NewLabelSelectorPreviewResponse

`func NewLabelSelectorPreviewResponse() *LabelSelectorPreviewResponse`

NewLabelSelectorPreviewResponse instantiates a new LabelSelectorPreviewResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelSelectorPreviewResponseWithDefaults

`func NewLabelSelectorPreviewResponseWithDefaults() *LabelSelectorPreviewResponse`

NewLabelSelectorPreviewResponseWithDefaults instantiates a new LabelSelectorPreviewResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetAst

`func (o *LabelSelectorPreviewResponse) GetAst() LabelSelectorASTNode`

GetAst returns the Ast field if non-nil, zero value otherwise.

### GetAstOk

`func (o *LabelSelectorPreviewResponse) GetAstOk() (*LabelSelectorASTNode, bool)`

GetAstOk returns a tuple with the Ast field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAst

`func (o *LabelSelectorPreviewResponse) SetAst(v LabelSelectorASTNode)`

SetAst sets Ast field to given value.

### HasAst

`func (o *LabelSelectorPreviewResponse) HasAst() bool`

HasAst returns a boolean if a field has been set.

### GetErrors

`func (o *LabelSelectorPreviewResponse) GetErrors() []LabelSelectorError`

GetErrors returns the Errors field if non-nil, zero value otherwise.

### GetErrorsOk

`func (o *LabelSelectorPreviewResponse) GetErrorsOk() (*[]LabelSelectorError, bool)`

GetErrorsOk returns a tuple with the Errors field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetErrors

`func (o *LabelSelectorPreviewResponse) SetErrors(v []LabelSelectorError)`

SetErrors sets Errors field to given value.

### HasErrors

`func (o *LabelSelectorPreviewResponse) HasErrors() bool`

HasErrors returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


