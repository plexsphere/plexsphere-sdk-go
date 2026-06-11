# LabelSelectorPreviewRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Expression** | **string** | Raw label-selector expression (for example &#x60;env&#x3D;prod, owner in (alice, bob)&#x60;).  | 

## Methods

### NewLabelSelectorPreviewRequest

`func NewLabelSelectorPreviewRequest(expression string, ) *LabelSelectorPreviewRequest`

NewLabelSelectorPreviewRequest instantiates a new LabelSelectorPreviewRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelSelectorPreviewRequestWithDefaults

`func NewLabelSelectorPreviewRequestWithDefaults() *LabelSelectorPreviewRequest`

NewLabelSelectorPreviewRequestWithDefaults instantiates a new LabelSelectorPreviewRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetExpression

`func (o *LabelSelectorPreviewRequest) GetExpression() string`

GetExpression returns the Expression field if non-nil, zero value otherwise.

### GetExpressionOk

`func (o *LabelSelectorPreviewRequest) GetExpressionOk() (*string, bool)`

GetExpressionOk returns a tuple with the Expression field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetExpression

`func (o *LabelSelectorPreviewRequest) SetExpression(v string)`

SetExpression sets Expression field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


