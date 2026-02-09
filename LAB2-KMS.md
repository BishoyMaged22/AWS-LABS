#KMS (Key management service)
it's a service used to generate and rotate,delete keys used to encrypt data at rest 
integrated with AWS services such as S3,RDS,Lambda,EBS
KMS types
1- AWS managed keys: Aws generate it and be responsibile for rotation and permissions 
2-CMK (customer managed keys): the customer is responsibile for key generating,rotation,poilcy,deleting 
the generated key from AWS or CMK is being encrypted again and called data key and that's used to encrypt data at rest
