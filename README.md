#### psawscerdevopsengsecudovvali
######6 UsingIAM
In EC2: ping self:
```
curl http://169.254.169.254/latest/meta-data/iam/security-credentials/Rolename
```

######24 Protecting data in S3
server-side encryption
- s3 managed keys
- KMS key managment service
- customer-provided keys
client-side encryption
- KMS-managed customer master key
- client side master key  

Demo:  
s3->upload->serverside encryption  
service master key: S3 will decrypt the object for anyone with permission to access this object.  
kms master key: S3 will decrypt the object for anyone with permission to access this object and permission to use the master key.  


######25 working with amazon EBS volume
For amazon offical ami, root volume can not encrypted.  
To encrypt root volume, you need to create your own ami copy from official ami.  
copy amzlinux:ami-31490d51, rightclick: copy AMI



######32 Physical and logical Access Control
physical access control
- SOC1 SOC2
- PCI DSS
- ISO 27001
- FedRAMP
######33 Securing IT resource
- Hardware VPN
- AWS direct connect
- AWS VPN Cloudhub
- software VPN


AWS storage gateway: A on-premise  application to securely backup data to aws platform.  
AWS i/e: transfer by mail, not internet
