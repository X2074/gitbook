# getBlockTotal :: Qitmeer 文档

### getBlockTotal <a href="#getblocktotal" id="getblocktotal"></a>

#### 函数名：getBlockTotal <a href="#han-shu-ming-getblocktotal" id="han-shu-ming-getblocktotal"></a>

#### 说明：无参数，该节点所有已知的区块总数量。 <a href="#shuo-ming-wu-can-shu-gai-jie-dian-suo-you-yi-zhi-de-qu-kuai-zong-shu-liang" id="shuo-ming-wu-can-shu-gai-jie-dian-suo-you-yi-zhi-de-qu-kuai-zong-shu-liang"></a>

该数量包含可能存在的当前还未被BlockDAG共识定序的区块

**实例**

```
$ curl -s -k -u test:test -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"2.0","method":"getBlockTotal","params":[],"id":1}' https://127.0.0.1:18131
```

输出

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": 21177
}
```
