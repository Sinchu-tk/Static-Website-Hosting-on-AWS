# Static Website Hosting on AWS

This guide demonstrates how to host a static website using Amazon S3 and CloudFront without the DNS setup. 

## Prerequisites
- AWS Account
- Static website files (HTML, CSS, JavaScript, etc.)

## Steps to Set Up Static Website Hosting

### 1. Create an S3 Bucket
- Navigate to **Amazon S3** in the AWS Management Console.
- Create a new bucket with a globally unique name.
- Enable **Static Website Hosting** in the bucket properties.

### 2. Upload Website Files
- Upload your website's static files to the S3 bucket (HTML, CSS, JavaScript).

### 3. Set Bucket Policy
- Set the bucket policy to allow public access to the files. The policy should allow `s3:GetObject` for all files in the bucket.
- Example policy:
  ```json
  {
      "Version": "2012-10-17",
      "Statement": [
          {
              "Sid": "AllowPublicRead",
              "Effect": "Allow",
              "Principal": "*",
              "Action": "s3:GetObject",
              "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
          }
      ]
  }
