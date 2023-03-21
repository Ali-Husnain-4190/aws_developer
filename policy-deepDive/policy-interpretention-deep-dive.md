
```

{
    "Version": "2012-10-17",
    "Statement": 
    [
      {
        "Effect":"Allow",
        "Action":[
           "s3:PutObject",
           "s3:PutObjectAcl",
           "s3:GetObject",
           "s3:GetObjectAcl",
           "s3:DeleteObject"
        ],
        "Resource":"arn:aws:s3:::holidaygifts/*"
      },
      {
        "Effect": "Deny",
        "Action": [
          "s3:GetObject",
          "s3:GetObjectAcl"
        ],
        "Resource":"arn:aws:s3:::holidaygifts/*",
        "Condition": {
            "DateGreaterThan": {"aws:CurrentTime": "2022-12-01T00:00:00Z"},
            "DateLessThan": {"aws:CurrentTime": "2022-12-25T06:00:00Z"}
        }
      }
    ]
}

```



# Deny policy
Not fully understand

<!-- ```

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "DenyNonApprovedRegions",
            "Effect": "Deny",
            "NotAction": [
                "cloudfront:*",
                "iam:*",
                "route53:*",
                "support:*"
            ],
            "Resource": "*",
            "Condition": {
                "StringNotEquals": {
                    "aws:RequestedRegion": [
                        "ap-southeast-2",
                        "eu-west-1"
                    ]
                }
            }
        }
    ]
}
```
In above NotAction section mean is deny everything but allow the thing which is in define in NotAction block.

StringNotEqual only be true for those region is not in list -->
