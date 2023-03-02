# getMempool :: Qitmeer 文档

### getMempool <a href="#getmempool" id="getmempool"></a>

#### 函数名：getMempool {txtype} {verbose} <a href="#han-shu-ming-getmempooltxtypeverbose" id="han-shu-ming-getmempooltxtypeverbose"></a>

#### 说明： <a href="#shuo-ming" id="shuo-ming"></a>

* txType: 交易类型，目前只支持regular。
* verbose：显示详细信息，目前只支持false。

**实例**

```
curl -s -k -u test:test -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"2.0","method":"getMempool","params":["regular",false],"id":1}' https://127.0.0.1:18131
```

输出

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": [
    "8df1c9019dd7110e9c3a421f62973ff245cbad435452808363ac291bf2265613"
  ]
}
```
