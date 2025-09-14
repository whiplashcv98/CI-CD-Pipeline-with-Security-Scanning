# CI-CD-Pipeline-with-Security-Scanning
This project demonstrates the integration of security scanning into a CI/CD pipeline using AWS services and the Trend Micro Cloud One - Conformity Template Scanner. The goal is to enforce security best practices by scanning infrastructure-as-code (IaC) templates before deployment.

# Introduction
CI/CD pipelines are crucial for automating and securing software delivery. This project highlights how to enhance this process by incorporating the Cloud One - Conformity Template Scanner, which automatically identifies security and compliance issues in CloudFormation templates.

# Prerequisites
To follow this guide, you will need the following:

1.VSCode IDE
2.Trend Micro Cloud One—Conformity Plugin
3.An AWS account

# Set-up and Configuration
Creating the CI/CD Pipeline
The pipeline is built using several AWS services:

CodeCommit: The repository where the initial CloudFormation templates and application code are committed.

CodeBuild: A build project is set up to build the CloudFormation template and run the security scan.

CodePipeline: This service orchestrates the entire workflow, integrating the source repository (CodeCommit), the build process (CodeBuild), and the security scanner.

# Integration with Cloud One – Conformity Template Scanner
The template scanner is integrated into the CodeBuild stage of the pipeline. It scans the CloudFormation template for potential security and compliance issues.

# Pipeline Execution and Results
Running the Pipeline
The pipeline is automatically triggered when a new commit is made to the CodeCommit repository.

# Analyzing Results
After the pipeline runs, the results of the security scan are available. The Conformity Template Scanner generates a JSON report that details all identified issues, which can be reviewed to understand and prioritize fixes.

# Fixing Issues and Re-deployment
Updating CloudFormation Template
To fix the issues, you update the CloudFormation template in your local environment based on the scanner's findings.

# Re-running the Pipeline
Once the fixes are committed to CodeCommit, the pipeline automatically runs again. The goal is to see a successful pipeline execution, confirming that all security issues have been resolved.
