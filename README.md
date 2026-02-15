# Static-Resume-Website-using-Amazon-S3-CloudFront-AWS-
The goal was to understand static website hosting, CDN integration, security, and cost control using AWS Free Tier–friendly services.

Project Overview

This project demonstrates how to host a static resume (CV) website on AWS using Amazon S3 for storage and Amazon CloudFront as a Content Delivery Network (CDN).
The goal was to understand static website hosting, CDN integration, security, and cost control using AWS Free Tier–friendly services.

Objectives:

Host a static website using Amazon S3
Distribute content globally using CloudFront
Improve website performance and availability
Understand AWS security controls and access management
Ensure zero unexpected billing by proper cleanup

Architecture Used:
     User Browser
          ↓
     Amazon CloudFront (CDN)
          ↓
     Amazon S3 (Static Website Hosting)


AWS Services Used:

Amazon S3
Static website hosting
Object storage for HTML/CSS files
Amazon CloudFront
Global CDN for faster content delivery
HTTPS support
AWS IAM
Managed access permissions automatically via CloudFront



Implementation Steps:-
 S3 Bucket Setup

Created an S3 bucket with a globally unique name
Uploaded static website files (index.html)
Enabled Static Website Hosting
Configured:
      Index document: index.html
      Error handling (default)

CloudFront Distribution:-

Created a CloudFront distribution
Selected Amazon S3 as origin
Granted CloudFront permission to access the S3 bucket
Used recommended cache and origin settings
Set Default Root Object to index.html
Deployed distribution successfully




Security Configuration:-

Used CloudFront’s built-in security protections
Did not expose S3 bucket publicly
CloudFront accessed S3 using restricted permissions
No custom domain or SSL certificate used (Free plan)


Testing:

Verified website accessibility using:

https://<cloudfront-distribution-domain>
   Confirmed content delivery through CloudFront



Key Learnings

Difference between S3 static hosting endpoint and S3 REST endpoint
How CloudFront securely accesses private S3 buckets
Importance of Default Root Object in CloudFront
CloudFront pricing plan behavior and deletion constraints
Safe cleanup practices to avoid billing
