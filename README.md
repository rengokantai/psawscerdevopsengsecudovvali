#### psawscerdevopsengsecudovvali
######6 UsingIAM
In EC2: ping self:
```
curl http://169.254.169.254/latest/meta-data/iam/security-credentials/Rolename
```
######7 Following the principle of least privilege
```
"Condition":{
  "IpAddress":{
    "aws:SourceIp":"1.2.3.4/32"
  }
}
```
######15 Delegating Access to Resources in Another AWS Account
02:21
create role-> select role type->Role for cross-account access

######17
######18 Creating an aws managed active directory
security and identity->Directory service->Create MicroSoft AD  
Directory DNS : ke.com  
NetBIOS name: ke  
2:50  
create access URL , countinue

######19 Launching an EC2 Instance
00:40  
create EC2 ,win2012->step3->Domain join directory.(choose we created)  
role select we will create.  
create role->AWS service roles->Amazon EC2 Role for simple systems manager->select->AmzEC2RoleForSSM->next step  
2:00
Advanced details,create ps1:
```
<powershell>
Install-WindowsFeature rsat-adds -IncludeManagementTools
</powershell>
```
######20 Setting up Federated Access
after connection to win2012, go to control panel->administrative tools->active directory users and computers  
shift rc,run as different user
(tbc 4:00)

######21 Web Identity Federation





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
