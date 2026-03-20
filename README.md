# aws-s3-pipeline
<img width="327" height="364" alt="Screenshot 2026-03-20 100017" src="https://github.com/user-attachments/assets/e6019f9f-11bf-48a7-8f26-42e00feeae8f" />

# AWS CI/CD Pipeline: Static Website Deployment

This project demonstrates a fully automated Continuous Integration and Continuous Deployment (CI/CD) pipeline for a static website hosted on Amazon S3.

## 📐 Architecture
1. **Source:** Code is stored in an **AWS CodeCommit** repository.
2. **Deploy:** **AWS CodePipeline** triggers on every commit.
3. **Host:** The files are deployed to an **Amazon S3** bucket configured for Static Website Hosting.

## 🚀 Learning Objectives
* Configuring AWS CodeCommit for version control.
* Setting up an S3 bucket with public-read permissions via Bucket Policies.
* Architecting a pipeline that automates the transition from code to live production.

## 🛠️ How to Replicate
1. **S3 Setup:** Create a bucket, enable "Static website hosting," and disable "Block all public access." 
2. **Permissions:** Apply a bucket policy to allow `s3:GetObject` for all users.
3. **Repository:** Push your `index.html` and assets to CodeCommit.
4. **Pipeline:** Create a new pipeline in AWS CodePipeline, selecting CodeCommit as the provider and S3 as the deployment provider.

## 📄 Files Included
* `index.html` - The main website landing page.
* `images/` - Site assets.
