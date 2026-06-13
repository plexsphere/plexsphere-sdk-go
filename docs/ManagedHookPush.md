# ManagedHookPush

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Recorded push identifier (UUIDv7). | 
**DomainId** | **string** | Owning Domain identifier. | 
**HookName** | **string** | Name of the PlexdHook object applied. | 
**Namespace** | **string** | Namespace the hook was applied into. | 
**Status** | [**ManagedHookPushStatus**](ManagedHookPushStatus.md) |  | 
**HadPriorState** | **bool** | Whether the apply replaced an existing object. When &#x60;true&#x60; a rollback restores the prior object; when &#x60;false&#x60; a rollback deletes the applied object.  | 
**PushedAt** | **time.Time** | Timestamp the object was applied. | 
**RolledBackAt** | Pointer to **time.Time** | Timestamp the push was rolled back, or &#x60;null&#x60; when the push has not been rolled back.  | [optional] 

## Methods

### NewManagedHookPush

`func NewManagedHookPush(id string, domainId string, hookName string, namespace string, status ManagedHookPushStatus, hadPriorState bool, pushedAt time.Time, ) *ManagedHookPush`

NewManagedHookPush instantiates a new ManagedHookPush object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewManagedHookPushWithDefaults

`func NewManagedHookPushWithDefaults() *ManagedHookPush`

NewManagedHookPushWithDefaults instantiates a new ManagedHookPush object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *ManagedHookPush) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *ManagedHookPush) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *ManagedHookPush) SetId(v string)`

SetId sets Id field to given value.


### GetDomainId

`func (o *ManagedHookPush) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *ManagedHookPush) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *ManagedHookPush) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.


### GetHookName

`func (o *ManagedHookPush) GetHookName() string`

GetHookName returns the HookName field if non-nil, zero value otherwise.

### GetHookNameOk

`func (o *ManagedHookPush) GetHookNameOk() (*string, bool)`

GetHookNameOk returns a tuple with the HookName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHookName

`func (o *ManagedHookPush) SetHookName(v string)`

SetHookName sets HookName field to given value.


### GetNamespace

`func (o *ManagedHookPush) GetNamespace() string`

GetNamespace returns the Namespace field if non-nil, zero value otherwise.

### GetNamespaceOk

`func (o *ManagedHookPush) GetNamespaceOk() (*string, bool)`

GetNamespaceOk returns a tuple with the Namespace field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNamespace

`func (o *ManagedHookPush) SetNamespace(v string)`

SetNamespace sets Namespace field to given value.


### GetStatus

`func (o *ManagedHookPush) GetStatus() ManagedHookPushStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *ManagedHookPush) GetStatusOk() (*ManagedHookPushStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *ManagedHookPush) SetStatus(v ManagedHookPushStatus)`

SetStatus sets Status field to given value.


### GetHadPriorState

`func (o *ManagedHookPush) GetHadPriorState() bool`

GetHadPriorState returns the HadPriorState field if non-nil, zero value otherwise.

### GetHadPriorStateOk

`func (o *ManagedHookPush) GetHadPriorStateOk() (*bool, bool)`

GetHadPriorStateOk returns a tuple with the HadPriorState field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetHadPriorState

`func (o *ManagedHookPush) SetHadPriorState(v bool)`

SetHadPriorState sets HadPriorState field to given value.


### GetPushedAt

`func (o *ManagedHookPush) GetPushedAt() time.Time`

GetPushedAt returns the PushedAt field if non-nil, zero value otherwise.

### GetPushedAtOk

`func (o *ManagedHookPush) GetPushedAtOk() (*time.Time, bool)`

GetPushedAtOk returns a tuple with the PushedAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPushedAt

`func (o *ManagedHookPush) SetPushedAt(v time.Time)`

SetPushedAt sets PushedAt field to given value.


### GetRolledBackAt

`func (o *ManagedHookPush) GetRolledBackAt() time.Time`

GetRolledBackAt returns the RolledBackAt field if non-nil, zero value otherwise.

### GetRolledBackAtOk

`func (o *ManagedHookPush) GetRolledBackAtOk() (*time.Time, bool)`

GetRolledBackAtOk returns a tuple with the RolledBackAt field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetRolledBackAt

`func (o *ManagedHookPush) SetRolledBackAt(v time.Time)`

SetRolledBackAt sets RolledBackAt field to given value.

### HasRolledBackAt

`func (o *ManagedHookPush) HasRolledBackAt() bool`

HasRolledBackAt returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


