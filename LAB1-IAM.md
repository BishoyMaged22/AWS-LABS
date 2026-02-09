<h1>IAM (Identity and Access Management)</h1>
Goal
IAM is used to manage who can access an account and what actions they can perform.
Core Components
1. Identity (Who?)
- IAM Users: Individual accounts for specific people.
- IAM Groups: Collections of users to simplify permission management.
- IAM Roles: Temporary identities used for delegation or cross-service access.
2. Access (What?) on [IAM users, Resources]
- IAM Policies: JSON documents that define permissions (Authorization).
3. Management (Administration)
Admins are responsible for:
- Creating users.
- Creating groups.
- Attaching policies to control permissions.
<h2>lab IAM </h2>
<img width="1919" height="230" alt="image" src="https://github.com/user-attachments/assets/1c90a9ef-de71-483f-b67a-dc8af32dc98b" />
Existing users
<img width="1919" height="869" alt="image" src="https://github.com/user-attachments/assets/81b04e36-89ec-4693-a2ec-0b2d95bc6daa" />
creating new user
The access can be through Keys or management console (GUI)
<img width="1919" height="872" alt="image" src="https://github.com/user-attachments/assets/b059e2d0-5ec9-44b8-b7db-1233d38fdb01" />
permissions can be attached from another user or can be attached from stable templates or we can create a new one
<img width="1919" height="882" alt="image" src="https://github.com/user-attachments/assets/c22b0d2b-1766-4cc9-9672-d4f9b3ea87ed" />
<img width="1919" height="826" alt="image" src="https://github.com/user-attachments/assets/b15d875d-bad4-4585-938d-2ca669eb3cdb" />
<img width="1919" height="873" alt="image" src="https://github.com/user-attachments/assets/952e23b8-edb7-4be5-805e-030fb489e45f" />
back to users
<img width="1919" height="482" alt="image" src="https://github.com/user-attachments/assets/ef64a070-bb5d-4c10-b000-3ccf90becd9d" />
user 1 doesn't have any permissions 
<img width="1919" height="883" alt="image" src="https://github.com/user-attachments/assets/792bdfcb-4f4b-49e7-b6c8-a648e9ca93c1" />
not attached to any groups too
<img width="1919" height="414" alt="image" src="https://github.com/user-attachments/assets/7617ff9f-cab5-45dc-b417-4a01cb9d8415" />
i'll add user1 to EC2 support group and he will get these permissions directly
<img width="1919" height="571" alt="image" src="https://github.com/user-attachments/assets/2a2fc1ee-ab5c-4205-95d8-56dd484fc4f2" />
<img width="1919" height="343" alt="image" src="https://github.com/user-attachments/assets/c598efa8-03cb-41b5-b225-918a9c81b8c2" />
<img width="1508" height="495" alt="image" src="https://github.com/user-attachments/assets/fb92a3e0-8b17-4849-ad55-425eafe3f3c3" />
and for S3 Read only access
<img width="1527" height="425" alt="image" src="https://github.com/user-attachments/assets/de4d4c81-338d-4436-9fa9-a36862ae465e" />
and for EC2 admin
<img width="1513" height="449" alt="image" src="https://github.com/user-attachments/assets/37b4865f-d610-4d54-97cc-28885ae8bd88" />
<img width="1630" height="407" alt="image" src="https://github.com/user-attachments/assets/035e8e9d-35c0-473a-8ad0-83223ac51a7e" />
Now as the following table i'll add every user to it's specific group
<img width="1919" height="474" alt="image" src="https://github.com/user-attachments/assets/355b6e6d-6d55-4694-bfaa-bc52cc222023" />
user-2
<img width="1919" height="459" alt="image" src="https://github.com/user-attachments/assets/b9183387-6c5d-4b21-a6ea-ceec186a1429" />
user-3
<img width="1919" height="484" alt="image" src="https://github.com/user-attachments/assets/c9d4e71c-1d32-45ca-bfee-12aa425dc5e8" />
And now we can test the users
<img width="1919" height="929" alt="image" src="https://github.com/user-attachments/assets/dfb2ff3b-1fcf-48b9-81fd-a3d5d978c34e" />
to sign in to user1 
i'll copy console sign in link
<img width="1919" height="978" alt="image" src="https://github.com/user-attachments/assets/e27000cb-0edf-4d01-a971-dbeba882739a" />
<img width="1919" height="389" alt="image" src="https://github.com/user-attachments/assets/c00c5574-9f43-4586-abe7-d1783dbce26b" />
S3 bucket
<img width="1919" height="866" alt="image" src="https://github.com/user-attachments/assets/08333a64-5943-4cf3-9ca9-123955377cdf" />
and trying to create a bucket >Denied 
<img width="1919" height="862" alt="image" src="https://github.com/user-attachments/assets/4838b8af-87a8-4186-a74f-a8909c68bad7" />
user-2 Readonly EC2
<img width="1919" height="980" alt="image" src="https://github.com/user-attachments/assets/a91bb7fe-68ac-459a-a85d-9bdfc9dfa94f" />
<img width="1919" height="866" alt="image" src="https://github.com/user-attachments/assets/a0566a54-40c9-476d-b1b7-71604f832a19" />
<img width="1919" height="873" alt="image" src="https://github.com/user-attachments/assets/568815f9-442e-4c7f-9c3a-6b1d5dafb960" />
<img width="1919" height="488" alt="image" src="https://github.com/user-attachments/assets/0a997117-f2c6-4e15-9149-b5c49651a15e" />
user-3 EC2 
<img width="1919" height="1024" alt="image" src="https://github.com/user-attachments/assets/467d2c50-645d-4cc2-b857-227c5bb27f83" />
<img width="1919" height="871" alt="image" src="https://github.com/user-attachments/assets/810b34e6-4bff-499e-8e15-4aa3fca5d371" />
i can stop instance because i have admin permissions
<i>Author:bishoy maged</i>







