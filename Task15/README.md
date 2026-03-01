# Task 15: CloudFront Distribution for S3 Static Website

## Objective
To understand global content distribution and CDN (Content Delivery Network) capabilities by deploying Amazon CloudFront in front of an existing S3 static website.

## Implementation Steps

### 1. Origin Configuration
- Navigated to the Amazon CloudFront console and initiated a new distribution creation.
- Selected the existing Amazon S3 bucket (provisioned in Task 5) as the Origin Domain.

### 2. Cache and Security Behavior
- Configured the Viewer Protocol Policy to 'Redirect HTTP to HTTPS' to enforce secure, encrypted connections for all users.
- Explicitly bypassed the Web Application Firewall (WAF) enablement to maintain a cost-effective, standard tier deployment.

### 3. Edge Routing
- Defined `index.html` as the Default Root Object so the CloudFront edge locations automatically serve the correct homepage when the base domain is queried.
- Successfully deployed the distribution across AWS Edge Locations.

### 4. Verification
- Retrieved the generated CloudFront Distribution Domain Name (e.g., `dXXXXX.cloudfront.net`).
- Verified that accessing the CloudFront URL successfully loads the website with lower latency and valid HTTPS encryption, rather than accessing the S3 endpoint directly.

## Proofs of Completion
- cloudfront_dashboard.png: Screenshot of the AWS CloudFront console showing the distribution successfully deployed and enabled.
- cloudfront_website.png: Screenshot of the web browser displaying the static website successfully loading via the secure CloudFront edge URL.