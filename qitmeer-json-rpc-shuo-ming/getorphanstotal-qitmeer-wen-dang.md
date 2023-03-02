# getOrphansTotal :: Qitmeer 文档

### getOrphansTotal <a href="#getorphanstotal" id="getorphanstotal"></a>

#### 函数名 getOrphansTotal <a href="#han-shu-ming-getorphanstotal" id="han-shu-ming-getorphanstotal"></a>

#### 说明：无参数，得到当前节点的孤儿区块的数量。 <a href="#shuo-ming-wu-can-shu-de-dao-dang-qian-jie-dian-de-gu-er-qu-kuai-de-shu-liang" id="shuo-ming-wu-can-shu-de-dao-dang-qian-jie-dian-de-gu-er-qu-kuai-de-shu-liang"></a>

孤儿区块指当前未关联到DAG中的区块。

**实例**

```
curl -s -k -u test:test -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"2.0","method":"getOrphansTotal","params":[],"id":null}' https://127.0.0.1:18131
```

输出

```
{
  "jsonrpc": "2.0",
  "id": null,
  "result": 0
}

```
