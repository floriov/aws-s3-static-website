# AWS S3 Static Website Hosting

## Project Overview
I created this project to demonstrate how to host a static website using Amazon S3. It includes setting up an S3 bucket, enabling static website hosting, and configuring permissions to make the site publicly accessible. The link to the website can be found [here](http://nextwork-website-project-vanessa.s3-website.eu-west-2.amazonaws.com/).

## Objective
My goal was to deploy a static website using AWS S3, leveraging its cost-effectiveness, scalability, and reliability.

## Technologies I Used
- **Amazon S3:** For static website hosting.
- **AWS Management Console:** For bucket management and configuration.
- **AWS IAM:** To set permissions and access control.
- **HTML, CSS, JavaScript:** For developing the website content.
- **VS Code:** My preferred text editor for development.

## Implementation Steps

### 1. Creating an S3 Bucket
1. I logged in to the AWS Management Console and navigated to the S3 service.
2. I clicked **Create bucket**, entered a unique bucket name (`nextwork-website-project-vanessa`), selected `eu-west-2` as the region, and created the bucket.

### 2. Enabling Static Website Hosting
1. I selected my bucket and went to the **Properties** tab.
2. Under **Static website hosting**, I clicked **Edit**, enabled it, and set `index.html` as the index document.

### 3. Uploading Website Files
1. I navigated to the **Objects** tab and clicked **Upload**.
2. I uploaded my website files, including `index.html` and other assets like CSS and JavaScript files.

### 4. Configuring Bucket Permissions
1. I went to the **Permissions** tab and added a **Bucket Policy** to allow public read access:
    ```json
    {
      "Version": "2012-10-17",
      "Statement": [
        {
          "Sid": "PublicReadGetObject",
          "Effect": "Allow",
          "Principal": "*",
          "Action": "s3:GetObject",
          "Resource": "arn:aws:s3:::nextwork-website-project-vanessa/*"
        }
      ]
    }
    ```
2. I saved the policy to make my files publicly accessible.

### 5. Testing the Website
1. I copied the **Bucket website endpoint URL** from the **Properties** tab.
2. I opened the URL in my browser to view the hosted website and ensure everything was working correctly.

## Outcome
I successfully hosted my static website on AWS S3. It’s now accessible via the S3 bucket URL, showcasing a scalable and cost-effective web hosting solution.

## Repository Information
**Repository Name:** `aws-s3-static-website`  
**Description:** "This project demonstrates how I hosted a static website using AWS S3."
