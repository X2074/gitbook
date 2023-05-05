# Qitmeer-wallet RPC :: Qitmeer Documentation

### Qitmeer-wallet RPC Reference <a href="#qitmeer-wallet-rpc-reference" id="qitmeer-wallet-rpc-reference"></a>

Download Qitmeer Wallet from [github.com/Qitmeer/qitmeer-wallet](https://github.com/Qitmeer/qitmeer-wallet)

```
# run rpc or ul model  will support rpc interface

./qitmeer-wallet web
```

Usage:

RPC interface URL http://127.0.0.1:38130/api

```

curl -k -u "user:password" -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"1.0","method":"wallet_createAccount","params":["account"],"id":1}' http://127.0.0.1:38130/api | jq
```

### API List <a href="#api-list" id="api-list"></a>

### 1. wallet\_unlock {password} {second} <a href="#1-wallet_unlock-password-second" id="1-wallet_unlock-password-second"></a>

#### info: 解锁钱包 <a href="#info-jie-suo-qian-bao" id="info-jie-suo-qian-bao"></a>

#### args： <a href="#args" id="args"></a>

* password 钱包密码
* second 解锁时间,单位秒

#### example: <a href="#example" id="example"></a>

```
{"jsonrpc":"1.0","method":"wallet_unlock","params":["password",30],"id":1}
```

### 2. wallet\_lock <a href="#2-wallet_lock" id="2-wallet_lock"></a>

#### info：锁定钱包 <a href="#info-suo-ding-qian-bao" id="info-suo-ding-qian-bao"></a>

#### example: <a href="#example-1" id="example-1"></a>

```
{"jsonrpc":"1.0","method":"wallet_lock","params":[],"id":1}
```

### 3. wallet\_getAccountsAndBalance <a href="#3-wallet_getaccountsandbalance" id="3-wallet_getaccountsandbalance"></a>

#### info: 获取所有的账号和余额 <a href="#info-huo-qu-suo-you-de-zhang-hao-he-yu-e" id="info-huo-qu-suo-you-de-zhang-hao-he-yu-e"></a>

#### example: <a href="#example-2" id="example-2"></a>

```
{"jsonrpc":"1.0","method":"wallet_getAccountsAndBalance","params":[],"id":1}
```

result:

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": {
        "account": {
            "TotalAmount": 0,
            "SpendAmount": 0,
            "UnspendAmount": 0,
            "ConfirmAmount": 0
        },
        "default": {
            "TotalAmount": 280000000000,
            "SpendAmount": 0,
            "UnspendAmount": 280000000000,
            "ConfirmAmount": 0
        },
        "imported": {
            "TotalAmount": 11172999678800,
            "SpendAmount": 325000000000,
            "UnspendAmount": 8754999678800,
            "ConfirmAmount": 2418000000000
        }
    }
}

```

### 4. wallet\_createAccount {accountName} <a href="#4-wallet_createaccount-accountname" id="4-wallet_createaccount-accountname"></a>

#### info: 添加账户 <a href="#info-tian-jia-zhang-hu" id="info-tian-jia-zhang-hu"></a>

#### args： <a href="#args-1" id="args-1"></a>

* accountName 新账户名

#### example: <a href="#example-3" id="example-3"></a>

```
{"jsonrpc":"1.0","method":"wallet_createAccount","params":["accountName"],"id":1}
```

### 5. wallet\_getAddressesByAccount {accountName} <a href="#5-wallet_getaddressesbyaccount-accountname" id="5-wallet_getaddressesbyaccount-accountname"></a>

#### info: 获取账户所有的地址 <a href="#info-huo-qu-zhang-hu-suo-you-de-di-zhi" id="info-huo-qu-zhang-hu-suo-you-de-di-zhi"></a>

#### args： <a href="#args-2" id="args-2"></a>

* accountName 账户名

#### example: <a href="#example-4" id="example-4"></a>

```
{"jsonrpc":"1.0","method":"wallet_getAddressesByAccount","params":["default"],"id":1}
```

result:

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": [
        "TmSbEJs3nDmy68Af7M4Rsuj4pyAwcAret5a",
        "Tmbzp2af9Ereh2hRejcVH9mCQgYdY2GHCAa",
        "TmZu8zU1i6xbZMpLQZLMAJsyWHanZXUZtiV"
    ]
}
```

### 6. wallet\_createAddress {accountName} <a href="#6-wallet_createaddress-accountname" id="6-wallet_createaddress-accountname"></a>

#### info: 创建地址 <a href="#info-chuang-jian-di-zhi" id="info-chuang-jian-di-zhi"></a>

#### args： <a href="#args-3" id="args-3"></a>

* accountName 账户名

#### example: <a href="#example-5" id="example-5"></a>

