#lambdaFunction
##workflow diagram
<img width="674" height="452" alt="image" src="https://github.com/user-attachments/assets/d4b5fc65-ef27-4353-a2a6-9e1f586d6d72" />
- A user uploads an object to the source bucket in Amazon S3 (object-created event).

2 -Amazon S3 detects the object-created event.

3 - Amazon S3 publishes the object-created event to AWS Lambda by invoking the Lambda function and passing event data as a function parameter.

4 - AWS Lambda executes the Lambda function.

5  - From the event data it receives, the Lambda function knows the source bucket name and object key name. The Lambda function reads the object and creates a thumbnail using graphics libraries, then saves the thumbnail to the target bucket.
Task 1: Create the Amazon S3 buckets
<img width="1919" height="232" alt="image" src="https://github.com/user-attachments/assets/bce58628-b428-4aca-99fc-b4321ee458fe" />
Creating the bucket s3 
<img width="1919" height="651" alt="image" src="https://github.com/user-attachments/assets/fd35a3bb-5786-4749-80f9-c2487db36188" />
<img width="1919" height="185" alt="image" src="https://github.com/user-attachments/assets/4150e109-67da-4bbf-a25f-1a63b9874d91" />
Creating another bucket for the thumbnail
<img width="1919" height="700" alt="image" src="https://github.com/user-attachments/assets/f2165a60-9fb6-4472-8584-f10b21c32f66" />
<img width="1919" height="667" alt="image" src="https://github.com/user-attachments/assets/7eb528ea-6138-4acf-bb60-43e7e4a8fc5e" />
uploading a picture to first bucket
<img width="1919" height="552" alt="image" src="https://github.com/user-attachments/assets/7366b7bf-e27a-467b-9827-ec7b3c3fdd38" />
Task 2: Create an AWS Lambda function
<img width="1919" height="231" alt="image" src="https://github.com/user-attachments/assets/82b3313e-fafc-4f97-9de0-d3c58a2c9294" />
<img width="1918" height="863" alt="image" src="https://github.com/user-attachments/assets/2ddcafd0-a3ec-49fd-a4e3-384872b6803b" />
IAM role
<img width="1896" height="384" alt="image" src="https://github.com/user-attachments/assets/adadfb16-1a89-4dfd-b70f-89fba03b3941" />
Note: This role grants permission to the Lambda function to access Amazon S3 to read and write the images.
<img width="1919" height="786" alt="image" src="https://github.com/user-attachments/assets/898d60ef-759a-445b-a4c2-1bfb42102962" />
specify the vpc and the subnet where the S3 is created
<img width="1919" height="530" alt="image" src="https://github.com/user-attachments/assets/6c1301b3-0379-40c3-8b51-7c11ad002583" />
<img width="1919" height="890" alt="image" src="https://github.com/user-attachments/assets/802ccd88-0003-4bbb-b107-867fa3e01511" />
<img width="1919" height="893" alt="image" src="https://github.com/user-attachments/assets/f63881b7-fe9c-4a74-88b9-eafccd3ebe71" />
<img width="1919" height="878" alt="image" src="https://github.com/user-attachments/assets/5976367b-e15c-45ff-ab52-0b0f8572a344" />
<img width="1919" height="649" alt="image" src="https://github.com/user-attachments/assets/ed19d117-e5b0-472f-89be-c52c04361118" />
Task 3: Test your function
<img width="1903" height="876" alt="image" src="https://github.com/user-attachments/assets/e52b1cd1-5d89-4cc4-8e53-d25ca7b1fc12" />
<img width="1919" height="889" alt="image" src="https://github.com/user-attachments/assets/0b892b35-e927-48e0-af9e-50607a9d4f48" />
<img width="1578" height="618" alt="image" src="https://github.com/user-attachments/assets/19e775ac-ed27-4a59-97af-a25c535ed193" />

