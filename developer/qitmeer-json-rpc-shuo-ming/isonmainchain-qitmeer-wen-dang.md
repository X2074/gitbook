# isOnMainChain :: Qitmeer 文档

### isOnMainChain <a href="#isonmainchain" id="isonmainchain"></a>

#### 函数名 isOnMainChain {blockhash} <a href="#han-shu-ming-isonmainchainblockhash" id="han-shu-ming-isonmainchainblockhash"></a>

#### 说明：判断该block是否在主链上 <a href="#shuo-ming-pan-duan-gai-block-shi-fou-zai-zhu-lian-shang" id="shuo-ming-pan-duan-gai-block-shi-fou-zai-zhu-lian-shang"></a>

**实例**

```
curl -s -k -u test:test -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"2.0","method":"isOnMainChain","params":["0011cc2a9cea757a2aaa235f27f41f00e3e2ed87282175fe76767c4f50b3aa05"],"id":1}' https://127.0.0.1:18131
```

输出

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": "true"
}
```