```
{"jsonrpc":"1.0","method":"wallet_createAddress","params":["default"],"id":1}
```

result:

```
{
    "jsonrpc": "2.0",
    "id": 1,
    "result": "TmhMzHPCH6F2k3WYQkyvjhwAXoZt7q8TFv9"
}
```

#### info: 发送交易 <a href="#info-fa-song-jiao-yi" id="info-fa-song-jiao-yi"></a>

#### args： <a href="#args-4" id="args-4"></a>

* fromAccount from account
* toAddr send to address
* amount send amount coin
* comment
* commentTo

#### example: <a href="#example-6" id="example-6"></a>

```
{"id":1574828051839,"method":"wallet_sendToAddressByAccount","params":["default","TmZu8zU1i6xbZMpLQZLMAJsyWHanZXUZtiV",800,"",""]}
```

result:

```
{
    "jsonrpc": "2.0",
    "id": 1574828051839,
    "result": "b1ff3645c374992313e66d504fdf4fd3f2006f9414b97a7e1f6382328cc74fb1"
}
```

### 8. wallet\_getTxListByAddr {addr} {type} {page} {pageSize} <a href="#8-wallet_gettxlistbyaddr-addr-type-page-pagesize" id="8-wallet_gettxlistbyaddr-addr-type-page-pagesize"></a>

#### info: 获取地址相关交易列表 <a href="#info-huo-qu-di-zhi-xiang-guan-jiao-yi-lie-biao" id="info-huo-qu-di-zhi-xiang-guan-jiao-yi-lie-biao"></a>

#### args： <a href="#args-5" id="args-5"></a>

* addr
* type 0: in tx; 1: out tx; 2: all tx
* page
* pageSize

#### example: <a href="#example-7" id="example-7"></a>

```
{"id":1574750774018,"method":"wallet_getTxListByAddr","params":["TmhJcjphz3Y3jRysKT56JaH8m9pzAzsFMu7",2,-1,100]}
```

result:

```
{
    "jsonrpc": "2.0",
    "id": 1574750774018,
    "result": {
        "Total": 1,
        "Page": 1,
        "PageSize": 1000000000,
        "transactions": [
            {
                "hex": "",
                "txid": "47879fb9dea684e4ce6f24f30812d3832d11fee34400754c6d8b34cd7d7eba8f",
                "txhash": "937de7e15ec48e9cd58d79c594e7395015d5c663924ab5af929a9ef5e5f2e446",
                "size": 377,
                "version": 1,
                "locktime": 0,
                "expire": 0,
                "vin": [
                   ...
                ],
                "vout": [
                   ...
                ],
                "blockhash": "026c6c85a1ae0183fe2e8bfda3450b9990acf9b8c4af3e995f9e361c7bb3d4cd",
                "confirmations": 0
            }
        ]
    }
}
```

### 9. wallet\_importWifPrivKey {accountName} {privKey} {rescan} <a href="#9-wallet_importwifprivkey-accountname-privkey-rescan" id="9-wallet_importwifprivkey-accountname-privkey-rescan"></a>

#### info: 导入wif格式私钥 <a href="#info-dao-ru-wif-ge-shi-si-yue" id="info-dao-ru-wif-ge-shi-si-yue"></a>

#### args： <a href="#args-6" id="args-6"></a>

* accountName 导入账户,目前只支持imported
* privKey 私钥
* rescan bool,是否重新扫描交易记录

#### example: <a href="#example-8" id="example-8"></a>

```
{"id":1574750774018,"method":"wallet_importWifPrivKey","params":["imported","xxxxx",false]}
```

### 10. wallet\_dumpPrivKey {addr} <a href="#10-wallet_dumpprivkey-addr" id="10-wallet_dumpprivkey-addr"></a>

#### info: 导出地址wif格式私钥 <a href="#info-dao-chu-di-zhi-wif-ge-shi-si-yue" id="info-dao-chu-di-zhi-wif-ge-shi-si-yue"></a>

#### args： <a href="#args-7" id="args-7"></a>

* addr 地址

#### example: <a href="#example-9" id="example-9"></a>

```
{"id":1574829854509,"method":"wallet_dumpPrivKey","params":["Tmh3je9zbnHAvPfwwHhQsFSJmKkeRTtKqmV"]}
```

### 11. ui\_openWallet {pass} <a href="#11-ui_openwallet-pass" id="11-ui_openwallet-pass"></a>

#### info: 打开钱包 <a href="#info-da-kai-qian-bao" id="info-da-kai-qian-bao"></a>

#### args： <a href="#args-8" id="args-8"></a>

* pass 钱包密码

#### example: <a href="#example-10" id="example-10"></a>

