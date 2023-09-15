# DevopsAssessment
- **Set up a BookStore web application.**

- **Database Setup:**

   Mysql database was installed in an ec2 instance.

   Security Groups for the database was configured.

   For the application "bookdb" database was created.

   The database contains table "book" with fields book,author,price. 

- **Database Backup:**

   Created an EBS volume and attached to the instance for automating backup. 

   Cronjob is created to execute the backup file for automation of backup.

   <img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/Screenshot%20from%202023-09-13%2018-49-55.png" width="600" height="400">

   <img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/Screenshot%20from%202023-09-13%2020-16-50.png" width="500" height="300">

- **Maven:**

  Maven was used to package the application into a jar file.

- **Docker Build:**
  
   Build a Docker image of the application using Dockerfile(in BookStoreTrials folder).

   The image is pushed to Docker Hub.

   <img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/Screenshot%20from%202023-09-13%2019-18-30.png" width="800" height="600">

- **Kubernetes:**
    
   Set up Kubernetes cluster using kubeadm , EKS with two worker nodes and provided necessery security groups.

   Created a Deployment and service configuration to deploy the containerized instance of web application (yaml file in kubernetes folder).

   Using kubectl commands made sure that all pods are running.

   <img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/Screenshot%20from%202023-09-13%2022-02-49.png" width="600" height="200">

   <img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/Screenshot%20from%202023-09-13%2022-03-45.png" width="600" height="400">
   
- **AWS Configuration:**

    Created Target Group to to route traffic to the worker nodes.

    Attached the target group to an AWS Application load balancer (ALB) to manage the traffic and created appropriate target group.

    http://demo-alb-1847155200.ap-south-1.elb.amazonaws.com/

    <img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/Screenshot%20from%202023-09-13%2013-43-39.png" width="800" height="600">
   
    <img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/Screenshot%20from%202023-09-13%2013-43-54.png" width="800" height="600">

    <img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/load%20balancer.jpeg" width="800" height="600">

- **Jenkins Pipeline**

    Jenkins pipeline was created for the Deployment(Jenkins file in Repository).

    **Stage 1: Github Integration:** The webapp repository is cloned.

    **Stage 2: Maven Build:** Packaged the application into jar file using mvn clean package.

    **Stage 3: Docker build and push:** Build docker image and push the image to Docker hub.

    **Stage 4: Upload to Nexus:** Upload the application to nexus repository manager.

    **Stage 5: Deploy to Kubernetes:** The application is then deployed into kubernetes.

   <img src="https://github.com/Haseen-Fairuz/DevopsAssessment/blob/main/Screenshots/Screenshot%20from%202023-09-13%2021-29-51.png" width="600" height="300">
