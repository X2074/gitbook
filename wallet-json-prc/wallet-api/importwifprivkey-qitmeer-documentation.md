# importWifPrivKey :: Qitmeer Documentation

### wallet\_importWifPrivKey <a href="#wallet_importwifprivkey" id="wallet_importwifprivkey"></a>

#### info: 导入wif格式私钥 <a href="#info-dao-ru-wif-ge-shi-si-yue" id="info-dao-ru-wif-ge-shi-si-yue"></a>

#### args： <a href="#args" id="args"></a>

* accountName 导入账户,目前只支持imported
* privKey 私钥
* rescan bool,是否重新扫描交易记录

#### example: <a href="#example" id="example"></a>

```
{"id":1574750774018,"method":"wallet_importWifPrivKey","params":["imported","xxxxx",false]}
```
