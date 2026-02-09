#KMS (Key management service)
it's a service used to generate and rotate,delete keys used to encrypt data at rest 
integrated with AWS services such as S3,RDS,Lambda,EBS
KMS types
1- AWS managed keys: Aws generate it and be responsibile for rotation and permissions 
2-CMK (customer managed keys): the customer is responsibile for key generating,rotation,poilcy,deleting 
the generated key from AWS or CMK is being encrypted again and called data key and that's used to encrypt data at rest
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
open
<img width="1919" height="1009" alt="image" src="https://github.com/user-attachments/assets/2a0a13c1-4f8d-4df0-8ed2-f67abce78977" />
Amazon S3 sends the encrypted data key to AWS KMS
AWS KMS decrypts the key by using the appropriate master key and sends the plaintext key back to Amazon S3
Amazon S3 decrypts the ciphertext and removes the plaintext data key from memory as soon as possible
when opening from url without kms (regular user)
<img width="1919" height="435" alt="image" src="https://github.com/user-attachments/assets/aab9031d-bb5d-4741-876c-4ba5b9b896ee" />
<img width="1919" height="760" alt="image" src="https://github.com/user-attachments/assets/aaabe05c-43a6-41b4-8311-1ad9467ca95c" />
<img width="1919" height="880" alt="image" src="https://github.com/user-attachments/assets/6dbc5cbe-e9d4-44e6-9ac3-3fffb754f4b8" />
<img width="1919" height="906" alt="image" src="https://github.com/user-attachments/assets/e77ddeaa-d493-4c44-8d0d-4316b3cf3bd6" />
<img width="1919" height="638" alt="image" src="https://github.com/user-attachments/assets/e21b95c7-b9f0-4283-abfb-226d0269d29c" />
<img width="1919" height="307" alt="image" src="https://github.com/user-attachments/assets/1a3daefd-f334-4cc8-82f5-f7e0272e24f0" />


