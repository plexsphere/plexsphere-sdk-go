# OutputRef

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | [**OutputRefKind**](OutputRefKind.md) |  | 
**InlineBytes** | Pointer to **string** | Base64-encoded output bytes. Present only on the &#x60;inline&#x60; variant; bounded at 16 KiB.  | [optional] 
**Bucket** | Pointer to **string** | Object-store bucket holding the uploaded output. Present only on the &#x60;object_store&#x60; variant.  | [optional] 
**Key** | Pointer to **string** | Object-store key addressing the uploaded output. Present only on the &#x60;object_store&#x60; variant.  | [optional] 
**Sha256** | Pointer to **string** | Hex-encoded SHA-256 digest of the uploaded output. Present only on the &#x60;object_store&#x60; variant.  | [optional] 

## Methods

### NewOutputRef

`func NewOutputRef(kind OutputRefKind, ) *OutputRef`

NewOutputRef instantiates a new OutputRef object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewOutputRefWithDefaults

`func NewOutputRefWithDefaults() *OutputRef`

NewOutputRefWithDefaults instantiates a new OutputRef object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetKind

`func (o *OutputRef) GetKind() OutputRefKind`

GetKind returns the Kind field if non-nil, zero value otherwise.

### GetKindOk

`func (o *OutputRef) GetKindOk() (*OutputRefKind, bool)`

GetKindOk returns a tuple with the Kind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKind

`func (o *OutputRef) SetKind(v OutputRefKind)`

SetKind sets Kind field to given value.


### GetInlineBytes

`func (o *OutputRef) GetInlineBytes() string`

GetInlineBytes returns the InlineBytes field if non-nil, zero value otherwise.

### GetInlineBytesOk

`func (o *OutputRef) GetInlineBytesOk() (*string, bool)`

GetInlineBytesOk returns a tuple with the InlineBytes field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetInlineBytes

`func (o *OutputRef) SetInlineBytes(v string)`

SetInlineBytes sets InlineBytes field to given value.

### HasInlineBytes

`func (o *OutputRef) HasInlineBytes() bool`

HasInlineBytes returns a boolean if a field has been set.

### GetBucket

`func (o *OutputRef) GetBucket() string`

GetBucket returns the Bucket field if non-nil, zero value otherwise.

### GetBucketOk

`func (o *OutputRef) GetBucketOk() (*string, bool)`

GetBucketOk returns a tuple with the Bucket field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetBucket

`func (o *OutputRef) SetBucket(v string)`

SetBucket sets Bucket field to given value.

### HasBucket

`func (o *OutputRef) HasBucket() bool`

HasBucket returns a boolean if a field has been set.

### GetKey

`func (o *OutputRef) GetKey() string`

GetKey returns the Key field if non-nil, zero value otherwise.

### GetKeyOk

`func (o *OutputRef) GetKeyOk() (*string, bool)`

GetKeyOk returns a tuple with the Key field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetKey

`func (o *OutputRef) SetKey(v string)`

SetKey sets Key field to given value.

### HasKey

`func (o *OutputRef) HasKey() bool`

HasKey returns a boolean if a field has been set.

### GetSha256

`func (o *OutputRef) GetSha256() string`

GetSha256 returns the Sha256 field if non-nil, zero value otherwise.

### GetSha256Ok

`func (o *OutputRef) GetSha256Ok() (*string, bool)`

GetSha256Ok returns a tuple with the Sha256 field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSha256

`func (o *OutputRef) SetSha256(v string)`

SetSha256 sets Sha256 field to given value.

### HasSha256

`func (o *OutputRef) HasSha256() bool`

HasSha256 returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


