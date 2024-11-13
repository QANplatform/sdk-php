# QAN PHP SDK

This repository is guaranteed up-to-date with the upstream QAN API definitions, and leverages OpenAPI technology to stay consistent.

Versioning is based on SEMVER, meaning:

- Stable releases guarantee backwards compatibility for the same major versions.
- Minor releases will not contain breaking changes.
- Patch releases only focus on fixing issues.

## Documentation for API Endpoints

All URIs are relative to *https://rpc-testnet.qanplatform.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*QANApi* | [**qanBlockNumber**](docs/Api/QANApi.md#qanblocknumber) | **GET** /blockNumber/ | Returns the latest block number of the blockchain.
*QANApi* | [**qanCall**](docs/Api/QANApi.md#qancall) | **POST** /call/ | Executes a new message call immediately without creating a transaction on the block chain.
*QANApi* | [**qanChainId**](docs/Api/QANApi.md#qanchainid) | **GET** /chainId/ | Returns the current network/chain ID, used to sign replay-protected transaction introduced in EIP-155.
*QANApi* | [**qanEstimateGas**](docs/Api/QANApi.md#qanestimategas) | **POST** /estimateGas/ | Returns an estimation of gas for a given transaction.
*QANApi* | [**qanFeeHistory**](docs/Api/QANApi.md#qanfeehistory) | **POST** /feeHistory/ | Returns the collection of historical gas information.
*QANApi* | [**qanGasPrice**](docs/Api/QANApi.md#qangasprice) | **GET** /gasPrice/ | Returns the current gas price on the network in wei.
*QANApi* | [**qanGetBalance**](docs/Api/QANApi.md#qangetbalance) | **GET** /getBalance/{Address}/ | Returns the balance of the account of given address.
*QANApi* | [**qanGetBlockByHash**](docs/Api/QANApi.md#qangetblockbyhash) | **GET** /getBlockByHash/{Hash}/{TransactionDetailFlag}/ | Returns information of the block matching the given block hash.
*QANApi* | [**qanGetBlockByNumber**](docs/Api/QANApi.md#qangetblockbynumber) | **GET** /getBlockByNumber/{BlockNumber}/{TransactionDetailFlag}/ | Returns information of the block matching the given block number.
*QANApi* | [**qanGetBlockReceipts**](docs/Api/QANApi.md#qangetblockreceipts) | **GET** /getBlockReceipts/{BlockNumber}/ | Returns all transaction receipts for a given block.
*QANApi* | [**qanGetBlockTransactionCountByHash**](docs/Api/QANApi.md#qangetblocktransactioncountbyhash) | **GET** /getBlockTransactionCountByHash/{Hash}/ | Returns the number of transactions for the block matching the given block hash.
*QANApi* | [**qanGetBlockTransactionCountByNumber**](docs/Api/QANApi.md#qangetblocktransactioncountbynumber) | **GET** /getBlockTransactionCountByNumber/{BlockNumber}/ | Returns the number of transactions for the block matching the given block number.
*QANApi* | [**qanGetCode**](docs/Api/QANApi.md#qangetcode) | **GET** /getCode/{Address}/ | Returns the compiled bytecode of a smart contract.
*QANApi* | [**qanGetFilterChanges**](docs/Api/QANApi.md#qangetfilterchanges) | **GET** /getFilterChanges/{FilterId}/ | Polling method for a filter, which returns an array of events that have occurred since the last poll.
*QANApi* | [**qanGetFilterLogs**](docs/Api/QANApi.md#qangetfilterlogs) | **GET** /getFilterLogs/{Id}/ | Returns an array of all logs matching filter with given id.
*QANApi* | [**qanGetLogs**](docs/Api/QANApi.md#qangetlogs) | **POST** /getLogs/ | Returns an array of all logs matching a given filter object.
*QANApi* | [**qanGetProof**](docs/Api/QANApi.md#qangetproof) | **POST** /getProof/ | Returns the account and storage values of the specified account including the Merkle-proof.
*QANApi* | [**qanGetStorageAt**](docs/Api/QANApi.md#qangetstorageat) | **POST** /getStorageAt/ | Returns the value from a storage position at a given address.
*QANApi* | [**qanGetTransactionByBlockHashAndIndex**](docs/Api/QANApi.md#qangettransactionbyblockhashandindex) | **GET** /getTransactionByBlockHashAndIndex/{blockHash}/{index}/ | Returns information about a transaction given a blockhash and transaction index position.
*QANApi* | [**qanGetTransactionByBlockNumberAndIndex**](docs/Api/QANApi.md#qangettransactionbyblocknumberandindex) | **GET** /getTransactionByBlockNumberAndIndex/{blockNumber}/{index}/ | Returns information about a transaction given a block number and transaction index position.
*QANApi* | [**qanGetTransactionByHash**](docs/Api/QANApi.md#qangettransactionbyhash) | **GET** /getTransactionByHash/{hash}/ | Returns the information about a transaction from a transaction hash.
*QANApi* | [**qanGetTransactionCount**](docs/Api/QANApi.md#qangettransactioncount) | **GET** /getTransactionCount/{Address}/{BlockNumber}/ | Returns the number of transactions sent from an address.
*QANApi* | [**qanGetTransactionReceipt**](docs/Api/QANApi.md#qangettransactionreceipt) | **GET** /getTransactionReceipt/{Hash}/ | Returns the receipt of a transaction by transaction hash.
*QANApi* | [**qanMaxPriorityFeePerGas**](docs/Api/QANApi.md#qanmaxpriorityfeepergas) | **GET** /maxPriorityFeePerGas/ | Get the priority fee needed to be included in a block.
*QANApi* | [**qanNewBlockFilter**](docs/Api/QANApi.md#qannewblockfilter) | **GET** /newBlockFilter/ | Creates a filter in the node, to notify when a new block arrives.
*QANApi* | [**qanNewFilter**](docs/Api/QANApi.md#qannewfilter) | **POST** /newFilter/ | Creates a filter object, based on filter options, to notify when the state changes (logs).
*QANApi* | [**qanNewPendingTransactionFilter**](docs/Api/QANApi.md#qannewpendingtransactionfilter) | **GET** /newPendingTransactionFilter/ | Creates a filter in the node to notify when new pending transactions arrive.
*QANApi* | [**qanSendRawTransaction**](docs/Api/QANApi.md#qansendrawtransaction) | **POST** /sendRawTransaction/ | Creates new message call transaction or a contract creation for signed transactions.
*QANApi* | [**qanSyncing**](docs/Api/QANApi.md#qansyncing) | **GET** /syncing/ | Returns an object with the sync status of the node if the node is out-of-sync and is syncing. Returns null when the node is already in sync.
*QANApi* | [**qanUninstallFilter**](docs/Api/QANApi.md#qanuninstallfilter) | **GET** /uninstallFilter/{FilterId}/ | Uninstalls a filter with the given filter id.
*QANApi* | [**qanXlinkValid**](docs/Api/QANApi.md#qanxlinkvalid) | **GET** /xlinkValid/{Address}/ | Returns the xlink validity time of the account of given address.


## Documentation For Models

 - [ErrorDetail](docs/ErrorDetail.md)
 - [ErrorModel](docs/ErrorModel.md)
 - [EstimateGasObject](docs/EstimateGasObject.md)
 - [FilterObject](docs/FilterObject.md)
 - [InputCall](docs/InputCall.md)
 - [InputEstimateGas](docs/InputEstimateGas.md)
 - [InputFeeHistory](docs/InputFeeHistory.md)
 - [InputGetLogs](docs/InputGetLogs.md)
 - [InputGetProof](docs/InputGetProof.md)
 - [InputGetStorageAt](docs/InputGetStorageAt.md)
 - [InputNewFilter](docs/InputNewFilter.md)
 - [InputSendRawTransaction](docs/InputSendRawTransaction.md)
 - [InputSubscribe](docs/InputSubscribe.md)
 - [OutputAccounts](docs/OutputAccounts.md)
 - [OutputBlobBaseFee](docs/OutputBlobBaseFee.md)
 - [OutputBlockNumber](docs/OutputBlockNumber.md)
 - [OutputCall](docs/OutputCall.md)
 - [OutputChainId](docs/OutputChainId.md)
 - [OutputEstimateGas](docs/OutputEstimateGas.md)
 - [OutputFeeHistory](docs/OutputFeeHistory.md)
 - [OutputGasPrice](docs/OutputGasPrice.md)
 - [OutputGetAccount](docs/OutputGetAccount.md)
 - [OutputGetBalance](docs/OutputGetBalance.md)
 - [OutputGetBlockByHash](docs/OutputGetBlockByHash.md)
 - [OutputGetBlockByNumber](docs/OutputGetBlockByNumber.md)
 - [OutputGetBlockReceipts](docs/OutputGetBlockReceipts.md)
 - [OutputGetBlockTransactionCountByHash](docs/OutputGetBlockTransactionCountByHash.md)
 - [OutputGetBlockTransactionCountByNumber](docs/OutputGetBlockTransactionCountByNumber.md)
 - [OutputGetCode](docs/OutputGetCode.md)
 - [OutputGetFilterChanges](docs/OutputGetFilterChanges.md)
 - [OutputGetFilterLogs](docs/OutputGetFilterLogs.md)
 - [OutputGetLogs](docs/OutputGetLogs.md)
 - [OutputGetProof](docs/OutputGetProof.md)
 - [OutputGetStorageAt](docs/OutputGetStorageAt.md)
 - [OutputGetTransactionByBlockHashAndIndex](docs/OutputGetTransactionByBlockHashAndIndex.md)
 - [OutputGetTransactionByBlockNumberAndIndex](docs/OutputGetTransactionByBlockNumberAndIndex.md)
 - [OutputGetTransactionByHash](docs/OutputGetTransactionByHash.md)
 - [OutputGetTransactionCount](docs/OutputGetTransactionCount.md)
 - [OutputGetTransactionReceipt](docs/OutputGetTransactionReceipt.md)
 - [OutputGetUncleCountByBlockHash](docs/OutputGetUncleCountByBlockHash.md)
 - [OutputGetUncleCountByBlockNumber](docs/OutputGetUncleCountByBlockNumber.md)
 - [OutputMaxPriorityFeePerGas](docs/OutputMaxPriorityFeePerGas.md)
 - [OutputNewBlockFilter](docs/OutputNewBlockFilter.md)
 - [OutputNewFilter](docs/OutputNewFilter.md)
 - [OutputNewPendingTransactionFilter](docs/OutputNewPendingTransactionFilter.md)
 - [OutputSendRawTransaction](docs/OutputSendRawTransaction.md)
 - [OutputSubscribe](docs/OutputSubscribe.md)
 - [OutputSyncing](docs/OutputSyncing.md)
 - [OutputUninstallFilter](docs/OutputUninstallFilter.md)
 - [OutputUnsubscribe](docs/OutputUnsubscribe.md)
 - [ParamsTransaction](docs/ParamsTransaction.md)
 - [QanXlinkValidResponse](docs/QanXlinkValidResponse.md)
 - [ResponseBlock](docs/ResponseBlock.md)
 - [ResponseLog](docs/ResponseLog.md)
 - [ResponseStorageEntry](docs/ResponseStorageEntry.md)
 - [ResponseTransaction](docs/ResponseTransaction.md)
 - [ResponseTransactionReceipt](docs/ResponseTransactionReceipt.md)
 - [ResponseWithdrawals](docs/ResponseWithdrawals.md)
 - [SyncStatus](docs/SyncStatus.md)

## Acknowledgements

We would like to thank Smartbear and OpenAPITools tech for making building declarative APIs possible.
A huge benefit for the whole industry!
