# LabelAssignment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DefinitionId** | **string** | Parent Label Definition identifier (UUIDv7). | 
**QualifiedKey** | **string** | Fully-qualified Label key (denormalised). | 
**ObjectKind** | **string** | Lowercase object-kind discriminator. | 
**ObjectId** | **string** | Object identifier (UUIDv7). | 
**Value** | **interface{}** |  | 
**AssignedBy** | **string** | Provenance marker — &#x60;user&#x60; for human callers, &#x60;system&#x60; for seed Assignments.  | 
**AssignedAt** | **time.Time** | RFC 3339 timestamp of the most recent write. | 

## Methods

### NewLabelAssignment

`func NewLabelAssignment(definitionId string, qualifiedKey string, objectKind string, objectId string, value interface{}, assignedBy string, assignedAt time.Time, ) *LabelAssignment`

NewLabelAssignment instantiates a new LabelAssignment object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewLabelAssignmentWithDefaults

`func NewLabelAssignmentWithDefaults() *LabelAssignment`

NewLabelAssignmentWithDefaults instantiates a new LabelAssignment object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDefinitionId

`func (o *LabelAssignment) GetDefinitionId() string`

GetDefinitionId returns the DefinitionId field if non-nil, zero value otherwise.

### GetDefinitionIdOk

`func (o *LabelAssignment) GetDefinitionIdOk() (*string, bool)`

GetDefinitionIdOk returns a tuple with the DefinitionId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDefinitionId

`func (o *LabelAssignment) SetDefinitionId(v string)`

SetDefinitionId sets DefinitionId field to given value.


### GetQualifiedKey

`func (o *LabelAssignment) GetQualifiedKey() string`

GetQualifiedKey returns the QualifiedKey field if non-nil, zero value otherwise.

### GetQualifiedKeyOk

`func (o *LabelAssignment) GetQualifiedKeyOk() (*string, bool)`

GetQualifiedKeyOk returns a tuple with the QualifiedKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetQualifiedKey

`func (o *LabelAssignment) SetQualifiedKey(v string)`

SetQualifiedKey sets QualifiedKey field to given value.


### GetObjectKind

`func (o *LabelAssignment) GetObjectKind() string`

GetObjectKind returns the ObjectKind field if non-nil, zero value otherwise.

### GetObjectKindOk

`func (o *LabelAssignment) GetObjectKindOk() (*string, bool)`

GetObjectKindOk returns a tuple with the ObjectKind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetObjectKind

`func (o *LabelAssignment) SetObjectKind(v string)`

SetObjectKind sets ObjectKind field to given value.


### GetObjectId

`func (o *LabelAssignment) GetObjectId() string`

GetObjectId returns the ObjectId field if non-nil, zero value otherwise.

### GetObjectIdOk

`func (o *LabelAssignment) GetObjectIdOk() (*string, bool)`

GetObjectIdOk returns a tuple with the ObjectId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetObjectId

`func (o *LabelAssignment) SetObjectId(v string)`

SetObjectId sets ObjectId field to given value.


### GetValue

`func (o *LabelAssignment) GetValue() interface{}`

GetValue returns the Value field if non-nil, zero value otherwise.

### GetValueOk

`func (o *LabelAssignment) GetValueOk() (*interface{}, bool)`

GetValueOk returns a tuple with the Value field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetValue

`func (o *LabelAssignment) SetValue(v interface{})`

SetValue sets Value field to given value.


### SetValueNil

`func (o *LabelAssignment) SetValueNil(b bool)`

 SetValueNil sets the value for Value to be an explicit nil

### UnsetValue
`func (o *LabelAssignment) UnsetValue()`

UnsetValue ensures that no value is present for Value, not even an explicit nil
### GetAssignedBy

`func (o *LabelAssignment) GetAssignedBy() string`

GetAssignedBy returns the AssignedBy field if non-nil, zero value otherwise.

### GetAssignedByOk

`func (o *LabelAssignment) GetAssignedByOk() (*string, bool)`

GetAssignedByOk returns a tuple with the AssignedBy field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAssignedBy

`func (o *LabelAssignment) SetAssignedBy(v string)`

SetAssignedBy sets AssignedBy field to given value.


### GetAssignedAt

`func (o *LabelAssignment) GetAssignedAt() time.Time`

GetAssignedAt returns the AssignedAt field if non-nil, zero value otherwise.

### GetAssignedAtOk

`func (o *LabelAssignment) GetAssignedAtOk() (*time.Time, bool)`

GetAssignedAtOk returns a tuple with the AssignedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAssignedAt

`func (o *LabelAssignment) SetAssignedAt(v time.Time)`

SetAssignedAt sets AssignedAt field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


