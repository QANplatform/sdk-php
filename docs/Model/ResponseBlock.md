# # ResponseBlock

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**base_fee_per_gas** | **string** | A string of the base fee encoded in decimal format. Please note that this response field will not be included in a block requested before the EIP-1559 upgrade |
**difficulty** | **string** | The integer of the difficulty for this block encoded as a decimal |
**extra_data** | **string** | The “extra data” field of this block |
**gas_limit** | **string** | The maximum gas allowed in this block encoded as a decimal |
**gas_used** | **string** | The total used gas by all transactions in this block encoded as a decimal |
**hash** | **string** | The block hash of the requested block. null if pending |
**logs_bloom** | **string** | The bloom filter for the logs of the block. null if pending |
**miner** | **string** | The address of the beneficiary to whom the mining rewards were given |
**mix_hash** | **string** | A string of a 256-bit hash encoded as a decimal |
**nonce** | **string** | The hash of the generated proof-of-work. null if pending |
**number** | **string** | The block number of the requested block encoded as a decimal. null if pending |
**parent_hash** | **string** | The hash of the parent block |
**receipts_root** | **string** | The root of the receipts trie of the bloc |
**sha3_uncles** | **string** | The SHA3 of the uncles data in the block |
**size** | **string** | The size of this block in bytes as an Integer value encoded as decimal |
**state_root** | **string** | The root of the final state trie of the block |
**timestamp** | **string** | The unix timestamp for when the block was collated |
**total_difficulty** | **string** | The integer of the total difficulty of the chain until this block encoded as a decimal |
**transactions** | [**\qan\qan\ResponseTransaction[]**](ResponseTransaction.md) | An array of transaction objects - please see getTransactionByHash for exact shape |
**transactions_root** | **string** | The root of the transaction trie of the block |
**uncles** | **string[]** | An array of uncle hashes |
**withdrawals** | [**\qan\qan\ResponseWithdrawals**](ResponseWithdrawals.md) | A withdrawals object contains information about withdrawals made by validators. Please note that this field will not be included in a block requested before the EIP-4895 upgrade |
**withdrawals_root** | **string** | The Merkle root of withdrawal data. Also, please note that this field will not be included in a block requested before the EIP-4895 upgrade |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
