# RegisterResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**NodeId** | **string** | Freshly-allocated Node aggregate id (UUIDv7). Echoed in the response so plexd records its own identity.  | 
**MeshIp** | **string** | Allocator-assigned mesh address inside the Domain&#39;s mesh CIDR. Canonical &#x60;netip.Addr&#x60; string form (&#x60;100.64.0.1&#x60;, never zero-padded).  | 
**SigningPublicKey** | **string** | Domain&#39;s active signing public key, base64-encoded. Plexd pins this and uses it to verify signed SSE events delivered.  | 
**SigningKeyId** | **string** | Identifier (kid) the Domain&#39;s active signing key is indexed under (e.g. a DID-URL fragment). Carried so plexd can rotate-aware verify SSE events whose header references a non-current kid during a rotation grace window.  | 
**Nsk** | **string** | Per-Node Node Secret Key plaintext (32 bytes, base64- encoded). **Shown exactly once** — there is no API surface that ever returns the plaintext again because the persistence layer stores only the wrapped form. Operators MUST capture it from this response and pin it on the registering Node out-of-band. The Spectral rule polices this guarantee against any future schema that would leak the marker outside this single response.  | 
**PeerSnapshot** | [**[]RegisterPeer**](RegisterPeer.md) | Initial wireguard peer set the registering Node needs to bring its table up. Empty for the first Node enrolled into a Domain. Subsequent membership churn is delivered through the SSE stream rather than re-issued here.  | 
**DomainMeshCidr** | **string** | Domain&#39;s mesh CIDR (e.g. &#x60;100.64.0.0/10&#x60;). Carried so plexd can program its routing table without a follow-up Domain lookup.  | 

## Methods

### NewRegisterResponse

`func NewRegisterResponse(nodeId string, meshIp string, signingPublicKey string, signingKeyId string, nsk string, peerSnapshot []RegisterPeer, domainMeshCidr string, ) *RegisterResponse`

NewRegisterResponse instantiates a new RegisterResponse object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewRegisterResponseWithDefaults

`func NewRegisterResponseWithDefaults() *RegisterResponse`

NewRegisterResponseWithDefaults instantiates a new RegisterResponse object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetNodeId

`func (o *RegisterResponse) GetNodeId() string`

GetNodeId returns the NodeId field if non-nil, zero value otherwise.

### GetNodeIdOk

`func (o *RegisterResponse) GetNodeIdOk() (*string, bool)`

GetNodeIdOk returns a tuple with the NodeId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNodeId

`func (o *RegisterResponse) SetNodeId(v string)`

SetNodeId sets NodeId field to given value.


### GetMeshIp

`func (o *RegisterResponse) GetMeshIp() string`

GetMeshIp returns the MeshIp field if non-nil, zero value otherwise.

### GetMeshIpOk

`func (o *RegisterResponse) GetMeshIpOk() (*string, bool)`

GetMeshIpOk returns a tuple with the MeshIp field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetMeshIp

`func (o *RegisterResponse) SetMeshIp(v string)`

SetMeshIp sets MeshIp field to given value.


### GetSigningPublicKey

`func (o *RegisterResponse) GetSigningPublicKey() string`

GetSigningPublicKey returns the SigningPublicKey field if non-nil, zero value otherwise.

### GetSigningPublicKeyOk

`func (o *RegisterResponse) GetSigningPublicKeyOk() (*string, bool)`

GetSigningPublicKeyOk returns a tuple with the SigningPublicKey field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSigningPublicKey

`func (o *RegisterResponse) SetSigningPublicKey(v string)`

SetSigningPublicKey sets SigningPublicKey field to given value.


### GetSigningKeyId

`func (o *RegisterResponse) GetSigningKeyId() string`

GetSigningKeyId returns the SigningKeyId field if non-nil, zero value otherwise.

### GetSigningKeyIdOk

`func (o *RegisterResponse) GetSigningKeyIdOk() (*string, bool)`

GetSigningKeyIdOk returns a tuple with the SigningKeyId field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetSigningKeyId

`func (o *RegisterResponse) SetSigningKeyId(v string)`

SetSigningKeyId sets SigningKeyId field to given value.


### GetNsk

`func (o *RegisterResponse) GetNsk() string`

GetNsk returns the Nsk field if non-nil, zero value otherwise.

### GetNskOk

`func (o *RegisterResponse) GetNskOk() (*string, bool)`

GetNskOk returns a tuple with the Nsk field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetNsk

`func (o *RegisterResponse) SetNsk(v string)`

SetNsk sets Nsk field to given value.


### GetPeerSnapshot

`func (o *RegisterResponse) GetPeerSnapshot() []RegisterPeer`

GetPeerSnapshot returns the PeerSnapshot field if non-nil, zero value otherwise.

### GetPeerSnapshotOk

`func (o *RegisterResponse) GetPeerSnapshotOk() (*[]RegisterPeer, bool)`

GetPeerSnapshotOk returns a tuple with the PeerSnapshot field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetPeerSnapshot

`func (o *RegisterResponse) SetPeerSnapshot(v []RegisterPeer)`

SetPeerSnapshot sets PeerSnapshot field to given value.


### GetDomainMeshCidr

`func (o *RegisterResponse) GetDomainMeshCidr() string`

GetDomainMeshCidr returns the DomainMeshCidr field if non-nil, zero value otherwise.

### GetDomainMeshCidrOk

`func (o *RegisterResponse) GetDomainMeshCidrOk() (*string, bool)`

GetDomainMeshCidrOk returns a tuple with the DomainMeshCidr field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDomainMeshCidr

`func (o *RegisterResponse) SetDomainMeshCidr(v string)`

SetDomainMeshCidr sets DomainMeshCidr field to given value.



[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


