```console
$ openssl s_client -crlf -connect ebssec.boc.cn:443 \
    -cipher ECC-SM2-WITH-SM4-SM3 \
    -enable_ntls -ntls
CONNECTED(00000003)
depth=0 C = CN, ST = \E5\8C\97\E4\BA\AC, L = \E5\8C\97\E4\BA\AC, O = \E4\B8\AD\E5\9B\BD\E9\93\B6\E8\A1\8C\E8\82\A1\E4\BB\BD\E6\9C\89\E9\99\90\E5\85\AC\E5\8F\B8, OU = Local RA, OU = SSL, CN = ebssec.boc.cn
verify error:num=20:unable to get local issuer certificate
verify return:1
depth=0 C = CN, ST = \E5\8C\97\E4\BA\AC, L = \E5\8C\97\E4\BA\AC, O = \E4\B8\AD\E5\9B\BD\E9\93\B6\E8\A1\8C\E8\82\A1\E4\BB\BD\E6\9C\89\E9\99\90\E5\85\AC\E5\8F\B8, OU = Local RA, OU = SSL, CN = ebssec.boc.cn
verify error:num=21:unable to verify the first certificate
verify return:1
depth=0 C = CN, ST = \E5\8C\97\E4\BA\AC, L = \E5\8C\97\E4\BA\AC, O = \E4\B8\AD\E5\9B\BD\E9\93\B6\E8\A1\8C\E8\82\A1\E4\BB\BD\E6\9C\89\E9\99\90\E5\85\AC\E5\8F\B8, OU = Local RA, OU = SSL, CN = ebssec.boc.cn
verify error:num=20:unable to get local issuer certificate
verify return:1
depth=0 C = CN, ST = \E5\8C\97\E4\BA\AC, L = \E5\8C\97\E4\BA\AC, O = \E4\B8\AD\E5\9B\BD\E9\93\B6\E8\A1\8C\E8\82\A1\E4\BB\BD\E6\9C\89\E9\99\90\E5\85\AC\E5\8F\B8, OU = Local RA, OU = SSL, CN = ebssec.boc.cn
verify error:num=21:unable to verify the first certificate
verify return:1
---
Certificate chain
 0 s:C = CN, ST = \E5\8C\97\E4\BA\AC, L = \E5\8C\97\E4\BA\AC, O = \E4\B8\AD\E5\9B\BD\E9\93\B6\E8\A1\8C\E8\82\A1\E4\BB\BD\E6\9C\89\E9\99\90\E5\85\AC\E5\8F\B8, OU = Local RA, OU = SSL, CN = ebssec.boc.cn
   i:C = CN, O = CFCA SM2 OCA1
 1 s:C = CN, ST = \E5\8C\97\E4\BA\AC, L = \E5\8C\97\E4\BA\AC, O = \E4\B8\AD\E5\9B\BD\E9\93\B6\E8\A1\8C\E8\82\A1\E4\BB\BD\E6\9C\89\E9\99\90\E5\85\AC\E5\8F\B8, OU = Local RA, OU = SSL, CN = ebssec.boc.cn
   i:C = CN, O = CFCA SM2 OCA1
---
Server certificate
-----BEGIN CERTIFICATE-----
MIICzzCCAnKgAwIBAgIFEzY5M3AwDAYIKoEcz1UBg3UFADAlMQswCQYDVQQGEwJD
TjEWMBQGA1UECgwNQ0ZDQSBTTTIgT0NBMTAeFw0yMTA2MTEwOTA1MjBaFw0yNjA2
MTkwODE2NTZaMIGRMQswCQYDVQQGEwJDTjEPMA0GA1UECAwG5YyX5LqsMQ8wDQYD
VQQHDAbljJfkuqwxJzAlBgNVBAoMHuS4reWbvemTtuihjOiCoeS7veaciemZkOWF
rOWPuDERMA8GA1UECwwITG9jYWwgUkExDDAKBgNVBAsMA1NTTDEWMBQGA1UEAwwN
ZWJzc2VjLmJvYy5jbjBZMBMGByqGSM49AgEGCCqBHM9VAYItA0IABPsNUnoZQM9C
SnvC57TbvdfyOTCuPOSlZmPAyxBKFj+Y1QH/xlubHdVf5XqHrO1jCDRi7aN5IKGX
QF1492c803OjggEeMIIBGjAfBgNVHSMEGDAWgBRck1ggWiRzVhAbZFAQ7OmnygdB
ETAMBgNVHRMBAf8EAjAAMEgGA1UdIARBMD8wPQYIYIEchu8qAQEwMTAvBggrBgEF
BQcCARYjaHR0cDovL3d3dy5jZmNhLmNvbS5jbi91cy91cy0xNC5odG0wNwYDVR0f
BDAwLjAsoCqgKIYmaHR0cDovL2NybC5jZmNhLmNvbS5jbi9TTTIvY3JsNTYxOC5j
cmwwGAYDVR0RBBEwD4INZWJzc2VjLmJvYy5jbjAOBgNVHQ8BAf8EBAMCBsAwHQYD
VR0OBBYEFJ6oFo/OrKgDhHFORpaq04kX7T1KMB0GA1UdJQQWMBQGCCsGAQUFBwMC
BggrBgEFBQcDATAMBggqgRzPVQGDdQUAA0kAMEYCIQCvhSvbv5h6ERl1YcCLg+fz
9UleQbaPfBYwUjUD2dAHVQIhAMRC4k9S/mSC0UpUvCqh/DQC2Ui8Tccd5G2IgYSs
cnUN
-----END CERTIFICATE-----
subject=C = CN, ST = \E5\8C\97\E4\BA\AC, L = \E5\8C\97\E4\BA\AC, O = \E4\B8\AD\E5\9B\BD\E9\93\B6\E8\A1\8C\E8\82\A1\E4\BB\BD\E6\9C\89\E9\99\90\E5\85\AC\E5\8F\B8, OU = Local RA, OU = SSL, CN = ebssec.boc.cn

issuer=C = CN, O = CFCA SM2 OCA1

---
No client certificate CA names sent
---
SSL handshake has read 1910 bytes and written 339 bytes
Verification error: unable to verify the first certificate
---
New, NTLSv1.1, Cipher is ECC-SM2-SM4-CBC-SM3
Server public key is 256 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
SSL-Session:
    Protocol  : NTLSv1.1
    Cipher    : ECC-SM2-SM4-CBC-SM3
    Session-ID: B63FFDDEEACAED81654DBBAD2D3FD108446E8C084DF00C258356EF59FDD7402C
    Session-ID-ctx: 
    Master-Key: BF1935A4B01B945E22F8C37AAB55564A44259DD66191F49580C3CDAF8B194517F3FA77782E2D3C9901369FB1615BFE07
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 300 (seconds)
    TLS session ticket:
    0000 - ba 97 fa fc 89 61 f1 00-1c a2 5f 5c be ed 58 87   .....a...._\..X.
    0010 - 76 e4 f3 94 36 c9 6c aa-9c 6e dd 8c 25 7f 03 03   v...6.l..n..%...
    0020 - c7 a1 6d cd 55 db 01 75-58 8b dc 9c b9 11 af 7b   ..m.U..uX......{
    0030 - ee 62 44 ae ab 7a 72 a1-17 7b dd 5a a0 02 bc d5   .bD..zr..{.Z....
    0040 - 80 ec 4c 14 55 21 c3 8c-a8 1b 6e b3 76 0b 67 5c   ..L.U!....n.v.g\
    0050 - 94 c0 fb 33 a9 e5 ea d2-2b ca a4 b6 cb 82 5a dc   ...3....+.....Z.
    0060 - 74 02 00 a9 c7 be eb 0a-d0 ff 68 f6 dc 8c 2f ba   t.........h.../.
    0070 - 05 f2 25 fd a8 f7 42 e9-ae 8f e2 7e 66 ea 01 26   ..%...B....~f..&
    0080 - 19 9e 7a b5 2c 42 79 0a-54 5f 86 e2 1b ca 7c 7d   ..z.,By.T_....|}
    0090 - e1 50 1a 4c 66 e0 f5 40-b8 70 41 8f 6a ae 11 3a   .P.Lf..@.pA.j..:
    00a0 - bb c0 5c 1a e7 ce 65 c2-0c 3a 37 c5 dd 34 e0 e3   ..\...e..:7..4..
    00b0 - 0c 82 cf fb 1f bf f0 2e-5a 2a cb b4 39 9e 64 b5   ........Z*..9.d.

    Start Time: 1641980220
    Timeout   : 7200 (sec)
    Verify return code: 21 (unable to verify the first certificate)
    Extended master secret: no
    QUIC: no
---
GET /

<!DOCTYPE html><html><head><meta http-equiv="refresh" content="0;url=/boc15/login.html"><meta name="renderer" content="ie-stand"></head><body></body></html>closed
$ 
···