```
{"jsonrpc":"1.0","method":"ui_openWallet","params":["pass"],"id":1}
```

### 12. wallet\_syncStats <a href="#12-wallet_syncstats" id="12-wallet_syncstats"></a>

#### info: 查看当前钱包同步高度 <a href="#info-cha-kan-dang-qian-qian-bao-tong-bu-gao-du" id="info-cha-kan-dang-qian-qian-bao-tong-bu-gao-du"></a>

#### args： <a href="#args-9" id="args-9"></a>

#### example: <a href="#example-11" id="example-11"></a>

```
{"jsonrpc":"1.0","method":"wallet_syncStats","params":[],"id":1}
```

result:

```
{
	"jsonrpc": "2.0",
	"id": 1,
	"result": {
		"Height": 20460
	}
}
```

### 13. wallet\_getUtxo {addr} <a href="#13-wallet_getutxo-addr" id="13-wallet_getutxo-addr"></a>

#### info: 获取指定地址可用utxo <a href="#info-huo-qu-zhi-ding-di-zhi-ke-yong-utxo" id="info-huo-qu-zhi-ding-di-zhi-ke-yong-utxo"></a>

#### args： <a href="#args-10" id="args-10"></a>

* addr 地址

#### example: <a href="#example-12" id="example-12"></a>

```
{"jsonrpc":"1.0","method":"wallet_getUtxo","params":["TmgD1mu8zMMV9aWmJrXqQYnWRhR9SBfDZG6"],"id":1}
```

result:

```
{
	"jsonrpc": "2.0",
	"id": 1,
	"result": [{
		"Txid": "54c47af3a17201c64a8f3b27164d4e09e8e38e05501b16bfd4f001caeddfa86a",
		"Index": 1,
		"Amount": 699925600
	}]
}
```

### 14. wallet\_importPrivKey {accountName} {privKey} {rescan} <a href="#14-wallet_importprivkey-accountname-privkey-rescan" id="14-wallet_importprivkey-accountname-privkey-rescan"></a>

#### info: 导入私钥 <a href="#info-dao-ru-si-yue" id="info-dao-ru-si-yue"></a>

#### args： <a href="#args-11" id="args-11"></a>

* accountName 导入账户,目前只支持imported
* privKey 私钥
* rescan bool,是否重新扫描交易记录

#### example: <a href="#example-13" id="example-13"></a>

```
{"jsonrpc":"1.0","method":"wallet_importPrivKey","params":["imported","xxxxxx",true],"id":1}
```

### 15. wallet\_getBalanceByAddr {addr} <a href="#15-wallet_getbalancebyaddr-addr" id="15-wallet_getbalancebyaddr-addr"></a>

#### info: 获取地址余额 <a href="#info-huo-qu-di-zhi-yu-e" id="info-huo-qu-di-zhi-yu-e"></a>

#### args： <a href="#args-12" id="args-12"></a>

* addr 地址

#### example: <a href="#example-14" id="example-14"></a>

```
{"jsonrpc":"1.0","method":"wallet_getBalanceByAddr","params":["TmfDniZnvsjdH98GsH4aetL3XQKFUTWPp4e",1],"id":16}
```

result:

```
{
	"jsonrpc": "2.0",
	"id": 16,
	"result": {
		"TotalAmount": 400000000,
		"SpendAmount": 0,
		"UnspendAmount": 400000000,
		"ConfirmAmount": 0
	}
}
```

### 15. wallet\_sendToAddressBatch {addr:amount} <a href="#15-wallet_sendtoaddressbatch-addramount" id="15-wallet_sendtoaddressbatch-addramount"></a>

#### info: 单地址批量交易 <a href="#info-dan-di-zhi-pi-liang-jiao-yi" id="info-dan-di-zhi-pi-liang-jiao-yi"></a>

#### args： <a href="#args-13" id="args-13"></a>

* addr 地址
* amount 金额

#### example: <a href="#example-15" id="example-15"></a>

```
{
	"id": 1578639635748,
	"method": "wallet_sendToAddressBatch",
	"params": [{
		"TmeUg4pxc14y64J5BQj4M7jKEryeYfJ4APh": 0.1,
		"TmU3Xwo1rnh4hTKBwifDYAccDrF3kxXaEFe": 0.2,
		"TmjbGfbcMN1nVVHdcvzmPA4ksKqGq4eEkXu": 0.3,
		"TmmWRCMcRZ1ZGdQEw2BwZ3ibsobATw4KTrw": 0.4
	}]
}
```

result:

```
{
    "jsonrpc": "2.0",
    "id": 1578639635748,
    "result": "d7a7d24d47bb66ad3d3185764808af730c9a9dbb5970686cf6e5a1d5f249923c"
}
```
