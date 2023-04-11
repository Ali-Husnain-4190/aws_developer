# Ec2 meta data
    1) Ec2 service which provide information about Ec2 instance
    2) http://169.252.169.254

`curl http://169.254.169.254/latest/meta-data/public-ipv4
curl http://169.254.169.254/latest/meta-data/public-hostname

wget http://s3.amazonaws.com/ec2metadata/ec2-metadata
chmod u+x ec2-metadata

ec2-metadata --help
ec2-metadata -a
ec2-metadata -z
ec2-metadata -s
`
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instancedata-data-retrieval.html

https://aws.amazon.com/developer/

`ipconfig` give you information about instance IPs