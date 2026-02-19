## Objectives
- Create a bucket in Amazon S3
- Add an object to a bucket
- Manage access permissions on an object and a bucket
- Create a bucket policy
- Use bucket versioning
--------------------
## Lab Scenario
You work for a company using Amazon S3 for data storage. An application residing on an EC2 instance needs to push reporting data to an S3 bucket daily. You are tasked with creating an S3 bucket for your company to use for storing this report data. For a successful deployment, you need to ensure the EC2 instance has enough privileges to be able to upload and retrieve data from the S3 bucket. For security reasons, only the EC2 instance can write data to the S3 bucket. The files in the S3 bucket also require protection against accidental deletion.
## Create S3 bucket
In this task, you create a bucket to hold your EC2 report data and then examine the different bucket configuration options
<img width="1919" height="364" alt="image" src="https://github.com/user-attachments/assets/9438c4a1-6483-436e-ad04-908b2fda0958" />
<img width="1892" height="930" alt="image" src="https://github.com/user-attachments/assets/48b818e9-1f39-4c52-a06c-06a617ebce55" />
<img width="1889" height="546" alt="image" src="https://github.com/user-attachments/assets/220cc753-5100-4f23-933c-2c71437b5510" />
## ADD an object to the bucket
<img width="1919" height="625" alt="image" src="https://github.com/user-attachments/assets/e524cc1c-4c7f-46da-9819-9e88aecb6d70" />
<img width="1894" height="874" alt="image" src="https://github.com/user-attachments/assets/fa2ac416-0996-4db6-a2ff-22c8d56f7e60" />
## Make an object public
s3://reportbucket-099818743643/new-report.png
Access Dinied
<img width="1919" height="245" alt="image" src="https://github.com/user-attachments/assets/de8cfa1a-2307-42bb-b2e2-636fa321985e" />
<img width="1919" height="878" alt="image" src="https://github.com/user-attachments/assets/2aa5a8ac-fba0-4aa2-ac11-5a516f5ffeec" />
Make public using acl
<img width="1919" height="877" alt="image" src="https://github.com/user-attachments/assets/235508e5-6c66-4b2a-b9d2-4cfe3038d567" />
<img width="1919" height="146" alt="image" src="https://github.com/user-attachments/assets/2790f213-1f15-4589-9846-4591c24deb8b" />
 Notice the warning Public access is blocked because Block Public Access settings are turned on for this bucket.
 <img width="1919" height="661" alt="image" src="https://github.com/user-attachments/assets/cffbeee8-ed56-4c0a-9377-4647a6a5d049" />
<img width="1919" height="76" alt="image" src="https://github.com/user-attachments/assets/94b0bf61-9c5a-4ab6-bd8b-091e44577f5e" />
<img width="1919" height="653" alt="image" src="https://github.com/user-attachments/assets/c529a52d-0cb1-4f90-b42e-d0f3358e24d8" />
<img width="1919" height="1026" alt="image" src="https://github.com/user-attachments/assets/a8f4c96b-4d96-4d53-9980-d6feabca42f6" />
## Test connectivity from the EC2 instance
<img width="1919" height="206" alt="image" src="https://github.com/user-attachments/assets/2532dfd8-eef3-4b1f-bc75-468e7189fe48" />
<img width="1919" height="237" alt="image" src="https://github.com/user-attachments/assets/0acfa48e-7552-4c10-a5b2-f94dbdd9cc9b" />
<img width="1919" height="873" alt="image" src="https://github.com/user-attachments/assets/e99ab347-8fcd-422a-a40f-4cb820bcf8fe" />
<img width="1919" height="429" alt="image" src="https://github.com/user-attachments/assets/313ee581-76bc-410d-a407-fd53e587976e" />
## Create a bucket policy
<img width="1919" height="608" alt="image" src="https://github.com/user-attachments/assets/13fd2d27-0b88-483b-a23f-313b28d83d8f" />
<img width="1919" height="874" alt="image" src="https://github.com/user-attachments/assets/67669d1b-5b5e-4184-a7e8-5461261888ba" />
<img width="1919" height="257" alt="image" src="https://github.com/user-attachments/assets/396d69e0-6957-4442-9338-86dc434d941f" />
i need to make it public access, the default access to objects is denied 
<img width="1919" height="311" alt="image" src="https://github.com/user-attachments/assets/edc3337c-ae24-40a7-a1e4-c065ee117465" />
<img width="1919" height="462" alt="image" src="https://github.com/user-attachments/assets/57761c1f-6138-412a-a004-cc79c393f3a5" />
<img width="1919" height="873" alt="image" src="https://github.com/user-attachments/assets/903ea498-78a0-44da-b8a1-bf598066fdba" />
<img width="1919" height="869" alt="image" src="https://github.com/user-attachments/assets/3ed3c221-0c44-4832-8fb1-8528883bc11e" />
<img width="1919" height="982" alt="image" src="https://github.com/user-attachments/assets/630d520e-145d-4791-83c0-ac64effa7965" />
<img width="1919" height="979" alt="image" src="https://github.com/user-attachments/assets/8bd95a06-42f1-4eb7-8dc8-8b1c0750a942" />
<img width="1050" height="800" alt="image" src="https://github.com/user-attachments/assets/91f9b3d0-856e-4823-965b-66222f75095d" />
<img width="1913" height="902" alt="image" src="https://github.com/user-attachments/assets/16417acf-3de5-4363-8f4b-b8d860ef27ca" />
principle role: that means who has the access to this s3 put and get objects (EC2)
<img width="1919" height="474" alt="image" src="https://github.com/user-attachments/assets/1d5aa17b-dcaa-4d43-bbd9-06c1341cd5b5" />

