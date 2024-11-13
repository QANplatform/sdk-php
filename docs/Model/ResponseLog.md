# # ResponseLog

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **string** | An address from which this log originated |
**block_hash** | **string** | The hash of the block where this log was in. null when its a pending log |
**block_number** | **string** | The block number where this log was in. null when its a pending log |
**data** | **string** | It contains one or more 32 Bytes non-indexed arguments of the log |
**log_index** | **string** | The integer of the log index position in the block. null when its a pending log |
**removed** | **bool** | It is true when the log was removed due to a chain reorganization, and false if it&#39;s a valid log |
**topics** | **string[]** | An array of zero to four 32 Bytes DATA of indexed log arguments. In Solidity, the first topic is the hash of the signature of the event (e.g. Deposit(address, bytes32, uint256)), except you declare the event with the anonymous specifier |
**transaction_hash** | **string** | The hash of the transactions this log was created from. null when its a pending log |
**transaction_index** | **string** | The integer of the transaction&#39;s index position that the log was created from. null when it&#39;s a pending log |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
