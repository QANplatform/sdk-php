# # ResponseTransactionReceipt

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**block_hash** | **string** | The hash of the block. null when pending | [optional]
**block_number** | **string** |  | [optional]
**contract_address** | **string** | The contract address created if the transaction was a contract creation, otherwise null | [optional]
**cumulative_gas_used** | **string** | The total amount of gas used when this transaction was executed in the block | [optional]
**effective_gas_price** | **string** | The actual value per gas deducted from the sender account | [optional]
**from** | **string** | The address of the sender | [optional]
**gas_used** | **string** | The amount of gas used by this specific transaction alone | [optional]
**logs** | [**\qan\qan\ResponseLog[]**](ResponseLog.md) | An array of log objects that generated this transaction | [optional]
**logs_bloom** | **string** | The bloom filter for light clients to quickly retrieve related logs | [optional]
**status** | **string** | It is either 1 (success) or 0 (failure) encoded as a decimal | [optional]
**to** | **string** | The address of the receiver. null when it&#39;s a contract creation transaction | [optional]
**transaction_hash** | **string** | The hash of the transaction | [optional]
**transaction_index** | **string** | An index of the transaction in the block | [optional]
**type** | **string** | The value type | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
