# isBlue :: Qitmeer 文档

### isBlue <a href="#isblue" id="isblue"></a>

#### 函数名：isBlue {blockhash} <a href="#han-shu-ming-isblueblockhash" id="han-shu-ming-isblueblockhash"></a>

#### 说明：通过节点判断该块是否为蓝色区块 <a href="#shuo-ming-tong-guo-jie-dian-pan-duan-gai-kuai-shi-fou-wei-lan-se-qu-kuai" id="shuo-ming-tong-guo-jie-dian-pan-duan-gai-kuai-shi-fou-wei-lan-se-qu-kuai"></a>

* blockhash：区块hash

#### 结果说明： <a href="#jie-guo-shuo-ming" id="jie-guo-shuo-ming"></a>

* 0:为红色区块，该块coinbase不能交易
* 1:为蓝色区块，该块的coinbase可以交易
* 2:还不能确定是蓝色或红色，待确认

**实例1**

```
$ curl -s -k -u test:test -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"2.0","method":"isBlue","params":["0003409cc9bcfc328630982797326e62135d6fc2431db7b85c2a0fe38ff5749c"],"id":1}' https://127.0.0.1:18131
```

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": 2
}
```

**实例2**

可以观察到对于是否蓝色区块的判断结果，由2变为1。即由不能确认变为蓝色区块。

```
$ date
Wed Jul  1 12:23:39 CST 2020
$ curl -s -k -u test:test -X POST -H 'Content-Type: application/json' --data '{"jsonrpc":"2.0","method":"isBlue","params":
["0003409cc9bcfc328630982797326e62135d6fc2431db7b85c2a0fe38ff5749c"],"id":1}' https://127.0.0.1:18131
```

```
{
  "jsonrpc": "2.0",
  "id": 1,
  "result": 1
}
```
