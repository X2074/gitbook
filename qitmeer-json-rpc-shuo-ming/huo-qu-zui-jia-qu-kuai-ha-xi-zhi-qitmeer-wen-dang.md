# 获取最佳区块哈希值 :: Qitmeer 文档

### getBestBlocktHash <a href="#getbestblockthash" id="getbestblockthash"></a>

#### 函数名：getBestBlockHash <a href="#han-shu-ming-getbestblockhash" id="han-shu-ming-getbestblockhash"></a>

#### 说明：无参数，获取当前最大区块Order的区块hash <a href="#shuo-ming-wu-can-shu-huo-qu-dang-qian-zui-da-qu-kuai-order-de-qu-kuai-hash" id="shuo-ming-wu-can-shu-huo-qu-dang-qian-zui-da-qu-kuai-order-de-qu-kuai-hash"></a>

#### 实例 <a href="#shi-li" id="shi-li"></a>

```
curl -s -k -u test:test -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"2.0","method":"getBestBlockHash","params":[],"id":1}' https://127.0.0.1:18131
```

输出

```

{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "000044c83486609eee3c5bb46cd539eb022ea05ed86c40ef4e6710357f225ea3"
}
```
