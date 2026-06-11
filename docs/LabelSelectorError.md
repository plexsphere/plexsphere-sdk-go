# LabelSelectorError

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Position** | **int32** | Byte offset of the offending token. | 
**Message** | **string** | Human-readable error detail. | 

## Methods

### NewLabelSelectorError

`func NewLabelSelectorError(position int32, message string, ) *LabelSelectorError`

NewLabelSelectorError instantiates a new LabelSelectorError object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelSelectorErrorWithDefaults

`func NewLabelSelectorErrorWithDefaults() *LabelSelectorError`

NewLabelSelectorErrorWithDefaults instantiates a new LabelSelectorError object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetPosition

`func (o *LabelSelectorError) GetPosition() int32`

GetPosition returns the Position field if non-nil, zero value otherwise.

### GetPositionOk

`func (o *LabelSelectorError) GetPositionOk() (*int32, bool)`

GetPositionOk returns a tuple with the Position field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPosition

`func (o *LabelSelectorError) SetPosition(v int32)`

SetPosition sets Position field to given value.


### GetMessage

`func (o *LabelSelectorError) GetMessage() string`

GetMessage returns the Message field if non-nil, zero value otherwise.

### GetMessageOk

`func (o *LabelSelectorError) GetMessageOk() (*string, bool)`

GetMessageOk returns a tuple with the Message field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMessage

`func (o *LabelSelectorError) SetMessage(v string)`

SetMessage sets Message field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


