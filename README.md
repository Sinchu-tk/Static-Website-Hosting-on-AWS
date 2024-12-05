# Static Website Hosting on AWS

This project demonstrates how to host a static website using Amazon S3 and CloudFront.

## Prerequisites

- AWS Account
- Domain name (external provider)

## Steps to Set Up Static Website Hosting

1. **Create an S3 bucket for hosting**:
   - Create a unique bucket name.
   - Enable static website hosting.

2. **Upload your website files**:
   - Upload HTML, CSS, and image files to S3.

3. **Set permissions**:
   - Add a bucket policy to allow public read access to your files.

4. **Create CloudFront distribution**:
   - Use CloudFront to serve your website efficiently.

5. **Configure DNS**:
   - Update DNS settings with a CNAME record pointing to CloudFront.
