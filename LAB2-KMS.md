# AWS KMS (Key Management Service)

## Overview
**AWS Key Management Service (KMS)** is a managed service used to **create, manage, rotate, and delete cryptographic keys** that are used to encrypt data **at rest**.

KMS is tightly integrated with many AWS services such as:
- Amazon S3
- Amazon RDS
- AWS Lambda
- Amazon EBS

---

## KMS Key Types

### 1. AWS Managed Keys
- Keys are **created and managed by AWS**
- AWS is responsible for:
  - Key rotation
  - Permissions management
- Minimal control for the customer

Used when you want **simple encryption without deep control**.

---

### 2. Customer Managed Keys (CMK)
- Keys are **created and managed by the customer**
- The customer controls:
  - Key creation
  - Key rotation
  - Key policies
  - Key deletion

Used when you need:
- Fine-grained access control
- Auditing
- Compliance requirements

---

## Data Keys & Envelope Encryption

Data is **not encrypted directly** using the CMK.

Instead, KMS uses **Envelope Encryption**:

1. AWS KMS generates a **Data Key**
2. The data is encrypted using the **Data Key**
3. The Data Key itself is encrypted using the **CMK**
4. The encrypted Data Key is stored alongside the encrypted data

This approach improves:
- Performance
- Security
- Scalability

---

## Example: S3 with SSE-KMS (Decryption Flow)

When an encrypted object is accessed from Amazon S3:

1. Amazon S3 sends the **encrypted data key** to AWS KMS
2. AWS KMS decrypts the data key using the appropriate **CMK**
3. The **plaintext data key** is returned to Amazon S3
4. Amazon S3 decrypts the object
5. The plaintext data key is removed from memory immediately

---

## Important Notes
- KMS is used for **data at rest encryption**
- Access to encrypted data depends on:
  - IAM permissions
  - KMS key policies
- Even if a user can access S3, they **cannot decrypt data** without KMS permissions

---
## 🔐 KMS + CloudTrail + S3 (SSE-KMS) Workflow

### Steps

1. **Create a KMS Key**
   - Create a customer-managed KMS key.
   - Assign **key administrators** and **key users**.
   - Define key policies to control who can manage and use the key.

2. **Create a CloudTrail**
   - Configure AWS CloudTrail to record account activity.
   - Set CloudTrail to store logs in an **S3 bucket**.

3. **Enable SSE-KMS on the S3 Bucket**
   - Enable **Server-Side Encryption with AWS KMS (SSE-KMS)** on the S3 bucket.
   - Select the previously created KMS key as the encryption key.
   - All objects stored in the bucket will now be encrypted at rest.

4. **Upload and Access Objects**
   - Upload any object (e.g., an image) to the S3 bucket.
   - A user **with permission to use the KMS key** can successfully view the object.
   - A user **without KMS permissions** will receive an **Access Denied** error.

5. **Test Data Protection**
   - Remove or restrict S3 and KMS permissions.
   - Attempt to access the object again.
   - The object remains **encrypted and unreadable**, even if accessed directly.

### Result
- CloudTrail logs and all uploaded objects are **encrypted at rest** using KMS.
- Access requires **both S3 permissions and KMS decrypt permissions**.
- Even if the object is obtained without proper access, the data remains protected.
## Architecture & Flow Diagrams

<!-- Images retained as provided -->
<img width="1419" height="287" alt="image" src="https://github.com/user-attachments/assets/f783cab6-06a7-4a73-aa13-aba94216135c" />
<img width="1343" height="232" alt="image" src="https://github.com/user-attachments/assets/72b70add-2f2d-4d09-869a-03a60cbb5362" />
<img width="1919" height="924" alt="image" src="https://github.com/user-attachments/assets/890d12a3-9ba1-4b2f-9284-167286e29799" />
<img width="1919" height="928" alt="image" src="https://github.com/user-attachments/assets/3281859c-3ce0-4961-a580-470e99cecdc1" />
<img width="1919" height="840" alt="image" src="https://github.com/user-attachments/assets/0b099abc-8913-4267-9f4a-527ed9b72c55" />
<img width="1919" height="795" alt="image" src="https://github.com/user-attachments/assets/70b2477a-ed25-496f-9e22-edef8e499c82" />
<img width="1919" height="795" alt="image" src="https://github.com/user-attachments/assets/d9fef415-e199-4c35-abcf-9104c6570caf" />
<img width="1459" height="249" alt="image" src="https://github.com/user-attachments/assets/34cf25fa-50e4-481f-81dd-41335f74dcea" />
<img width="1919" height="857" alt="image" src="https://github.com/user-attachments/assets/33379a2e-3b6c-4215-84f2-49ae7a99b83c" />
<img width="1915" height="851" alt="image" src="https://github.com/user-attachments/assets/e4afbd19-ce8d-48ff-a976-3f8696cffe81" />
<img width="1919" height="769" alt="image" src="https://github.com/user-attachments/assets/d966f033-ca0e-42d0-a7d9-71071c67f212" />
<img width="1919" height="873" alt="image" src="https://github.com/user-attachments/assets/f37bb67f-1e26-404e-ad62-f90b3a6ed7fd" />
<img width="1919" height="938" alt="image" src="https://github.com/user-attachments/assets/70d412a9-da31-4911-85b2-4a99799ab44f" />
<img width="1919" height="817" alt="image" src="https://github.com/user-attachments/assets/4273998a-7a11-416c-bb36-85246406bda1" />
<img width="1919" height="414" alt="image" src="https://github.com/user-attachments/assets/bdd18e51-2e7d-4b94-8e24-7d835604da5c" />

---

## Accessing Objects Without KMS Permissions
When accessing an S3 object via URL **without proper KMS permissions**:
- The request fails
- Even if the object is public
- Because KMS decryption permissions are required

<img width="1919" height="435" alt="image" src="https://github.com/user-attachments/assets/aab9031d-bb5d-4741-876c-4ba5b9b896ee" />
<img width="1919" height="760" alt="image" src="https://github.com/user-attachments/assets/aaabe05c-43a6-41b4-8311-1ad9467ca95c" />
<img width="1919" height="880" alt="image" src="https://github.com/user-attachments/assets/6dbc5cbe-e9d4-44e6-9ac3-3fffb754f4b8" />
<img width="1919" height="906" alt="image" src="https://github.com/user-attachments/assets/e77ddeaa-d493-4c44-8d0d-4316b3cf3bd6" />
<img width="1919" height="638" alt="image" src="https://github.com/user-attachments/assets/e21b95c7-b9f0-4283-abfb-226d0269d29c" />
<img width="1919" height="307" alt="image" src="https://github.com/user-attachments/assets/1a3daefd-f334-4cc8-82f5-f7e0272e24f0" />
