# Cloud HSM
    1) with KMS ... AWS managed service  and shared but seperate. They managed hardware and software then provide to you.
    2) Cloud HSM is single Tenant " hardware security module.
    3) AWS provisioned .... and customer manage. if you lost key so it is not easy to recover you have to provision again.
    4) cloud HSM is FIPS 140-2 level-3 (KMS is L2 Overall, some L3)
    5) You can use cloud HSM by API, PKCS #11 , java cryptography, Extentions(JCE), Microsfot Crypto NG (CNG) libraries