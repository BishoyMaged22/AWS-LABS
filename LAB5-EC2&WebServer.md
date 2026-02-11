# AWS EC2 Lab

## 🎯 Objectives
- Launch a web server with termination protection enabled.
- Monitor your EC2 instance.
- Modify the security group to allow HTTP access.
- Resize your EC2 instance to scale.
- Test termination protection.
- Terminate your EC2 instance.

---

## Task 1: Launch a Web Server with Termination Protection
1. Open the **EC2 service** in the AWS Management Console.
2. Launch a new EC2 instance with the desired AMI (e.g., Amazon Linux).
3. Enable **Termination Protection** during instance creation.
4. Verify the instance is running.

### Screenshots
<img width="1919" height="196" alt="image" src="https://github.com/user-attachments/assets/9de1bc70-603d-41b6-b94a-0ede2ff084ed" />  
<img width="1919" height="571" alt="image" src="https://github.com/user-attachments/assets/2bd57b16-a8a9-4f38-9e46-56a04e9b99d3" />  
<img width="1259" height="250" alt="image" src="https://github.com/user-attachments/assets/a4cff9bf-1cc5-4daf-8768-467b2f57caaa" />  
<img width="1243" height="232" alt="image" src="https://github.com/user-attachments/assets/d5c6e732-8654-455e-b9ff-f570db8f9c3a" />  
<img width="1283" height="612" alt="image" src="https://github.com/user-attachments/assets/815914e6-63c9-42cd-9da5-09b75edd6b04" />  
<img width="1317" height="687" alt="image" src="https://github.com/user-attachments/assets/ca3c3c35-41d1-4e6a-abff-34e5cce5562f" />  
<img width="1020" height="549" alt="image" src="https://github.com/user-attachments/assets/05fe5170-eb52-4a61-9818-6c218c79e9cb" />  

---

## Task 2: Monitor Your Instance
- EC2 performs automated checks on every running instance to identify hardware and software issues.
- You can view **Instance Status Checks** and **CloudWatch Metrics** to monitor performance.
- Logs can be collected for troubleshooting.

### Screenshots
<img width="1649" height="369" alt="image" src="https://github.com/user-attachments/assets/cc1569d1-f30e-4644-bff2-cb9564b21a72" />  
CloudWatch metrics:  
<img width="1644" height="553" alt="image" src="https://github.com/user-attachments/assets/c5346a5f-32be-4f1f-9f9b-b589de05cb7c" />  
To get the logs:  
<img width="1919" height="880" alt="image" src="https://github.com/user-attachments/assets/575451bd-1074-4703-9d5d-7869eea51210" />  
<img width="1903" height="616" alt="image" src="https://github.com/user-attachments/assets/709ecf54-a594-4b72-a87b-29015b0f07ca" />  
<img width="698" height="586" alt="image" src="https://github.com/user-attachments/assets/4a7cf9d7-1a9e-41ec-9f9d-ad6f5a6a7d59" />  

---

## Task 3: Update Security Group and Access the Web Server
1. The instance has a public IP (e.g., `44.244.140.93`).
2. To allow HTTP access, update the **Inbound Rules** of the Security Group.
3. Add a rule to allow traffic on port **80 (HTTP)**.

### Screenshots
<img width="1919" height="875" alt="image" src="https://github.com/user-attachments/assets/3fad5060-b3a4-4df8-8f75-58b61a476cd1" />  
Public IP: `44.244.140.93`  
<img width="1919" height="528" alt="image" src="https://github.com/user-attachments/assets/67f73794-6a57-4446-ac84-8257e207829b" />  
<img width="1919" height="515" alt="image" src="https://github.com/user-attachments/assets/9becaa43-10cf-4ce0-b1ac-6d774a732862" />  
<img width="1919" height="235" alt="image" src="https://github.com/user-attachments/assets/f2a04004-0c48-44c0-8a8e-d49244201a94" />  

---

## Task 4: Resize Your Instance (Instance Type and EBS Volume)
1. Stop your instance.
2. Modify the instance type to scale up or down.
3. Adjust the EBS volume size if needed.
4. Restart the instance.

---

## Task 5: Test Termination Protection
- If termination protection is enabled, you cannot terminate the instance directly.
- You must first disable termination protection before terminating.

---

## Task 6: Terminate Your Instance
1. Disable termination protection (if enabled).
2. Terminate the instance.

### Screenshots
<img width="1919" height="356" alt="image" src="https://github.com/user-attachments/assets/3e25df5e-9a9a-42a8-9eba-8ba0fa66dcae" />  
<img width="1919" height="881" alt="image" src="https://github.com/user-attachments/assets/eee90a6f-f32a-4880-bba1-aef7093bfa82" />  
<img width="1917" height="880" alt="image" src="https://github.com/user-attachments/assets/36d34f2a-4f66-45cf-a015-8a9f3def13c1" />  
<img width="1919" height="851" alt="image" src="https://github.com/user-attachments/assets/48c43512-def7-44f4-b58a-4fbae0a11107" />  
<img width="1919" height="879" alt="image" src="https://github.com/user-attachments/assets/6f5e6718-6ae2-4074-adb4-cac5df9d9ed9" />  
<img width="1915" height="393" alt="image" src="https://github.com/user-attachments/assets/e228977a-0d6a-4ae4-8dab-00ada107eefb" />  
<img width="1915" height="393" alt="image" src="https://github.com/user-attachments/assets/b07f4fcf-0ea7-409b-a7fa-27afab78cb92" />  
<img width="1919" height="812" alt="image" src="https://github.com/user-attachments/assets/89c0bb90-b8c5-4229-a2ca-2fd17c3946cb" />  

---

## Notes
- If the instance is not deleted, you can change the **Termination Protection** setting to **Enable**.
