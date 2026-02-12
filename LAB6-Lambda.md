# 🖼️ AWS Lambda Thumbnail Generator (S3 Trigger)

## 📌 Overview

This project demonstrates how to build a **serverless image processing workflow** using:

- Amazon S3  
- AWS Lambda  
- IAM Role  

When a user uploads an image to an S3 bucket, Lambda is automatically triggered to create a thumbnail and store it in another bucket.

---

## 🧭 Workflow Diagram

<img width="674" height="452" alt="Workflow Diagram" src="https://github.com/user-attachments/assets/d4b5fc65-ef27-4353-a2a6-9e1f586d6d72" />

---

## 🔄 Architecture Flow

1. A user uploads an object to the **source S3 bucket** (ObjectCreated event).  
2. Amazon S3 detects the event.  
3. S3 invokes the AWS Lambda function and passes event data.  
4. Lambda executes the function.  
5. The function:
   - Reads the source bucket name and object key.
   - Downloads the image.
   - Creates a thumbnail.
   - Uploads the resized image to the target bucket.

---

# 🪣 Task 1: Create the Amazon S3 Buckets

## 1️⃣ Create Source Bucket

<img width="1919" height="232" alt="Create Bucket" src="https://github.com/user-attachments/assets/bce58628-b428-4aca-99fc-b4321ee458fe" />

<img width="1919" height="651" alt="Source Bucket Setup" src="https://github.com/user-attachments/assets/fd35a3bb-5786-4749-80f9-c2487db36188" />

<img width="1919" height="185" alt="Bucket Confirmation" src="https://github.com/user-attachments/assets/4150e109-67da-4bbf-a25f-1a63b9874d91" />

---

## 2️⃣ Create Target Bucket (For Thumbnails)

<img width="1919" height="700" alt="Create Thumbnail Bucket" src="https://github.com/user-attachments/assets/f2165a60-9fb6-4472-8584-f10b21c32f66" />

<img width="1919" height="667" alt="Thumbnail Bucket Setup" src="https://github.com/user-attachments/assets/7eb528ea-6138-4acf-bb60-43e7e4a8fc5e" />

---

## 3️⃣ Upload an Image to Source Bucket

<img width="1919" height="552" alt="Upload Image" src="https://github.com/user-attachments/assets/7366b7bf-e27a-467b-9827-ec7b3c3fdd38" />

---

# ⚡ Task 2: Create AWS Lambda Function

<img width="1919" height="231" alt="Create Lambda" src="https://github.com/user-attachments/assets/82b3313e-fafc-4f97-9de0-d3c58a2c9294" />

<img width="1918" height="863" alt="Lambda Setup" src="https://github.com/user-attachments/assets/2ddcafd0-a3ec-49fd-a4e3-384872b6803b" />

---

## 🔐 IAM Role

<img width="1896" height="384" alt="IAM Role" src="https://github.com/user-attachments/assets/adadfb16-1a89-4dfd-b70f-89fba03b3941" />

**Note:**  
This role grants permission to the Lambda function to:

- Read objects from the source bucket  
- Write objects to the target bucket
  
## 🌐 VPC Configuration

Specify the VPC and subnet (if required by your lab environment):
<img width="1919" height="786" alt="Role Permissions" src="https://github.com/user-attachments/assets/898d60ef-759a-445b-a4c2-1bfb42102962" />
---

## 🔔 Lambda Trigger
<img width="1919" height="530" alt="VPC Setup" src="https://github.com/user-attachments/assets/6c1301b3-0379-40c3-8b51-7c11ad002583" />

<img width="1919" height="890" alt="Lambda Trigger" src="https://github.com/user-attachments/assets/802ccd88-0003-4bbb-b107-867fa3e01511" />

<img width="1919" height="893" alt="Trigger Confirmation" src="https://github.com/user-attachments/assets/f63881b7-fe9c-4a74-88b9-eafccd3ebe71" />

<img width="1919" height="878" alt="Trigger Details" src="https://github.com/user-attachments/assets/5976367b-e15c-45ff-ab52-0b0f8572a344" />

<img width="1919" height="649" alt="Trigger Review" src="https://github.com/user-attachments/assets/ed19d117-e5b0-472f-89be-c52c04361118" />

---

# 🧪 Task 3: Test the Function

<img width="1903" height="876" alt="Create Test Event" src="https://github.com/user-attachments/assets/e52b1cd1-5d89-4cc4-8e53-d25ca7b1fc12" />

<img width="1919" height="889" alt="Test Event JSON" src="https://github.com/user-attachments/assets/0b892b35-e927-48e0-af9e-50607a9d4f48" />

<img width="1578" height="618" alt="Test Execution Result" src="https://github.com/user-attachments/assets/19e775ac-ed27-4a59-97af-a25c535ed193" />

---

# ✅ Expected Result

- Uploading an image to the source bucket triggers Lambda.  
- A resized thumbnail is automatically created.  
- The thumbnail is stored in the target bucket.  

---

# 🏗️ Technologies Used

- Amazon S3  
- AWS Lambda  
- IAM  
- Event-Driven Architecture  
- Python (Boto3 + Pillow)  
