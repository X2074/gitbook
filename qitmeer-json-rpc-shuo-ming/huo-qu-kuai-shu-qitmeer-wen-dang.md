# 获取块数 :: Qitmeer 文档

### getBlockCount <a href="#getblockcount" id="getblockcount"></a>

#### 函数名：getBlockCount <a href="#han-shu-ming-getblockcount" id="han-shu-ming-getblockcount"></a>

#### 说明：无参数，当前已定序的区块数量。 <a href="#shuo-ming-wu-can-shu-dang-qian-yi-ding-xu-de-qu-kuai-shu-liang" id="shuo-ming-wu-can-shu-dang-qian-yi-ding-xu-de-qu-kuai-shu-liang"></a>

该数量-1即为当前最大的Block order

**实例**

```
$ curl -s -k -u test:test -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"2.0","method":"getBlockCount","params":[],"id":1}' https://127.0.0.1:18131
```

输出

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": 21177
}
```
