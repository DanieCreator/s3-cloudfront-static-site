# Secure Static Website Hosting with Amazon S3 + CloudFront
## Overview

This project demonstrates how to host a static website on AWS using a secure and production-oriented approach.

Instead of exposing the S3 bucket publicly, the architecture ensures that all access is routed through CloudFront, improving both security and performance.

## Architecture

User → CloudFront (CDN) → S3 (Private Bucket)

## Key Design Decisions
- I kept the S3 bucket private to prevent direct public access
- I used CloudFront as the only entry point for users
- I implemented Origin Access Control (OAC) to securely connect CloudFront to S3
- I enabled HTTPS by default through CloudFront
## What This Solves
- Prevents unauthorized access to S3 objects
- Improves global performance through caching
- Reduces latency for users in different regions
## Testing
- Direct S3 access returns Access Denied
- CloudFront URL successfully serves the website
## Future Improvements
- Add CI/CD pipeline for automatic deployments
- Configure a custom domain with SSL (ACM)
- Enable logging and monitoring (CloudWatch, S3 logs)
## Lessons Learned

This project helped me understand how to design secure cloud architectures by separating storage from public access and using managed services effectively.
