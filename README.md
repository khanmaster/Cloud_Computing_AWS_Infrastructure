# Cloud Computing
## Amazon Web Services (AWS)
### AWS Global Infrastructure
#### AWS Regions
#### AWS Availability Zones (AZs)
#### Advantages of Cloud Computing and AWS

### Public Cloud - Pivate Cloud and Hybrid Cloud use cases
- Iaas - PaaS - SaaS examples?
- Cloud Data Centers



## AWS Services
- Elasic Compute Service `EC2`
  
- Simple Storage Service `S3`
- Virtual Private Network `VPC`
- Internet Gateway `IG`
- Route Tables `RT`
- Subnets `sn`
- Network Access Control `NALs`
- Security Groups `SG`
- Cloudwatch `CW`
- Simple Notification Service `SNS`
- Simple Queue Service `SQS`
- Load Balancers `LB` - `ALB` - `ELB` - `NLB`
- Autoscaling Groups `ASG`
- Amazon Machine Image `AMI`
- Dynamodb - Mongodb
  
  # Launch ec2 instance

- ssh debugging
```
eval ssh-agent

ssh-add "keyfile.pem"
```
- update and upgrade system
- install nginx
- nginx enabled
- check the public globally
  
- install node correct version
- install required dependencies
- `app code` currently available on `localhost`
- task: `find out how to migrate/transfer/copy data from on prem to cloud`
  
- npm install 
- npm start

- share your public ip with port 3000 displaying node home page
- second iteration set up the reverse proxy so we could load node page on the public ip with out port 3000

### AWS Global Infrastructure
- AWS Region and Availability Zones
  
![](images/aws_networking_sg1.png)

- 2Tier Achitecture Deployment

![](images/MicrosoftTeams-image%20(8).png)


### Monitoring
![](images/Screenshot%20(157).png)



### S3
- `aws s3 ls` to list buckets
- `aws --version`
- `aws configure` to add our keys and config 
- `aws s3 mb s3://name --region name`
- `aws s3 cp s3://name/ file.md`
- `aws s3 rm s3://bucketname --recursive`
- `aws s3 rb s://bucketname`
- `aws s3 sync s3://bucketname/ test`
  
### AWSCLI
- AWSCLI can be used to create any `aws` resources required

### CD Jenkins
```
ssh -A -o "StrictHostKeyChecking=no" ubuntu@34.251.140.216 << EOF	

cd /home/ubuntu/app
export DB_HOST=db-ip:27017/posts/
node seeds/seed.js
nohup node app.js > /dev/null 2>&1 &

EOF
```