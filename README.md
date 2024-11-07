# Zero-Https
Zero-Https
# 1. 概述
## 1.1 简介
>HTTPS，也称作HTTP over TLS。TLS的前身是SSL，TLS 1.0通常被标示为SSL 3.1，TLS 1.1为SSL 3.2，TLS 1.2为SSL 3.3 HTTPS和HTTP协议相比提供了 
> 1. 数据完整性：内容传输经过完整性校验 
> 2. 数据隐私性：内容经过对称加密，每个连接生成一个唯一的加密密钥 
> 3. 身份认证：第三方无法伪造服务端(客户端)身份 

> 其中，数据完整性和隐私性由TLS Record Protocol保证，身份认证由TLS Handshaking Protocols实现。

# 2. 功能

# 3. 使用
## 3.1 证书生成
```shell
# 自签名证书
keytool -genkey -alias tomcat -storetype PKCS12 -keyalg RSA -keysize 2048 -keystore keystore.p12 -validity 3650
```
> 1. -genkey: 生成SSL证书 
> 2. -alias: 证书别名 
> 3. -storetype: 秘钥仓库类型 
> 4. -keyalg: 生成证书算法 
> 5. -keysize: 证书大小 
> 6. -keystore: 生成证书保存路径 
> 7. -validity: 证书有效期

> 将当前目录下keystore.p12，放到自己的springboot项目中的resource下

## 3.2 申请CA证书
> google搜索一下免费的ssl证书 <br/>
> [免费申请HTTPS证书六大方法](https://zhuanlan.zhihu.com/p/138792764)

# 4. 其他

# 5. 参考