# Secure Deployment Guardian

A DevSecOps project demonstrating how to automate security checks and container validation before deployment using GitHub Actions, Docker, GitLeaks, and Trivy.

## Project Overview

Secure Deployment Guardian helps prevent insecure code from reaching production by automatically validating every code change pushed to GitHub.

The CI pipeline performs:

* Secret scanning using GitLeaks
* Application validation
* Docker image build
* Container vulnerability scanning using Trivy

This project demonstrates a practical DevSecOps workflow used in modern software delivery pipelines.

---

## Architecture

Developer
↓
Git Push
↓
GitHub Actions CI Pipeline
↓
GitLeaks Secret Scan
↓
Python/FastAPI Validation
↓
Docker Image Build
↓
Trivy Vulnerability Scan
↓
Ready for Deployment

---

## Technologies Used

* Python 3.12
* FastAPI
* Docker
* GitHub Actions
* GitLeaks
* Trivy
* Git
* Linux

---

## CI/CD Workflow

Whenever code is pushed to the main branch:

### Step 1: Source Code Checkout

The latest code is pulled into the GitHub Actions runner.

### Step 2: Secret Detection

GitLeaks scans the repository for:

* API Keys
* AWS Credentials
* Passwords
* Tokens
* Hardcoded Secrets

### Step 3: Application Validation

The FastAPI application is imported and validated to ensure there are no startup errors.

### Step 4: Docker Image Build

A Docker image is built from the application's Dockerfile.

### Step 5: Vulnerability Scanning

Trivy scans the Docker image for:

* Critical vulnerabilities
* High severity vulnerabilities
* Insecure packages
* Known CVEs

---

## Security Benefits

* Prevents accidental credential leaks
* Detects vulnerabilities before deployment
* Ensures application startup validation
* Automates security checks in CI/CD
* Improves software supply chain security

---

## Results

✅ Automated CI/CD pipeline

✅ Secret detection with GitLeaks

✅ Docker image validation

✅ Vulnerability scanning with Trivy

✅ GitHub Actions integration

---

## Learning Outcomes

Through this project I learned:

* Git and GitHub workflows
* GitHub Actions CI/CD pipelines
* Docker containerization
* DevSecOps fundamentals
* Secret scanning techniques
* Container security scanning
* Automated software validation

---

## Future Enhancements

* Infrastructure as Code using Terraform
* AWS Deployment Automation
* Kubernetes Deployment
* Prometheus Monitoring
* Grafana Dashboards
* SonarQube Code Quality Analysis

---

## Author

Yashvi Shah
