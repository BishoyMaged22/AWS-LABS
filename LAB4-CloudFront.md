# AWS CloudFront Lab

## 🎯 Objective
The purpose of this lab is to:
- Create an **S3 bucket** and upload an image file.
- Create a **CloudFront web distribution** and configure it with the S3 bucket as the origin.
- Understand how CloudFront delivers content from S3 through its global CDN.

---

## Task 1: Creating an S3 Bucket and Storing an Image File
1. Open the **Amazon S3** service in the AWS Management Console.
2. Create a new bucket with a unique name 
3. Upload an image file (e.g., `test.jpg`) into the bucket.
4. Verify that the image is stored successfully.

### Screenshots
![S3 Bucket Creation](https://github.com/user-attachments/assets/d9193c23-1786-4deb-b8ce-48a0c21620ae)  
![S3 Bucket Upload](https://github.com/user-attachments/assets/96563426-7410-4a8e-9060-a384ab41534b)

---

## Task 2: Creating a CloudFront Web Distribution
1. Open the **CloudFront** service in the AWS Management Console.
2. Create a new **Web Distribution**.
3. Configure the **Origin** as the S3 bucket created in Task 1.
4. Leave default caching and distribution settings (or adjust as needed).
5. Save and deploy the distribution.

### Screenshots
![CloudFront Distribution](https://github.com/user-attachments/assets/31cd0375-4c6b-45a8-b4dc-d3f8b8937081)  
![CloudFront Settings](https://github.com/user-attachments/assets/de7a6013-6f81-42af-be9e-18f8f5721809)  
![CloudFront Deployment](https://github.com/user-attachments/assets/33c2b6ba-7e29-4a9e-a73a-7d99954d28ab)

---

## Notes
- In this lab, only the **S3 bucket** and **CloudFront distribution** were created.  
- Due to restrictions, the bucket was not fully linked to CloudFront for public access.  
- The main takeaway is understanding how CloudFront acts as a **CDN** to deliver content stored in S3 with lower latency and global availability.

---

## 🔑 Key Concepts
- **S3 Bucket**: Stores the original content (images/files).
- **CloudFront**: Distributes cached copies of the content globally via edge locations.
- **Users**: Request content through CloudFront, which serves it faster and more securely.
