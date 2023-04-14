# Route 53 CNAME VS Alias
- "A" map name to IP address like cate.io to 12345
- CNAME map a name to another NAME like cate.io to cate.io
- CNAME is not valid for 1 `naked/apex` (categram.io)
- Many AWS services use DNS name (ELBs)
- with CNAME - categram.io => ELBs will be invalid
NOTE:
    ANything which is not naked domain where you point name to another name then `CNAME` record fine.


# Alias
    - ALIAS record map `NAME` to AWS resources
    - It can be use for both naken/apex and normal record.
    - There is not charges for request pointing at AWS resources
    - For AWS services default to pick ALIAS
    - such as API Gateway, S3, Elastic Beantalk, ELB, Global accelrator
    
