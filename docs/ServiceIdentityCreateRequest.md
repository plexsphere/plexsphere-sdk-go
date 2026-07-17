# ServiceIdentityCreateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | **string** | Operator-facing label for the service identity (for example &#x60;CI deploy bot&#x60;). Trimmed; must be non-empty.  | 
**Subject** | **string** | Upstream workload subject the presented credential must carry — the OIDC &#x60;sub&#x60; claim or the SPIFFE ID, depending on &#x60;federation_kind&#x60;. Unique per Domain: a second identity reusing the same subject is rejected with &#x60;409&#x60;.  | 
**Audience** | **string** | Expected audience claim for the presented credential.  | 
**FederationKind** | [**ServiceFederationKind**](ServiceFederationKind.md) |  | 

## Methods

### NewServiceIdentityCreateRequest

`func NewServiceIdentityCreateRequest(displayName string, subject string, audience string, federationKind ServiceFederationKind, ) *ServiceIdentityCreateRequest`

NewServiceIdentityCreateRequest instantiates a new ServiceIdentityCreateRequest object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewServiceIdentityCreateRequestWithDefaults

`func NewServiceIdentityCreateRequestWithDefaults() *ServiceIdentityCreateRequest`

NewServiceIdentityCreateRequestWithDefaults instantiates a new ServiceIdentityCreateRequest object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetDisplayName

`func (o *ServiceIdentityCreateRequest) GetDisplayName() string`

GetDisplayName returns the DisplayName field if non-nil, zero value otherwise.

### GetDisplayNameOk

`func (o *ServiceIdentityCreateRequest) GetDisplayNameOk() (*string, bool)`

GetDisplayNameOk returns a tuple with the DisplayName field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDisplayName

`func (o *ServiceIdentityCreateRequest) SetDisplayName(v string)`

SetDisplayName sets DisplayName field to given value.


### GetSubject

`func (o *ServiceIdentityCreateRequest) GetSubject() string`

GetSubject returns the Subject field if non-nil, zero value otherwise.

### GetSubjectOk

`func (o *ServiceIdentityCreateRequest) GetSubjectOk() (*string, bool)`

GetSubjectOk returns a tuple with the Subject field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSubject

`func (o *ServiceIdentityCreateRequest) SetSubject(v string)`

SetSubject sets Subject field to given value.


### GetAudience

`func (o *ServiceIdentityCreateRequest) GetAudience() string`

GetAudience returns the Audience field if non-nil, zero value otherwise.

### GetAudienceOk

`func (o *ServiceIdentityCreateRequest) GetAudienceOk() (*string, bool)`

GetAudienceOk returns a tuple with the Audience field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetAudience

`func (o *ServiceIdentityCreateRequest) SetAudience(v string)`

SetAudience sets Audience field to given value.


### GetFederationKind

`func (o *ServiceIdentityCreateRequest) GetFederationKind() ServiceFederationKind`

GetFederationKind returns the FederationKind field if non-nil, zero value otherwise.

### GetFederationKindOk

`func (o *ServiceIdentityCreateRequest) GetFederationKindOk() (*ServiceFederationKind, bool)`

GetFederationKindOk returns a tuple with the FederationKind field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetFederationKind

`func (o *ServiceIdentityCreateRequest) SetFederationKind(v ServiceFederationKind)`

SetFederationKind sets FederationKind field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


