# # OutputGetProof

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schema** | **string** | A URL to the JSON Schema for this object. | [optional] [readonly]
**account_proof** | **string** | An array of rlp-serialized MerkleTree-Nodes which starts with the stateRoot-Node and follows the path of the SHA3 address as key |
**address** | **string** | The address associated with the account |
**balance** | **string** | The current balance of the account in wei |
**code_hash** | **string** | A 32 byte hash of the code of the account |
**nonce** | **string** | The hash of the generated proof-of-work. Null if pending |
**storage_hash** | **string** | A 32 byte SHA3 of the storageRoot. All storage will deliver a MerkleProof starting with this rootHash |
**storage_proof** | [**\qan\qan\ResponseStorageEntry[]**](ResponseStorageEntry.md) | An array of storage-entries as requested. Each entry is an object with the following fields: |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
