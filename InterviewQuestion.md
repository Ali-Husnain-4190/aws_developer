How to encrypt  volume if not encrypt
    you have to create a snapshot and you can make it encrypt

How to move volume one az to other
    After stop instance you can create a snapshot then create volume and select different az.
    
    If you want to move EBS to other region you have copy and create volume then attach to EC2


NOTE :
    restart instance do not remove the mount volume in instance host.
    But if you stop and start again instance then instance move to different host. so will loss data



Question come up in exam?
Can we get orignal IP if we remove elastic IP ?
    if your instance have public IP and you remove it and attach to elastic IP. Then reomve it you will not get previous (orignal)public IP
