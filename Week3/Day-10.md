
# Day 10 — Amazon S3 and Static Website Hosting

**Training Date:** 13 July 2026

## 1. Overview

Day 10 focused on Amazon Simple Storage Service (Amazon S3), an AWS cloud storage service used to store and manage files and other data as objects. The session covered S3 buckets, file management, access permissions, object versioning, and the deployment of a simple static website using HTML and image files.

## 2. Topics Covered

### 2.1 Introduction to Amazon S3

Amazon S3 (Simple Storage Service) is an object storage service provided by Amazon Web Services (AWS). It allows users to store, retrieve, and manage data in the cloud.

Key concepts learned:

- **Object Storage:** S3 stores data as objects, which consist of the data, a key (name), and metadata.
- **Buckets:** Buckets are containers used to organize and store objects in S3.
- **AWS Regions:** S3 buckets are created in a selected AWS Region, allowing users to choose where their data is stored.
- **Scalability:** S3 can store and manage large amounts of data without requiring users to maintain physical storage infrastructure.

### 2.2 Creating and Managing an S3 Bucket

An S3 bucket was created to explore cloud storage and file management.

The following operations were practiced:

- Creating an S3 bucket.
- Uploading files and folders.
- Organizing stored objects.
- Deleting files and folders when they were no longer required.
- Exploring the bucket interface and its available management options.

### 2.3 Bucket Permissions and Access Control

The session explored how permissions determine who can access S3 buckets and their objects.

The following features were studied:

- **Block Public Access:** A set of settings designed to prevent unintended public access to S3 resources.
- **Bucket Policies:** Resource-based policies that define which actions are allowed or denied for specified users or other principals.
- **Public Access:** Understanding how objects can be made publicly accessible when a use case requires it.
- **Tags:** Key-value pairs used to categorize AWS resources for identification, organization, and management.

Public access should only be enabled when necessary. Bucket policies and public access settings must be configured carefully to avoid exposing sensitive information.

### 2.4 Object Versioning

Object versioning was explored as a way to preserve multiple versions of an object in an S3 bucket.

Key learnings:

- Versioning helps maintain previous versions of files.
- When an object is updated, S3 can retain its earlier versions.
- When an object is deleted in a versioned bucket, a delete marker is generally added instead of immediately removing all previous versions.
- Previous versions can be recovered when required, subject to permissions and version-management settings.

Object versioning is useful for recovering from accidental modifications or deletions and maintaining a history of stored files.

### 2.5 Exploring Bucket Properties and Permissions

The Permissions and Properties sections of the S3 bucket were explored.

- **Permissions:** Used to review access controls, public access settings, and bucket policies.
- **Properties:** Used to explore bucket configuration and features such as versioning and static website hosting.

These sections help administrators understand and manage the behavior, accessibility, and configuration of an S3 bucket.

## 3. Practical Implementation

### 3.1 File and Folder Management

An S3 bucket was created, and files and folders were uploaded, organized, and deleted to understand how objects are managed in cloud storage.

### 3.2 Exploring Access Settings

The bucket's permissions were explored, including Block Public Access, bucket policies, tags, and the configuration required for public access when needed.

### 3.3 Testing Object Versioning

Object versioning was explored to understand how previous versions of files can be retained and recovered after changes or deletions.

### 3.4 Deploying a Static Website Using Amazon S3

A simple static website was deployed using an `index.html` file and images stored in an S3 bucket.

The deployment involved:

1. Preparing the website's HTML file and image assets.
2. Uploading the files to the S3 bucket.
3. Exploring the bucket's static website hosting settings.
4. Reviewing the permissions and configuration needed to make the website accessible.
5. Understanding how S3 can serve static website content without requiring a traditional web server.

Static website hosting is suitable for websites made of files such as HTML, CSS, JavaScript, and images. It does not directly execute server-side application code.

## 4. Key Learnings

- Understood Amazon S3 and its role in AWS cloud storage.
- Learned how buckets and objects are used to organize stored data.
- Practiced uploading, organizing, and deleting files and folders.
- Explored Block Public Access, bucket policies, tags, and object permissions.
- Understood how object versioning helps recover earlier versions of files.
- Explored the Permissions and Properties sections of an S3 bucket.
- Deployed a simple static website using an HTML file and images.

## 5. Learning Outcome

The session provided practical exposure to Amazon S3 for cloud-based file storage, access management, version control of stored objects, and static website hosting. It strengthened the understanding of how AWS storage services can be used to store website assets and publish static web content.

---

[⬅️ Back to Week 3](README.md) | [⬅️ Back to Main Training Diary](../README.md)
