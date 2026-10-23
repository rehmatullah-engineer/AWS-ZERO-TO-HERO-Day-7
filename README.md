Amazon S3 — Buckets, Objects & Static Website Hosting
A concise, visual study guide for learning essential Amazon Simple Storage Service (Amazon S3) operations on AWS. This repository covers bucket creation, object uploads and deletion, bucket removal, static website hosting, permissions, and security best practices.
📌 Topics Covered
- S3 Buckets: Create buckets, select an AWS Region, and follow bucket naming rules.
- Objects & Object Keys: Upload files and folders, understand object keys, and remove objects.
- Bucket Deletion: Empty a bucket before deleting it.
- Static Website Hosting: Configure an index document and optional error document, then access the website endpoint.
- Permissions & Security: Understand IAM permissions, bucket policies, and Block Public Access.
- Best Practices: Versioning, lifecycle rules, least-privilege access, and meaningful bucket names.
🗂️ Repository Contents

🖼️ Visual Cheat Sheet

🚀 Quick Reference
1. Create an S3 Bucket
1. Open the Amazon S3 console.
2. Select Create bucket.
3. Enter a globally unique bucket name.
4. Choose the AWS Region.
5. Review the settings and create the bucket.
Bucket naming reminders: Names must be globally unique, 3–63 characters long, and follow S3 naming restrictions. Use lowercase letters and numbers where possible, with hyphens when needed. Avoid consecutive periods and names that start or end with a hyphen.
2. Upload and Delete Objects
1. Open the bucket.
2. Select Upload and add files or folders.
3. Review the files and upload.
4. To remove an object, select it and choose Delete.
An object key identifies an object within a bucket. For example, images/logo.png is a key that includes a prefix resembling a folder path.

Important: Deleting an object may create a delete marker in a versioned bucket. Permanently removing all versions requires additional care.
3. Delete a Bucket
1. Back up any data you need to keep.
2. Empty the bucket, including object versions and delete markers where applicable.
3. Open the bucket's actions menu and choose Delete.
4. Confirm the bucket name when prompted.
A bucket cannot be deleted while it still contains objects or versions.
4. Host a Static Website
1. Upload your static website files, such as index.html, CSS, JavaScript, and images.
2. Open the bucket's Properties tab.
3. Find Static website hosting and choose Edit.
4. Enable hosting and set the index document (for example, index.html).
5. Optionally set an error document (for example, error.html).
6. Save the changes and open the website endpoint shown by S3.
Security note: S3 website endpoints use HTTP, not HTTPS. For a public production website, consider Amazon CloudFront with an appropriate origin-access configuration and a custom domain. Configure public access deliberately; do not disable Block Public Access without understanding the exposure and access policy.
🔐 Permissions & Security
Common IAM actions include:
Action	Purpose
s3:CreateBucket	Create a bucket
s3:ListBucket	List objects in a bucket
s3:PutObject	Upload an object
s3:GetObject	Read an object
s3:DeleteObject	Delete an object
s3:DeleteBucket	Delete an empty bucket


Grant only the actions and resources required for the task. s3:ListAllMyBuckets is a separate permission used to list buckets across the account. A user may have access to a specific bucket without permission to list every bucket in the account.

For public static website access, the bucket policy and account-level or bucket-level Block Public Access settings must be considered together. Prefer CloudFront and private S3 access for production use when appropriate.
✅ Best Practices
- Enable S3 Versioning when recovery from accidental changes or deletions is important.
- Use Lifecycle rules to transition or expire objects according to retention needs.
- Apply least-privilege IAM policies.
- Keep bucket names meaningful and non-sensitive.
- Enable encryption and use appropriate access controls.
- Review public access settings before exposing files.
- Consider logging, monitoring, and cost controls for production workloads.
- Test website configuration and error handling before sharing the endpoint.
🎯 Learning Outcomes
After reviewing this guide, you should be able to explain what S3 buckets and objects are, perform common bucket and object operations, configure basic static website hosting, and identify the main IAM and security considerations.
📚 Official AWS Documentation
- Amazon S3 User Guide
- General purpose bucket naming rules
- Uploading objects
- Deleting objects
- Hosting a static website using Amazon S3
- Amazon S3 security best practices
Note: This repository is a learning reference. AWS console labels and service behavior may change. Check the official AWS documentation before applying changes to production resources.
