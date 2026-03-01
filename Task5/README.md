# Task 5: Static Website Hosting in S3

## Objective
To learn serverless hosting using S3 by deploying a static website using an Amazon S3 bucket.

## Implementation Steps
1. Bucket Creation: Created an Amazon S3 bucket and disabled the "Block all public access" setting to allow web traffic.
2. Website Configuration: Enabled the "Static website hosting" feature in the bucket properties and specified `index.html` as the default index document.
3. Access Management: Applied a Bucket Policy to grant `s3:GetObject` permissions to all public principals (`*`), ensuring the website files are publicly readable.
4. Deployment: Uploaded the `index.html` file to the bucket and successfully accessed the live website via the S3-provided endpoint URL.

## Proofs
- s3_hosting_enabled.png: AWS console screenshot showing the bucket properties with Static Website Hosting successfully enabled and the endpoint generated.
- website_output.png: Browser screenshot showing the live HTML website loaded via the S3 endpoint URL.
