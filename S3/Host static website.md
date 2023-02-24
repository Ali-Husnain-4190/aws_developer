# Static website hosting
    Normal access via API
    This feature allow access via HTTP
    index and Error are documents are set
    We can also creat website endpoint
    We can also set custom domain  Via R53


You never charg to transfer data into S3. It always free.

# S3 pricing detail
https://aws.amazon.com/s3/pricing/


Host static website


## Step 1
    Create a bucket and make it public
## Step 2
    Go to Properties tab and Scroll down at the end and enable static website host.
    For hosting type select : Host static website. And provide inex.html and error.html file. and Save it
## Step 3 
    After save file scrol down and copy the url in notebook. 
## step 4 copy index and error.html file to your object. If you have images upload that folder aswell and click on upload

## Step 5 paste your copied url in browser you will get error Access denied . The error is because you are not able to access bucket file in publicaly for that you have to attach policy to bucket.
## Step 6 Go to  permession tab, Click on bucket policy. Replace Resource with your bucket name.

``` 
{
    "Version":"2012-10-17",
    "Statement":[
      {
        "Sid":"PublicRead",
        "Effect":"Allow",
        "Principal": "*",
        "Action":["s3:GetObject"],
        "Resource":["arn:aws:s3:::examplebucket/*"]
      }
    ]
  }
```

# Step 7
    Go back to your browser and past copied URL again.But add index.html at end of url like below. you will get you data

    http://alihusnain-cat.s3-website-us-east-1.amazonaws.com/index.html