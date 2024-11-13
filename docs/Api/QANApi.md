# qan\QANApi

All URIs are relative to https://rpc-testnet.qanplatform.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**qanBlockNumber()**](QANApi.md#qanBlockNumber) | **GET** /blockNumber/ | Returns the latest block number of the blockchain. |
| [**qanCall()**](QANApi.md#qanCall) | **POST** /call/ | Executes a new message call immediately without creating a transaction on the block chain. |
| [**qanChainId()**](QANApi.md#qanChainId) | **GET** /chainId/ | Returns the current network/chain ID, used to sign replay-protected transaction introduced in EIP-155. |
| [**qanEstimateGas()**](QANApi.md#qanEstimateGas) | **POST** /estimateGas/ | Returns an estimation of gas for a given transaction. |
| [**qanFeeHistory()**](QANApi.md#qanFeeHistory) | **POST** /feeHistory/ | Returns the collection of historical gas information. |
| [**qanGasPrice()**](QANApi.md#qanGasPrice) | **GET** /gasPrice/ | Returns the current gas price on the network in wei. |
| [**qanGetBalance()**](QANApi.md#qanGetBalance) | **GET** /getBalance/{Address}/ | Returns the balance of the account of given address. |
| [**qanGetBlockByHash()**](QANApi.md#qanGetBlockByHash) | **GET** /getBlockByHash/{Hash}/{TransactionDetailFlag}/ | Returns information of the block matching the given block hash. |
| [**qanGetBlockByNumber()**](QANApi.md#qanGetBlockByNumber) | **GET** /getBlockByNumber/{BlockNumber}/{TransactionDetailFlag}/ | Returns information of the block matching the given block number. |
| [**qanGetBlockReceipts()**](QANApi.md#qanGetBlockReceipts) | **GET** /getBlockReceipts/{BlockNumber}/ | Returns all transaction receipts for a given block. |
| [**qanGetBlockTransactionCountByHash()**](QANApi.md#qanGetBlockTransactionCountByHash) | **GET** /getBlockTransactionCountByHash/{Hash}/ | Returns the number of transactions for the block matching the given block hash. |
| [**qanGetBlockTransactionCountByNumber()**](QANApi.md#qanGetBlockTransactionCountByNumber) | **GET** /getBlockTransactionCountByNumber/{BlockNumber}/ | Returns the number of transactions for the block matching the given block number. |
| [**qanGetCode()**](QANApi.md#qanGetCode) | **GET** /getCode/{Address}/ | Returns the compiled bytecode of a smart contract. |
| [**qanGetFilterChanges()**](QANApi.md#qanGetFilterChanges) | **GET** /getFilterChanges/{FilterId}/ | Polling method for a filter, which returns an array of events that have occurred since the last poll. |
| [**qanGetFilterLogs()**](QANApi.md#qanGetFilterLogs) | **GET** /getFilterLogs/{Id}/ | Returns an array of all logs matching filter with given id. |
| [**qanGetLogs()**](QANApi.md#qanGetLogs) | **POST** /getLogs/ | Returns an array of all logs matching a given filter object. |
| [**qanGetProof()**](QANApi.md#qanGetProof) | **POST** /getProof/ | Returns the account and storage values of the specified account including the Merkle-proof. |
| [**qanGetStorageAt()**](QANApi.md#qanGetStorageAt) | **POST** /getStorageAt/ | Returns the value from a storage position at a given address. |
| [**qanGetTransactionByBlockHashAndIndex()**](QANApi.md#qanGetTransactionByBlockHashAndIndex) | **GET** /getTransactionByBlockHashAndIndex/{blockHash}/{index}/ | Returns information about a transaction given a blockhash and transaction index position. |
| [**qanGetTransactionByBlockNumberAndIndex()**](QANApi.md#qanGetTransactionByBlockNumberAndIndex) | **GET** /getTransactionByBlockNumberAndIndex/{blockNumber}/{index}/ | Returns information about a transaction given a block number and transaction index position. |
| [**qanGetTransactionByHash()**](QANApi.md#qanGetTransactionByHash) | **GET** /getTransactionByHash/{hash}/ | Returns the information about a transaction from a transaction hash. |
| [**qanGetTransactionCount()**](QANApi.md#qanGetTransactionCount) | **GET** /getTransactionCount/{Address}/{BlockNumber}/ | Returns the number of transactions sent from an address. |
| [**qanGetTransactionReceipt()**](QANApi.md#qanGetTransactionReceipt) | **GET** /getTransactionReceipt/{Hash}/ | Returns the receipt of a transaction by transaction hash. |
| [**qanMaxPriorityFeePerGas()**](QANApi.md#qanMaxPriorityFeePerGas) | **GET** /maxPriorityFeePerGas/ | Get the priority fee needed to be included in a block. |
| [**qanNewBlockFilter()**](QANApi.md#qanNewBlockFilter) | **GET** /newBlockFilter/ | Creates a filter in the node, to notify when a new block arrives. |
| [**qanNewFilter()**](QANApi.md#qanNewFilter) | **POST** /newFilter/ | Creates a filter object, based on filter options, to notify when the state changes (logs). |
| [**qanNewPendingTransactionFilter()**](QANApi.md#qanNewPendingTransactionFilter) | **GET** /newPendingTransactionFilter/ | Creates a filter in the node to notify when new pending transactions arrive. |
| [**qanSendRawTransaction()**](QANApi.md#qanSendRawTransaction) | **POST** /sendRawTransaction/ | Creates new message call transaction or a contract creation for signed transactions. |
| [**qanSyncing()**](QANApi.md#qanSyncing) | **GET** /syncing/ | Returns an object with the sync status of the node if the node is out-of-sync and is syncing. Returns null when the node is already in sync. |
| [**qanUninstallFilter()**](QANApi.md#qanUninstallFilter) | **GET** /uninstallFilter/{FilterId}/ | Uninstalls a filter with the given filter id. |
| [**qanXlinkValid()**](QANApi.md#qanXlinkValid) | **GET** /xlinkValid/{Address}/ | Returns the xlink validity time of the account of given address. |


## `qanBlockNumber()`

```php
qanBlockNumber(): \qan\qan\OutputBlockNumber
```

Returns the latest block number of the blockchain.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->qanBlockNumber();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanBlockNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\qan\qan\OutputBlockNumber**](../Model/OutputBlockNumber.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanCall()`

```php
qanCall($input_call): \qan\qan\OutputCall
```

Executes a new message call immediately without creating a transaction on the block chain.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$input_call = new \qan\qan\InputCall(); // \qan\qan\InputCall

try {
    $result = $apiInstance->qanCall($input_call);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanCall: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **input_call** | [**\qan\qan\InputCall**](../Model/InputCall.md)|  | |

### Return type

[**\qan\qan\OutputCall**](../Model/OutputCall.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanChainId()`

```php
qanChainId(): \qan\qan\OutputChainId
```

Returns the current network/chain ID, used to sign replay-protected transaction introduced in EIP-155.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->qanChainId();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanChainId: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\qan\qan\OutputChainId**](../Model/OutputChainId.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanEstimateGas()`

```php
qanEstimateGas($input_estimate_gas): \qan\qan\OutputEstimateGas
```

Returns an estimation of gas for a given transaction.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$input_estimate_gas = new \qan\qan\InputEstimateGas(); // \qan\qan\InputEstimateGas

try {
    $result = $apiInstance->qanEstimateGas($input_estimate_gas);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanEstimateGas: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **input_estimate_gas** | [**\qan\qan\InputEstimateGas**](../Model/InputEstimateGas.md)|  | |

### Return type

[**\qan\qan\OutputEstimateGas**](../Model/OutputEstimateGas.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanFeeHistory()`

```php
qanFeeHistory($input_fee_history): \qan\qan\OutputFeeHistory
```

Returns the collection of historical gas information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$input_fee_history = new \qan\qan\InputFeeHistory(); // \qan\qan\InputFeeHistory

try {
    $result = $apiInstance->qanFeeHistory($input_fee_history);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanFeeHistory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **input_fee_history** | [**\qan\qan\InputFeeHistory**](../Model/InputFeeHistory.md)|  | |

### Return type

[**\qan\qan\OutputFeeHistory**](../Model/OutputFeeHistory.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGasPrice()`

```php
qanGasPrice(): \qan\qan\OutputGasPrice
```

Returns the current gas price on the network in wei.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->qanGasPrice();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGasPrice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\qan\qan\OutputGasPrice**](../Model/OutputGasPrice.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetBalance()`

```php
qanGetBalance($address, $block_number): \qan\qan\OutputGetBalance
```

Returns the balance of the account of given address.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$address = 0xa1e4380a3b1f749673e270229993ee55f35663b4; // string | A 20 bytes long hexadecimal value representing an address
$block_number = 'latest'; // string | The block number in hexadecimal or decimal format or the string latest, earliest, pending

try {
    $result = $apiInstance->qanGetBalance($address, $block_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetBalance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **address** | **string**| A 20 bytes long hexadecimal value representing an address | |
| **block_number** | **string**| The block number in hexadecimal or decimal format or the string latest, earliest, pending | [optional] [default to &#39;latest&#39;] |

### Return type

[**\qan\qan\OutputGetBalance**](../Model/OutputGetBalance.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetBlockByHash()`

```php
qanGetBlockByHash($hash, $transaction_detail_flag): \qan\qan\OutputGetBlockByHash
```

Returns information of the block matching the given block hash.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$hash = 0x4e3a3754410177e6937ef1f84bba68ea139e8d1a2258c5f85db9f1cd715a1bdd; // string | The hash (32 bytes) of the block
$transaction_detail_flag = false; // bool | The method returns the full transaction objects when this value is true otherwise, it returns only the hashes of the transactions

try {
    $result = $apiInstance->qanGetBlockByHash($hash, $transaction_detail_flag);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetBlockByHash: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **hash** | **string**| The hash (32 bytes) of the block | |
| **transaction_detail_flag** | **bool**| The method returns the full transaction objects when this value is true otherwise, it returns only the hashes of the transactions | [default to false] |

### Return type

[**\qan\qan\OutputGetBlockByHash**](../Model/OutputGetBlockByHash.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetBlockByNumber()`

```php
qanGetBlockByNumber($block_number, $transaction_detail_flag): \qan\qan\OutputGetBlockByNumber
```

Returns information of the block matching the given block number.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$block_number = 'latest'; // string | The block number in hexadecimal or decimal format or the string latest, earliest, pending
$transaction_detail_flag = false; // bool | The method returns the full transaction objects when this value is true otherwise, it returns only the hashes of the transactions

try {
    $result = $apiInstance->qanGetBlockByNumber($block_number, $transaction_detail_flag);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetBlockByNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **block_number** | **string**| The block number in hexadecimal or decimal format or the string latest, earliest, pending | [default to &#39;latest&#39;] |
| **transaction_detail_flag** | **bool**| The method returns the full transaction objects when this value is true otherwise, it returns only the hashes of the transactions | [default to false] |

### Return type

[**\qan\qan\OutputGetBlockByNumber**](../Model/OutputGetBlockByNumber.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetBlockReceipts()`

```php
qanGetBlockReceipts($block_number): \qan\qan\OutputGetBlockReceipts
```

Returns all transaction receipts for a given block.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$block_number = 'latest'; // string | The block number in hexadecimal or decimal format or the string latest, earliest, pending

try {
    $result = $apiInstance->qanGetBlockReceipts($block_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetBlockReceipts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **block_number** | **string**| The block number in hexadecimal or decimal format or the string latest, earliest, pending | [default to &#39;latest&#39;] |

### Return type

[**\qan\qan\OutputGetBlockReceipts**](../Model/OutputGetBlockReceipts.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetBlockTransactionCountByHash()`

```php
qanGetBlockTransactionCountByHash($hash): \qan\qan\OutputGetBlockTransactionCountByHash
```

Returns the number of transactions for the block matching the given block hash.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$hash = 0x4e3a3754410177e6937ef1f84bba68ea139e8d1a2258c5f85db9f1cd715a1bdd; // string | The hash of the block

try {
    $result = $apiInstance->qanGetBlockTransactionCountByHash($hash);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetBlockTransactionCountByHash: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **hash** | **string**| The hash of the block | |

### Return type

[**\qan\qan\OutputGetBlockTransactionCountByHash**](../Model/OutputGetBlockTransactionCountByHash.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetBlockTransactionCountByNumber()`

```php
qanGetBlockTransactionCountByNumber($block_number): \qan\qan\OutputGetBlockTransactionCountByNumber
```

Returns the number of transactions for the block matching the given block number.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$block_number = latest; // string | The block number in hexadecimal or decimal format or the string latest, earliest, pending

try {
    $result = $apiInstance->qanGetBlockTransactionCountByNumber($block_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetBlockTransactionCountByNumber: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **block_number** | **string**| The block number in hexadecimal or decimal format or the string latest, earliest, pending | |

### Return type

[**\qan\qan\OutputGetBlockTransactionCountByNumber**](../Model/OutputGetBlockTransactionCountByNumber.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetCode()`

```php
qanGetCode($address, $block_number): \qan\qan\OutputGetCode
```

Returns the compiled bytecode of a smart contract.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$address = 0xa1e4380a3b1f749673e270229993ee55f35663b4; // string | The address of the smart contract from which the bytecode will be obtained
$block_number = latest; // string | The block number in hexadecimal or decimal format or the string latest, earliest, pending

try {
    $result = $apiInstance->qanGetCode($address, $block_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetCode: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **address** | **string**| The address of the smart contract from which the bytecode will be obtained | |
| **block_number** | **string**| The block number in hexadecimal or decimal format or the string latest, earliest, pending | [optional] [default to &#39;latest&#39;] |

### Return type

[**\qan\qan\OutputGetCode**](../Model/OutputGetCode.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetFilterChanges()`

```php
qanGetFilterChanges($filter_id): \qan\qan\OutputGetFilterChanges
```

Polling method for a filter, which returns an array of events that have occurred since the last poll.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$filter_id = 'filter_id_example'; // string | The filter id that is returned from getFilterChangesnewFilter, getFilterChangesnewBlockFilter or getFilterChangesnewPendingTransactionFilter

try {
    $result = $apiInstance->qanGetFilterChanges($filter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetFilterChanges: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **filter_id** | **string**| The filter id that is returned from getFilterChangesnewFilter, getFilterChangesnewBlockFilter or getFilterChangesnewPendingTransactionFilter | |

### Return type

[**\qan\qan\OutputGetFilterChanges**](../Model/OutputGetFilterChanges.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetFilterLogs()`

```php
qanGetFilterLogs($id): \qan\qan\OutputGetFilterLogs
```

Returns an array of all logs matching filter with given id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$id = 'id_example'; // string | The filter ID

try {
    $result = $apiInstance->qanGetFilterLogs($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetFilterLogs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The filter ID | |

### Return type

[**\qan\qan\OutputGetFilterLogs**](../Model/OutputGetFilterLogs.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetLogs()`

```php
qanGetLogs($input_get_logs): \qan\qan\OutputGetLogs
```

Returns an array of all logs matching a given filter object.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$input_get_logs = new \qan\qan\InputGetLogs(); // \qan\qan\InputGetLogs

try {
    $result = $apiInstance->qanGetLogs($input_get_logs);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetLogs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **input_get_logs** | [**\qan\qan\InputGetLogs**](../Model/InputGetLogs.md)|  | |

### Return type

[**\qan\qan\OutputGetLogs**](../Model/OutputGetLogs.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetProof()`

```php
qanGetProof($input_get_proof): \qan\qan\OutputGetProof
```

Returns the account and storage values of the specified account including the Merkle-proof.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$input_get_proof = new \qan\qan\InputGetProof(); // \qan\qan\InputGetProof

try {
    $result = $apiInstance->qanGetProof($input_get_proof);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetProof: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **input_get_proof** | [**\qan\qan\InputGetProof**](../Model/InputGetProof.md)|  | |

### Return type

[**\qan\qan\OutputGetProof**](../Model/OutputGetProof.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetStorageAt()`

```php
qanGetStorageAt($input_get_storage_at): \qan\qan\OutputGetStorageAt
```

Returns the value from a storage position at a given address.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$input_get_storage_at = new \qan\qan\InputGetStorageAt(); // \qan\qan\InputGetStorageAt

try {
    $result = $apiInstance->qanGetStorageAt($input_get_storage_at);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetStorageAt: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **input_get_storage_at** | [**\qan\qan\InputGetStorageAt**](../Model/InputGetStorageAt.md)|  | |

### Return type

[**\qan\qan\OutputGetStorageAt**](../Model/OutputGetStorageAt.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetTransactionByBlockHashAndIndex()`

```php
qanGetTransactionByBlockHashAndIndex($block_hash, $index): \qan\qan\OutputGetTransactionByBlockHashAndIndex
```

Returns information about a transaction given a blockhash and transaction index position.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$block_hash = 0x4e3a3754410177e6937ef1f84bba68ea139e8d1a2258c5f85db9f1cd715a1bdd; // string
$index = 0; // string | An integer of the transaction index position

try {
    $result = $apiInstance->qanGetTransactionByBlockHashAndIndex($block_hash, $index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetTransactionByBlockHashAndIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **block_hash** | **string**|  | |
| **index** | **string**| An integer of the transaction index position | |

### Return type

[**\qan\qan\OutputGetTransactionByBlockHashAndIndex**](../Model/OutputGetTransactionByBlockHashAndIndex.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetTransactionByBlockNumberAndIndex()`

```php
qanGetTransactionByBlockNumberAndIndex($block_number, $index): \qan\qan\OutputGetTransactionByBlockNumberAndIndex
```

Returns information about a transaction given a block number and transaction index position.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$block_number = latest; // string | The block number in hexadecimal or decimal format or the string latest, earliest, pending
$index = 0; // string | An integer of the transaction index position

try {
    $result = $apiInstance->qanGetTransactionByBlockNumberAndIndex($block_number, $index);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetTransactionByBlockNumberAndIndex: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **block_number** | **string**| The block number in hexadecimal or decimal format or the string latest, earliest, pending | |
| **index** | **string**| An integer of the transaction index position | |

### Return type

[**\qan\qan\OutputGetTransactionByBlockNumberAndIndex**](../Model/OutputGetTransactionByBlockNumberAndIndex.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetTransactionByHash()`

```php
qanGetTransactionByHash($hash): \qan\qan\OutputGetTransactionByHash
```

Returns the information about a transaction from a transaction hash.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$hash = 0x5c504ed432cb51138bcf09aa5e8a410dd4a1e204ef84bfed1be16dfba1b22060; // string | The hash of a transaction

try {
    $result = $apiInstance->qanGetTransactionByHash($hash);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetTransactionByHash: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **hash** | **string**| The hash of a transaction | |

### Return type

[**\qan\qan\OutputGetTransactionByHash**](../Model/OutputGetTransactionByHash.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetTransactionCount()`

```php
qanGetTransactionCount($address, $block_number): \qan\qan\OutputGetTransactionCount
```

Returns the number of transactions sent from an address.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$address = 0xa1e4380a3b1f749673e270229993ee55f35663b4; // string | The address from which the transaction count to be checked
$block_number = latest; // string | The block number in hexadecimal or decimal format or the string latest, earliest, pending

try {
    $result = $apiInstance->qanGetTransactionCount($address, $block_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetTransactionCount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **address** | **string**| The address from which the transaction count to be checked | |
| **block_number** | **string**| The block number in hexadecimal or decimal format or the string latest, earliest, pending | |

### Return type

[**\qan\qan\OutputGetTransactionCount**](../Model/OutputGetTransactionCount.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanGetTransactionReceipt()`

```php
qanGetTransactionReceipt($hash): \qan\qan\OutputGetTransactionReceipt
```

Returns the receipt of a transaction by transaction hash.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$hash = 0x4e3a3754410177e6937ef1f84bba68ea139e8d1a2258c5f85db9f1cd715a1bdd; // string | The hash of a transaction

try {
    $result = $apiInstance->qanGetTransactionReceipt($hash);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanGetTransactionReceipt: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **hash** | **string**| The hash of a transaction | |

### Return type

[**\qan\qan\OutputGetTransactionReceipt**](../Model/OutputGetTransactionReceipt.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanMaxPriorityFeePerGas()`

```php
qanMaxPriorityFeePerGas(): \qan\qan\OutputMaxPriorityFeePerGas
```

Get the priority fee needed to be included in a block.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->qanMaxPriorityFeePerGas();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanMaxPriorityFeePerGas: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\qan\qan\OutputMaxPriorityFeePerGas**](../Model/OutputMaxPriorityFeePerGas.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanNewBlockFilter()`

```php
qanNewBlockFilter(): \qan\qan\OutputNewBlockFilter
```

Creates a filter in the node, to notify when a new block arrives.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->qanNewBlockFilter();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanNewBlockFilter: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\qan\qan\OutputNewBlockFilter**](../Model/OutputNewBlockFilter.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanNewFilter()`

```php
qanNewFilter($input_new_filter): \qan\qan\OutputNewFilter
```

Creates a filter object, based on filter options, to notify when the state changes (logs).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$input_new_filter = new \qan\qan\InputNewFilter(); // \qan\qan\InputNewFilter

try {
    $result = $apiInstance->qanNewFilter($input_new_filter);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanNewFilter: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **input_new_filter** | [**\qan\qan\InputNewFilter**](../Model/InputNewFilter.md)|  | |

### Return type

[**\qan\qan\OutputNewFilter**](../Model/OutputNewFilter.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanNewPendingTransactionFilter()`

```php
qanNewPendingTransactionFilter(): \qan\qan\OutputNewPendingTransactionFilter
```

Creates a filter in the node to notify when new pending transactions arrive.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->qanNewPendingTransactionFilter();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanNewPendingTransactionFilter: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\qan\qan\OutputNewPendingTransactionFilter**](../Model/OutputNewPendingTransactionFilter.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanSendRawTransaction()`

```php
qanSendRawTransaction($input_send_raw_transaction): \qan\qan\OutputSendRawTransaction
```

Creates new message call transaction or a contract creation for signed transactions.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$input_send_raw_transaction = new \qan\qan\InputSendRawTransaction(); // \qan\qan\InputSendRawTransaction

try {
    $result = $apiInstance->qanSendRawTransaction($input_send_raw_transaction);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanSendRawTransaction: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **input_send_raw_transaction** | [**\qan\qan\InputSendRawTransaction**](../Model/InputSendRawTransaction.md)|  | |

### Return type

[**\qan\qan\OutputSendRawTransaction**](../Model/OutputSendRawTransaction.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanSyncing()`

```php
qanSyncing(): \qan\qan\OutputSyncing
```

Returns an object with the sync status of the node if the node is out-of-sync and is syncing. Returns null when the node is already in sync.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->qanSyncing();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanSyncing: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\qan\qan\OutputSyncing**](../Model/OutputSyncing.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanUninstallFilter()`

```php
qanUninstallFilter($filter_id): \qan\qan\OutputUninstallFilter
```

Uninstalls a filter with the given filter id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$filter_id = 'filter_id_example'; // string | The filter ID that needs to be uninstalled. It should always be called when watch is no longer needed. Additionally, Filters timeout when they aren't requested with getFilterChanges for a period of time

try {
    $result = $apiInstance->qanUninstallFilter($filter_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanUninstallFilter: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **filter_id** | **string**| The filter ID that needs to be uninstalled. It should always be called when watch is no longer needed. Additionally, Filters timeout when they aren&#39;t requested with getFilterChanges for a period of time | |

### Return type

[**\qan\qan\OutputUninstallFilter**](../Model/OutputUninstallFilter.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `qanXlinkValid()`

```php
qanXlinkValid($address): \qan\qan\OutputXlinkValid
```

Returns the xlink validity time of the account of given address.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new qan\Api\QANApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$address = 'address_example'; // string

try {
    $result = $apiInstance->qanXlinkValid($address);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling QANApi->qanXlinkValid: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **address** | **string**|  | |

### Return type

[**\qan\qan\OutputXlinkValid**](../Model/OutputXlinkValid.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/problem+json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
