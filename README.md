# DevopsAssessment
First I set up a BookStore web application. 
Mysql database was installed in an t2.micro ec2 instance.
Attached EBS volume to the instance for automating backup.
<img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/Screenshot%20from%202023-09-13%2018-49-55.png" width="800" height="600">
Then build a Docker image of the application and pushed it into Docker hub.
<img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/Screenshot%20from%202023-09-13%2019-18-30.png" width="800" height="600">
Set up Kubernetes master using a t2.medium ec2 instance and provided necessery security groups.
