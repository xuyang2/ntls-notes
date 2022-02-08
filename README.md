# ntls-notes

> *NTLS 的全名为 National TLS，即我国核准的传输层安全协议，所以也可以叫做国密 TLS。*
>
> Source: https://mp.weixin.qq.com/s/0aM9tL9PdraoQXMsduOsJg

## 标准
- GB/T 38636-2020 信息安全技术 传输层密码协议（TLCP）
  - http://openstd.samr.gov.cn/bzgk/gb/newGbInfo?hcno=778097598DA2761E94A5FF3F77BD66DA
- ~~GM/T 0024-2014 SSL VPN 技术规范~~
  - [密码行业标准化技术委员会](http://www.gmbz.org.cn/)
    - [标准列表](http://www.gmbz.org.cn/main/bzlb.html)
    - [文件查看](http://www.gmbz.org.cn/main/viewfile/20180110021416665180.html)
- RFC 8998 ShangMi (SM) Cipher Suites for TLS 1.3
  - https://www.rfc-editor.org/rfc/rfc8998.html

## 算法套件

### 《GB/T 38636-2020》
	每个密码套件包括一个密钥交换算法，一个加密算法及密钥长度，和一个校验算法。
	在本标准中实现 ECC 和 ECDHE 的算法为 SM2;
	实现 IBC 和 IBSDH 的算法为 SM9。

密码套件列表：

| 名称                   | 密钥交换  |     加密  |     效验 | 值           |
|----------------------|-------|---------|--------|-------------|
| ECDHE_SM4_CBC_SM3    | ECDHE | SM4_CBC | SM3    | {0xe0,0x11} |
| ECDHE_SM4_GCM_SM3    | ECDHE | SM4_GCM | SM3    | {0xe0,0x51} |
| ECC_SM4_CBC_SM3      | ECC   | SM4_CBC | SM3    | {0xe0,0x13} |
| ECC_SM4_GCM_SM3      | ECC   | SM4_GCM | SM3    | {0xe0,0x53} |
| IBSDH_SM4_CBC_SM3    | IBSDH | SM4_CBC | SM4    | {0xe0,0x15} |
| IBSDH_SM4_GCM_SM3    | IBSDH | SM4_GCM | SM4    | {0xe0,0x55} |
| IBC_SM4_CBC_SM3      | IBC   | SM4_CBC | SM3    | {0xe0,0x17} |
| IBC_SM4_GCM_SM3      | IBC   | SM4_GCM | SM3    | {0xe0,0x57} |
| RSA_SM4_CBC_SM3      | RSA   | SM4_CBC | SM3    | {0xe0,0x19} |
| RSA_SM4_GCM_SM3      | RSA   | SM4_GCM | SM3    | {0xe0,0x59} |
| RSA_SM4_CBC_SHA256   | RSA   | SM4_CBC | SHA256 | {0xe0,0x1c} |
| RSA_SM4_GCM_SHA256   | RSA   | SM4_GCM | SHA256 | {0xe0,0x5a} |


### 《GM/T 0024-2014》
	每个密码套件包括一个密钥交换算法，一个加密算法，和一个校验算法。
	在本标准中实现 ECC 和 ECDHE 的算法为 SM2;
	实现 IBC 和 IBSDH 的算法为 SM9;

密码套件列表：

| 序号  | 名称            | 值           |
|-----|---------------|-------------|
| 1   | ECDHE_SM1_SM3 | {0xe0,0x01} |
| 2   | ECC_SM1_SM3   | {0xe0,0x03} |
| 3   | IBSDH_SM1_SM3 | {0xe0,0x05} | 
| 4   | IBC_SM1_SM3   | {0xe0,0x07} |
| 5   | RSA_SM1_SM3   | {0xe0,0x09} | 
| 6   | RSA_SM1_SHA1  | {0xe0,0x0a} |
| 7   | ECDHE_SM4_SM3 | {0xe0,0x11} |
| 8   | ECC_SM4_SM3   | {0xe0,0x13} |
| 9   | IBSDH_SM4_SM3 | {0xe0,0x15} |
| 10  | IBC_SM4_SM3   | {0xe0,0x17} |
| 11  | RSA_SM4_SM3   | {0xe0,0x19} |
| 12  | RSA_SM4_SHA1  | {0xe0,0x1a} |

常用算法套件：
- `ECC_SM4_SM3`
- `ECDHE_SM4_SM3`


## 文章

- [catbro666.github.io](https://catbro666.github.io/)
  - [一篇文章搞懂密码学基础及SSL/TLS协议](https://catbro666.github.io/posts/e92ef4b4/index.html)
  - [SSL及GMVPN握手协议详解](https://catbro666.github.io/posts/59c71edb/)

- [Jupiterliu.github.io](https://github.com/Jupiterliu/Jupiterliu.github.io/)
    - [国密算法/协议/工控](https://github.com/Jupiterliu/Jupiterliu.github.io/blob/5aff3927cc3cf5919b9a66be51b0a1cdf4a935b7/2021/04/28/%E5%9B%BD%E5%AF%86%E7%AE%97%E6%B3%95-%E5%8D%8F%E8%AE%AE-%E5%B7%A5%E6%8E%A7/index.html)

- [SOFAStack](https://www.sofastack.tech)
  - [RFC8998+BabaSSL---让国密驶向更远的星辰大海](https://www.sofastack.tech/blog/rfc8998-babassllet-guomi-sail-to-a-farther-starry-sea/)
  - [Tengine + BabaSSL ，让国密更易用](https://www.sofastack.tech/tengine-babassl-making-state-secrets-easier-to-use/)

## 测试

- [纽创信安 SSL/TLS 安全测试](https://securetls.cn/)
- [中国金融认证中心（CFCA）]
  - [CFCA数字证书下载平台](https://cs.cfca.com.cn/)
  - [普通SM2服务器测试证书下载地址](https://cs.cfca.com.cn/cgi-bin/compoundCertDownload/v_input.do)
  - [Certification Practice Statement Of CFCA Global-Trust System](https://www.cfca.com.cn/upload/CertificationPracticeStatementOfCFCAGlobal-TrustSystem20210811ENG.pdf)
  - [测试证书下载地址](http://cstest.cfca.com.cn)
  - [CFCA数字证书证书申请制作流程](https://www.cnblogs.com/wangqinyou/p/10696856.html)
