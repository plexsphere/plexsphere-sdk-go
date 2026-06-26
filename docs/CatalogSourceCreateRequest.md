# CatalogSourceCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** | Human-facing label. Not required unique — identity is the generated &#x60;id&#x60;. Whitespace-only is rejected.  | 
**OciReference** | [**OciReference**](OciReference.md) |  | 
**Verification** | [**VerificationPolicy**](VerificationPolicy.md) |  | 
**Tracking** | [**TrackingPolicy**](TrackingPolicy.md) |  | 
**CredentialRef** | Pointer to **string** | Optional &#x60;namespace/name&#x60; reference to the Kubernetes Secret the registry authenticates with. Omit or &#x60;null&#x60; for a public registry. A malformed reference surfaces as &#x60;400 invalid_credential_ref&#x60;.  | [optional] 
**DomainId** | Pointer to **string** | Owning Domain when the source is scoped to a single Domain. Omit or &#x60;null&#x60; for a catalog-global source. The scope drives the ReBAC gate: a Domain-scoped source gates on &#x60;domain#manage&#x60;, a catalog-global source on &#x60;platform#manage&#x60;.  | [optional] 
**Status** | [**CatalogSourceCreateRequestStatus**](CatalogSourceCreateRequestStatus.md) |  | 

## Methods

### NewCatalogSourceCreateRequest

`func NewCatalogSourceCreateRequest(name string, ociReference OciReference, verification VerificationPolicy, tracking TrackingPolicy, status CatalogSourceCreateRequestStatus, ) *CatalogSourceCreateRequest`

NewCatalogSourceCreateRequest instantiates a new CatalogSourceCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewCatalogSourceCreateRequestWithDefaults

`func NewCatalogSourceCreateRequestWithDefaults() *CatalogSourceCreateRequest`

NewCatalogSourceCreateRequestWithDefaults instantiates a new CatalogSourceCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetName

`func (o *CatalogSourceCreateRequest) GetName() string`

GetName returns the Name field if non-nil, zero value otherwise.

### GetNameOk

`func (o *CatalogSourceCreateRequest) GetNameOk() (*string, bool)`

GetNameOk returns a tuple with the Name field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetName

`func (o *CatalogSourceCreateRequest) SetName(v string)`

SetName sets Name field to given value.


### GetOciReference

`func (o *CatalogSourceCreateRequest) GetOciReference() OciReference`

GetOciReference returns the OciReference field if non-nil, zero value otherwise.

### GetOciReferenceOk

`func (o *CatalogSourceCreateRequest) GetOciReferenceOk() (*OciReference, bool)`

GetOciReferenceOk returns a tuple with the OciReference field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetOciReference

`func (o *CatalogSourceCreateRequest) SetOciReference(v OciReference)`

SetOciReference sets OciReference field to given value.


### GetVerification

`func (o *CatalogSourceCreateRequest) GetVerification() VerificationPolicy`

GetVerification returns the Verification field if non-nil, zero value otherwise.

### GetVerificationOk

`func (o *CatalogSourceCreateRequest) GetVerificationOk() (*VerificationPolicy, bool)`

GetVerificationOk returns a tuple with the Verification field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetVerification

`func (o *CatalogSourceCreateRequest) SetVerification(v VerificationPolicy)`

SetVerification sets Verification field to given value.


### GetTracking

`func (o *CatalogSourceCreateRequest) GetTracking() TrackingPolicy`

GetTracking returns the Tracking field if non-nil, zero value otherwise.

### GetTrackingOk

`func (o *CatalogSourceCreateRequest) GetTrackingOk() (*TrackingPolicy, bool)`

GetTrackingOk returns a tuple with the Tracking field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTracking

`func (o *CatalogSourceCreateRequest) SetTracking(v TrackingPolicy)`

SetTracking sets Tracking field to given value.


### GetCredentialRef

`func (o *CatalogSourceCreateRequest) GetCredentialRef() string`

GetCredentialRef returns the CredentialRef field if non-nil, zero value otherwise.

### GetCredentialRefOk

`func (o *CatalogSourceCreateRequest) GetCredentialRefOk() (*string, bool)`

GetCredentialRefOk returns a tuple with the CredentialRef field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetCredentialRef

`func (o *CatalogSourceCreateRequest) SetCredentialRef(v string)`

SetCredentialRef sets CredentialRef field to given value.

### HasCredentialRef

`func (o *CatalogSourceCreateRequest) HasCredentialRef() bool`

HasCredentialRef returns a boolean if a field has been set.

### GetDomainId

`func (o *CatalogSourceCreateRequest) GetDomainId() string`

GetDomainId returns the DomainId field if non-nil, zero value otherwise.

### GetDomainIdOk

`func (o *CatalogSourceCreateRequest) GetDomainIdOk() (*string, bool)`

GetDomainIdOk returns a tuple with the DomainId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainId

`func (o *CatalogSourceCreateRequest) SetDomainId(v string)`

SetDomainId sets DomainId field to given value.

### HasDomainId

`func (o *CatalogSourceCreateRequest) HasDomainId() bool`

HasDomainId returns a boolean if a field has been set.

### GetStatus

`func (o *CatalogSourceCreateRequest) GetStatus() CatalogSourceCreateRequestStatus`

GetStatus returns the Status field if non-nil, zero value otherwise.

### GetStatusOk

`func (o *CatalogSourceCreateRequest) GetStatusOk() (*CatalogSourceCreateRequestStatus, bool)`

GetStatusOk returns a tuple with the Status field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetStatus

`func (o *CatalogSourceCreateRequest) SetStatus(v CatalogSourceCreateRequestStatus)`

SetStatus sets Status field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


