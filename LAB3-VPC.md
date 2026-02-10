# Amazon Virtual Private Cloud (VPC)

## Objectives

1. **Create an Amazon VPC** using the VPC Wizard.  
2. **Explore the basic components of a VPC**, including:
   - Public and private subnets
   - Route tables and routes
   - NAT gateways
   - Network ACLs

---

## Creating VPC

**Step 1: Launch the VPC Wizard**  
<img width="918" height="643" alt="VPC Wizard" src="https://github.com/user-attachments/assets/46c42af9-de8a-4f78-bb54-c17ef4de7d49" />

**Step 2: Select VPC Settings**  
<img width="1919" height="254" alt="VPC Settings" src="https://github.com/user-attachments/assets/3fb0074b-5db4-4e21-84b9-feaf8f74aa53" />  

- **VPC CIDR**: `10.0.0.0/16`  
<img width="1919" height="887" alt="VPC CIDR" src="https://github.com/user-attachments/assets/f5c7f44b-1f9d-462b-bec7-21469deccd5c" />

- **Public Subnet IP**: `10.0.25.0/24`  
- **Private Subnet IP**: `10.0.50.0/24`  
<img width="606" height="637" alt="Subnets" src="https://github.com/user-attachments/assets/348854df-4edc-46e6-a6df-2be4b97d391b" />  
<img width="630" height="817" alt="Subnets" src="https://github.com/user-attachments/assets/24536ada-7382-4870-a618-148fece8adeb" />

**Step 3: View the VPC**  
<img width="1919" height="434" alt="VPC Overview" src="https://github.com/user-attachments/assets/6bde39b8-eebf-40dd-9f7e-68d4e4a375d3" />  

- **Internet Gateway (IGW)** attached to the public subnet  
- **Private Subnet** attached to NAT Gateway  
<img width="1919" height="921" alt="IGW and NAT" src="https://github.com/user-attachments/assets/a48b75f4-4e62-4339-8e0d-905bc019dece" />  
<img width="1919" height="880" alt="Route Tables" src="https://github.com/user-attachments/assets/a00c6057-574d-4a5d-90b3-4110c2337ddb" />  
<img width="1919" height="878" alt="Subnets Overview" src="https://github.com/user-attachments/assets/362b7f68-33c0-4a64-ba6f-c1edac722f3f" />

---

## Applying Security

**Step 4: Network ACL (NACL) for Subnet**  
<img width="1919" height="875" alt="NACL" src="https://github.com/user-attachments/assets/af86d1a1-67e7-411d-b11b-bcaee127ce19" />  

- **Allow all inbound traffic**  
<img width="1919" height="370" alt="Inbound Traffic" src="https://github.com/user-attachments/assets/9a08f014-c726-488d-a567-8f33ef1755d7" />  

- **Allow all outbound traffic**  
<img width="1919" height="491" alt="Outbound Traffic" src="https://github.com/user-attachments/assets/6b52ebc9-7dc0-4635-a7fb-5c9510ef2975" />  
<img width="1919" height="558" alt="Outbound Traffic" src="https://github.com/user-attachments/assets/af5405e6-6976-4f76-8be8-d4ba560819c9" />  
<img width="1919" height="876" alt="NACL Applied" src="https://github.com/user-attachments/assets/cb137dba-23bb-4580-8590-75558f8f72dc" />

---

## Security Groups (SG)

- **Default Security Group** is created automatically  
<img width="1919" height="204" alt="Default SG" src="https://github.com/user-attachments/assets/4a329063-a8c9-4c05-9480-2b1b5ea9b264" />  
<img width="1919" height="494" alt="Default SG Rules" src="https://github.com/user-attachments/assets/ab41f434-c928-4b18-89ca-22db3fcfe322" />

**Notes:**  
- `Source: Custom` → يسمح لجميع الخدمات المرتبطة بهذا الـ SG بالتواصل مع بعضها.  
- تغيير المصدر إلى `Anywhere (IPv4)` → يعني أن كل الإنترنت يمكنه الوصول.

---

