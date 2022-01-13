```console
$ openssl s_client -connect sm2test.ovssl.cn:443
CONNECTED(00000003)
depth=2 C = US, ST = New Jersey, L = Jersey City, O = The USERTRUST Network, CN = USERTrust RSA Certification Authority
verify error:num=20:unable to get local issuer certificate
verify return:1
depth=1 C = CN, O = WoTrus CA Limited, CN = WoTrus DV Server CA  [Run by the Issuer]
verify return:1
depth=0 CN = sm2test.ovssl.cn
verify return:1
---
Certificate chain
 0 s:CN = sm2test.ovssl.cn
   i:C = CN, O = WoTrus CA Limited, CN = WoTrus DV Server CA  [Run by the Issuer]
 1 s:C = CN, O = WoTrus CA Limited, CN = WoTrus DV Server CA  [Run by the Issuer]
   i:C = US, ST = New Jersey, L = Jersey City, O = The USERTRUST Network, CN = USERTrust RSA Certification Authority
 2 s:C = US, ST = New Jersey, L = Jersey City, O = The USERTRUST Network, CN = USERTrust RSA Certification Authority
   i:C = GB, ST = Greater Manchester, L = Salford, O = Comodo CA Limited, CN = AAA Certificate Services
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIFojCCBIqgAwIBAgIRALj0FNsGI9A0OT+5kttPryYwDQYJKoZIhvcNAQELBQAw
XDELMAkGA1UEBhMCQ04xGjAYBgNVBAoTEVdvVHJ1cyBDQSBMaW1pdGVkMTEwLwYD
VQQDDChXb1RydXMgRFYgU2VydmVyIENBICBbUnVuIGJ5IHRoZSBJc3N1ZXJdMB4X
DTIxMDQwNzAwMDAwMFoXDTIyMDQwNzIzNTk1OVowGzEZMBcGA1UEAxMQc20ydGVz
dC5vdnNzbC5jbjCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEBAMOlr+WG
ZhVplvHxD0eWiBK/Ju4FHLBzeLX/zKHbd8Yf8zkk73GA+hWLnNRwTmZ7uwxYSFpe
bogVyc0BYwUfRvbVlSz6XbABNmOD9LHjN8rBqPn+RCRetokB2Hjw9WtV7ldF59q3
fstBLl5Z+tYxWxVXqlybbBhlTctkivFVskXkVa1usuCcYpFhisxgDmDGlQM/D/QK
xC6icUpCHvDmqK/E3U6Q0x1jXC3gaWMNKab+0BCB6krV12slcrDhuiSYdMNGBs7r
ab2Y6gznV//VT9/ajp9d5FyBJP41rBaLmhMaCU6iqi9kMCa8+T2nTAd4r9MfQOXa
dv/qRLsk5wYixe8CAwEAAaOCAp4wggKaMB8GA1UdIwQYMBaAFJmbLfaL8KPbidSe
++V0L2jSkE/kMB0GA1UdDgQWBBSJz+8Ynhv/Fc8zDw4SIm3vJgxl6TAOBgNVHQ8B
Af8EBAMCBaAwDAYDVR0TAQH/BAIwADAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYB
BQUHAwIwSQYDVR0gBEIwQDA0BgsrBgEEAbIxAQICFjAlMCMGCCsGAQUFBwIBFhdo
dHRwczovL3NlY3RpZ28uY29tL0NQUzAIBgZngQwBAgEwPQYDVR0fBDYwNDAyoDCg
LoYsaHR0cDovL2NybC5jcmxvY3NwLmNuL1dvVHJ1c0RWU2VydmVyQ0FfMi5jcmww
bAYIKwYBBQUHAQEEYDBeMDgGCCsGAQUFBzAChixodHRwOi8vYWlhLmNybG9jc3Au
Y24vV29UcnVzRFZTZXJ2ZXJDQV8yLmNydDAiBggrBgEFBQcwAYYWaHR0cDovL29j
c3AuY3Jsb2NzcC5jbjCCAQQGCisGAQQB1nkCBAIEgfUEgfIA8AB2AEalVet1+pEg
MLWiiWn0830RLEF0vv1JuIWr8vxw/m1HAAABeKsAdYAAAAQDAEcwRQIhAIAGzXru
W3lVn9ZI58QfT5RJMqnOAm8/YyBgA7RpZPrCAiA9DyuUoqO0VyYkHA8U5iTzydiU
MINGRkcsYTwEW+/aAwB2AN+lXqtogk8fbK3uuF9OPlrqzaISpGpejjsSwCBEXCpz
AAABeKsAdWMAAAQDAEcwRQIgNcB0g7TcRoE8busLZHGO4CHdnBS/Oo/l80U1+/5s
rmICIQC/RqV1ZSWbbvDdIEQJjcW69OzQHHWOuYFL13YyddG/nzAbBgNVHREEFDAS
ghBzbTJ0ZXN0Lm92c3NsLmNuMA0GCSqGSIb3DQEBCwUAA4IBAQANOjjdAmSLL4rq
iDpEbrGWN75Ghd2FAngJzwwyNoTKNB86a1cuqvNdv48BCv6ZOx3pLnN/F8u5rDyp
u85L/aUFY4ySk3PimEkqNiFpPhTCttDTkLY+xMrDkpxIoMZj5DDCgW4u7GRta2I6
mXL4R7QMux7PSnxrUlFgGqLIhoDFe8NEiBE9AX9ap23hUeQrWBBi008UCTNm/0GI
j7nfja5ecS5DXQVhL0qaBUafyYOsA0YZhApqV6/R4DsAfb4Mem64VPs7wczFnxdh
XndWJON40sUVxSJ7ettgVgekxMV4vsV8zBg1a1gt6YrnlbaIbpUcgbIv/B3NBTc6
vnf6NZIa
-----END CERTIFICATE-----
subject=CN = sm2test.ovssl.cn

issuer=C = CN, O = WoTrus CA Limited, CN = WoTrus DV Server CA  [Run by the Issuer]

---
No client certificate CA names sent
---
SSL handshake has read 4739 bytes and written 644 bytes
Verification error: unable to get local issuer certificate
---
New, TLSv1.2, Cipher is AES256-GCM-SHA384
Server public key is 2048 bit
Secure Renegotiation IS supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
SSL-Session:
    Protocol  : TLSv1.2
    Cipher    : AES256-GCM-SHA384
    Session-ID: 7ACDBF6809BCF6286A4389BEABABD92FA061E4DA2C5BE036C9D6DBBB666F921D
    Session-ID-ctx:
    Master-Key: 1DDB8514EAEC14E1D0C2EC9C4A80BF9AD66A091E6970F8F3B587D78C5B18BD58F683FC651D2BD7E847B951958F9A3AF1
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - 31 80 b1 3a 72 5a 3a cb-66 c0 31 de 1e 3c 47 b3   1..:rZ:.f.1..<G.
    0010 - f4 3e 94 3e 0f 0d 5a 30-45 13 42 26 c8 20 3c b8   .>.>..Z0E.B&. <.
    0020 - 60 69 35 f4 b4 dc 06 ae-68 bd f5 43 76 cc 17 5f   `i5.....h..Cv.._
    0030 - d7 eb bb e3 8f a8 37 dc-1d 5c 69 21 4f ef 3b 01   ......7..\i!O.;.
    0040 - b3 47 1c 29 56 c5 01 b1-65 97 80 ad 78 fc 27 c1   .G.)V...e...x.'.
    0050 - 98 4b 5e e6 41 3b c5 5a-d1 12 88 22 a1 48 6b af   .K^.A;.Z...".Hk.
    0060 - 27 29 af 2f ed a2 df 38-bd 2d 93 a4 4e 81 18 32   ')./...8.-..N..2
    0070 - 4c fb f7 ee 2f 0c 29 ca-85 95 dc 2d 76 b3 a2 68   L.../.)....-v..h
    0080 - 31 e8 45 7c b4 e4 5f 88-5b e9 91 3a ef f3 8b db   1.E|.._.[..:....
    0090 - 69 e0 9d fb 12 de 69 5a-32 10 29 00 96 2a cc 63   i.....iZ2.)..*.c
    00a0 - 03 4a 2c 49 50 63 d4 8a-7d 5d bf 68 bf 5e 8e 22   .J,IPc..}].h.^."
    00b0 - 6d 06 ef a6 10 21 ab 58-2b c8 55 0a 76 00 0e d9   m....!.X+.U.v...
    00c0 - 0f c0 c1 38 1a f9 fc 0a-fd 83 62 2e d6 7d 3d 4d   ...8......b..}=M

    Start Time: 1641978231
    Timeout   : 7200 (sec)
    Verify return code: 20 (unable to get local issuer certificate)
    Extended master secret: yes
    QUIC: no
---
```
