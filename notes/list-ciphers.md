## BabaSSL list ciphers:

```
$ openssl ciphers -V -stdname | column -t | grep -E "(TLSv1.3|NTLS|SM)"
0x13,0x02  -  TLS_AES_256_GCM_SHA384                         -  TLS_AES_256_GCM_SHA384         TLSv1.3   Kx=any       Au=any    Enc=AESGCM(256)             Mac=AEAD
0x13,0x01  -  TLS_AES_128_GCM_SHA256                         -  TLS_AES_128_GCM_SHA256         TLSv1.3   Kx=any       Au=any    Enc=AESGCM(128)             Mac=AEAD
0x13,0x03  -  TLS_CHACHA20_POLY1305_SHA256                   -  TLS_CHACHA20_POLY1305_SHA256   TLSv1.3   Kx=any       Au=any    Enc=CHACHA20/POLY1305(256)  Mac=AEAD
0x00,0xC7  -  TLS_SM4_CCM_SM3                                -  TLS_SM4_CCM_SM3                TLSv1.3   Kx=any       Au=SM2    Enc=SM4-CCM(128)            Mac=AEAD
0x00,0xC6  -  TLS_SM4_GCM_SM3                                -  TLS_SM4_GCM_SM3                TLSv1.3   Kx=any       Au=SM2    Enc=SM4-GCM(128)            Mac=AEAD
0xE0,0x53  -  UNKNOWN                                        -  ECC-SM2-SM4-GCM-SM3            NTLSv1.1  Kx=SM2       Au=SM2    Enc=SM4-GCM(128)            Mac=AEAD
0xE0,0x51  -  UNKNOWN                                        -  ECDHE-SM2-SM4-GCM-SM3          NTLSv1.1  Kx=SM2DHE    Au=SM2    Enc=SM4-GCM(128)            Mac=AEAD
0xE0,0x13  -  UNKNOWN                                        -  ECC-SM2-SM4-CBC-SM3            NTLSv1.1  Kx=SM2       Au=SM2    Enc=SM4(128)                Mac=SM3
0xE0,0x11  -  UNKNOWN                                        -  ECDHE-SM2-SM4-CBC-SM3          NTLSv1.1  Kx=SM2DHE    Au=SM2    Enc=SM4(128)                Mac=SM3

$ openssl ciphers -V -stdname | column -t | grep -E "(TLS_ECDHE_ECDSA_WITH_AES|TLS_RSA_WITH_AES)"
0xC0,0x2C  -  TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384        -  ECDHE-ECDSA-AES256-GCM-SHA384  TLSv1.2   Kx=ECDH      Au=ECDSA  Enc=AESGCM(256)             Mac=AEAD
0xC0,0x2B  -  TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256        -  ECDHE-ECDSA-AES128-GCM-SHA256  TLSv1.2   Kx=ECDH      Au=ECDSA  Enc=AESGCM(128)             Mac=AEAD
0xC0,0x24  -  TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA384        -  ECDHE-ECDSA-AES256-SHA384      TLSv1.2   Kx=ECDH      Au=ECDSA  Enc=AES(256)                Mac=SHA384
0xC0,0x23  -  TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA256        -  ECDHE-ECDSA-AES128-SHA256      TLSv1.2   Kx=ECDH      Au=ECDSA  Enc=AES(128)                Mac=SHA256
0xC0,0x0A  -  TLS_ECDHE_ECDSA_WITH_AES_256_CBC_SHA           -  ECDHE-ECDSA-AES256-SHA         TLSv1     Kx=ECDH      Au=ECDSA  Enc=AES(256)                Mac=SHA1
0xC0,0x09  -  TLS_ECDHE_ECDSA_WITH_AES_128_CBC_SHA           -  ECDHE-ECDSA-AES128-SHA         TLSv1     Kx=ECDH      Au=ECDSA  Enc=AES(128)                Mac=SHA1
0x00,0x9D  -  TLS_RSA_WITH_AES_256_GCM_SHA384                -  AES256-GCM-SHA384              TLSv1.2   Kx=RSA       Au=RSA    Enc=AESGCM(256)             Mac=AEAD
0x00,0x9C  -  TLS_RSA_WITH_AES_128_GCM_SHA256                -  AES128-GCM-SHA256              TLSv1.2   Kx=RSA       Au=RSA    Enc=AESGCM(128)             Mac=AEAD
0x00,0x3D  -  TLS_RSA_WITH_AES_256_CBC_SHA256                -  AES256-SHA256                  TLSv1.2   Kx=RSA       Au=RSA    Enc=AES(256)                Mac=SHA256
0x00,0x3C  -  TLS_RSA_WITH_AES_128_CBC_SHA256                -  AES128-SHA256                  TLSv1.2   Kx=RSA       Au=RSA    Enc=AES(128)                Mac=SHA256
0x00,0x35  -  TLS_RSA_WITH_AES_256_CBC_SHA                   -  AES256-SHA                     SSLv3     Kx=RSA       Au=RSA    Enc=AES(256)                Mac=SHA1
0x00,0x2F  -  TLS_RSA_WITH_AES_128_CBC_SHA                   -  AES128-SHA                     SSLv3     Kx=RSA       Au=RSA    Enc=AES(128)                Mac=SHA1
```

## BabaSSL version:

```
$ which openssl
/opt/babassl/bin/openssl

$ openssl version
BabaSSL 8.3.0-dev
OpenSSL 1.1.1h  22 Sep 2020

$ openssl version -f
compiler: gcc -fPIC -pthread -m64 -Wa,--noexecstack -g -O3 -feliminate-unused-debug-types -pipe -Wall -Wp,-D_FORTIFY_SOURCE=2 -fexceptions -Wformat -Wformat-security -m64 -fasynchronous-unwind-tables -Wp,-D_REENTRANT -ftree-loop-distribute-patterns -Wl,-z -Wl,now -Wl,-z -Wl,relro -fno-semantic-interposition -ffat-lto-objects -fno-trapping-math -Wl,-sort-common -Wl,--enable-new-dtags -mtune=skylake  -fPIC -DOPENSSL_USE_NODELETE -DL_ENDIAN -DOPENSSL_PIC -DOPENSSL_CPUID_OBJ -DOPENSSL_IA32_SSE2 -DOPENSSL_BN_ASM_MONT -DOPENSSL_BN_ASM_MONT5 -DOPENSSL_BN_ASM_GF2m -DSHA1_ASM -DSHA256_ASM -DSHA512_ASM -DKECCAK1600_ASM -DRC4_ASM -DMD5_ASM -DAESNI_ASM -DVPAES_ASM -DGHASH_ASM -DECP_NISTZ256_ASM -DX25519_ASM -DPOLY1305_ASM -DNDEBUG
```

## Refs
- https://www.openssl.org/docs/man1.1.1/man1/ciphers.html
- https://www.redhat.com/sysadmin/6-openssl-commands
- https://www.jianshu.com/p/8010163f424c
