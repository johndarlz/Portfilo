# 🌐 AWS S3 Website Deployment with GitHub Actions

This project is a **simple static website** (HTML) that is **automatically deployed to AWS S3** using **GitHub Actions**. Every time you push code to the `main` branch, the site is uploaded to the S3 bucket and updated live!

---

## 🚀 Project Overview

- ✅ Basic HTML website (`index.html`)
- ✅ Code stored and managed in GitHub
- ✅ Deployed automatically to AWS S3 via GitHub Actions
- ✅ Publicly accessible as a static website

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **HTML** | To build the static web page (`index.html`) |
| **GitHub** | To host and manage code repository |
| **GitHub Actions** | For CI/CD pipeline to deploy website automatically |
| **AWS S3** | To host the static website |
| **AWS IAM** | For secure access to AWS services via programmatic credentials |
| **YAML** | Used for GitHub Actions workflow configuration |
| **Markdown** | For creating project documentation (`README.md`) |

---
---

## ⚙️ How It Works

### 🔁 1. GitHub Repository
- The website code is pushed to a GitHub repo (like this one).

### ⚡ 2. GitHub Actions Workflow
- A workflow file in `.github/workflows/deploy.yml` listens for pushes to `main`.
- When triggered, it uploads all files in the repo to your specified S3 bucket.

### ☁️ 3. AWS S3 Static Website Hosting
- The S3 bucket is configured for static website hosting.
- A bucket policy allows public access to the files.

---

## 🔐 GitHub Secrets Required

In your GitHub repo, go to **Settings → Secrets → Actions**, and add:

| Name | Description |
|------|-------------|
| `AWS_ACCESS_KEY_ID` | Your AWS IAM user's access key |
| `AWS_SECRET_ACCESS_KEY` | Your AWS IAM user's secret key |
| `AWS_REGION` | Your AWS region (e.g., `us-east-1`) |
| `S3_BUCKET_NAME` | The name of your S3 bucket |

---

## 🛠️ Setup Instructions (For Your Reference)

### 1. Create AWS S3 Bucket
- Enable static website hosting
- Set index document: `index.html`
- Make the bucket public with a bucket policy

### 2. Create AWS IAM User
- Allow `AmazonS3FullAccess` permission
- Save access key & secret key

### 3. Add GitHub Secrets
- Go to GitHub → Settings → Secrets → Actions → Add the keys listed above

### 4. Create Workflow
- Add `.github/workflows/deploy.yml` with the deployment script


### 5. Push Your Code



🌐 http://john-portfilo.s3-website.ap-south-1.amazonaws.com/

🙋‍♂️ Author
Kandukuri Jnaneswar(johndarlz)
Email: johnu.kandukuri@gmail.com
GitHub: @johndarlz


This project is licensed under the MIT License.
