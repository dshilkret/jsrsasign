jsrsasign
=========

[![license](https://img.shields.io/badge/license-MIT-green.svg?style=flat)](https://github.com/kjur/jsrsasign/blob/master/LICENSE.txt)
[![bower](https://img.shields.io/bower/v/jsrsasign.svg?maxAge=2592000)](https://libraries.io/bower/jsrsasign)
[![npm version](https://badge.fury.io/js/jsrsasign.svg)](https://badge.fury.io/js/jsrsasign)
[![npm downloads](https://img.shields.io/npm/dm/jsrsasign.svg)](https://www.npmjs.com/package/jsrsasign)
[![CDNJS](https://img.shields.io/cdnjs/v/jsrsasign.svg)](https://cdnjs.com/libraries/jsrsasign)
[![githubsponsors](https://img.shields.io/badge/github-donate-yellow.svg)](https://github.com/sponsors/kjur)
[![cryptocurrency](https://img.shields.io/badge/crypto-donate-yellow.svg)](https://github.com/kjur/jsrsasign#cryptocurrency)

The 'jsrsasign' (RSA-Sign JavaScript Library) is an opensource free cryptography library supporting RSA/RSAPSS/ECDSA/DSA signing/validation, ASN.1, PKCS#1/5/8 private/public key, X.509 certificate, CRL, OCSP, CMS SignedData, TimeStamp, CAdES JSON Web Signature/Token/Key in pure JavaScript.

Public page is https://kjur.github.io/jsrsasign .

Your bugfix and pull request contribution are always welcomed :)

HIGHLIGHTS
----------
- Swiss Army Knife style all in one package crypto and PKI library
- available on Node and browsers
- very easy API to use
- powerful various format key loader and ASN.1 API
- rich document and samples
- no dependency to other library
- no dependency to W3C Web Crypto API nor OpenSSL
- very popular crypto library with 6M+ npm downloads/month

INSTALL
-------
### Node NPM
    > npm install jsrsasign jsrsasign-util
### Bower
    > bower install jsrsasign
### Or include in HTML from many CDN sites
    > <script src="https://cdnjs.cloudflare.com/ajax/libs/jsrsasign/8.0.20/jsrsasign-all-min.js"></script>

USAGE
-----

Loading encrypted PKCS#5 private key:

    > var rs = require('jsrsasign');
    > var rsu = require('jsrsasign-util');
    > var pem = rsu.readFile('z1.prv.p5e.pem');
    > var prvKey = rs.KEYUTIL.getKey(pem, 'passwd');

Sign string 'aaa' with the loaded private key:

    > var sig = new a.Signature({alg: 'SHA1withRSA'});
    > sig.init(prvKey);
    > sig.updateString('aaa');
    > var sigVal = sig.sign();
    > sigVal
    'd764dcacb...'

MORE TUTORIALS AND SAMPLES
--------------------------
- [Tutorials in GitHub Wiki](https://github.com/kjur/jsrsasign/wiki)
- [Sample Node Scripts](https://github.com/kjur/jsrsasign/tree/master/sample_node)

## RECENT SECURITY ADVISORY

|published|fixed version|title/advisory|CVE|CVSS|
|:---|:---|:---|:---|:---|
|2020Jun22|8.0.19|[ECDSA signature validation vulnerability by accepting wrong ASN.1 encoding](https://github.com/kjur/jsrsasign/security/advisories/GHSA-p8c3-7rj8-q963)|CVE-2020-14966|5.5|
|2020Jun22|8.0.18|[RSA RSAES-PKCS1-v1_5 and RSA-OAEP decryption vulnerability with prepending zeros](https://github.com/kjur/jsrsasign/security/advisories/GHSA-xxxq-chmp-67g4)|CVE-2020-14967|4.8|
|2020Jun22|8.0.17|[RSA-PSS signature validation vulnerability by prepending zeros](https://github.com/kjur/jsrsasign/security/advisories/GHSA-q3gh-5r98-j4h3)|CVE-2020-14968|4.2|

Here is [full published security advisory list](https://github.com/kjur/jsrsasign/security/advisories?state=published).

## DONATIONS

If you like jsrsasign and my other project, you can support their development by donation through any of the platform/services below. Thank you as always.

### Github Sponsors
You can sponsor jsrsasign with the [GitHub Sponsors](https://github.com/sponsors/kjur) program.

### Cryptocurrency
You can donate cryptocurrency to jsrsasign using the following addresses:
- Bitcoin(BTC): [34vSRe7XHoMy78HKgps9YJ5BrBLYJLeM22](https://en.cryptobadges.io/donate/34vSRe7XHoMy78HKgps9YJ5BrBLYJLeM22)
- Ethereum(ETH): [0x9c4cdbb531e5b84796ff5f91a9f652704761e64e](https://en.cryptobadges.io/donate/0x9c4cdbb531e5b84796ff5f91a9f652704761e64e)
- Litecoin(LTC): [LPf3VDJVamwPcNJNjjVtrUQuJQ17ZyWzeU](https://en.cryptobadges.io/donate/LPf3VDJVamwPcNJNjjVtrUQuJQ17ZyWzeU)
- Bitcoin Cash(BCH): bitcoincash:pq3hy08pc9vm57q6ddgsc06cqdffmfzwwqxd9yejyf
