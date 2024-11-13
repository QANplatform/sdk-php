# # ResponseTransaction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_list** | **string** | A list of addresses and storage keys that the transaction plans to access | [optional]
**block_hash** | **string** | The hash of the block where this transaction was in. Null when it&#39;s a pending transaction | [optional]
**block_number** | **string** | The block number where this transaction was in. Null when it&#39;s a pending transaction | [optional]
**chain_id** | **string** | The chain id of the transaction, if any | [optional]
**from** | **string** | The address of the sender | [optional]
**gas** | **string** | The gas provided by the sender, encoded as decimal | [optional]
**gas_price** | **string** | The gas price provided by the sender in wei encoded as decimal | [optional]
**hash** | **string** | The hash of the transaction | [optional]
**input** | **string** | The data sent along with the transaction | [optional]
**max_fee_per_gas** | **string** | The maximum fee per gas set in the transaction | [optional]
**max_priority_fee_per_gas** | **string** | The maximum priority gas fee set in the transaction | [optional]
**nonce** | **string** | The number of transactions made by the sender prior to this one encoded as decimal | [optional]
**r** | **string** | The R field of the signature | [optional]
**s** | **string** | The S field of the signature | [optional]
**to** | **string** | The address of the receiver. Null when its a contract creation transaction | [optional]
**transaction_index** | **string** | The integer of the transaction&#39;s index position that the log was created from. Null when it&#39;s a pending log | [optional]
**type** | **string** | The transaction type | [optional]
**v** | **string** | The standardized V field of the signature | [optional]
**value** | **string** | The value transferred in wei encoded as decimal | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
