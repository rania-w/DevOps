# Approach

 
 # Phase 1

In the initial phase, we have developed a budget estimate and envisioned the infrastructure of the application. Upon carefully reviewing the project requirements, we made a strategic decision to establish two private and two public subnets within the Virtual Private Cloud (VPC), spanning across two Availability Zones. The private subnets are exclusively designated for the database, with the second subnet serving as a reliable backup for the primary one. As for the application itself, we have positioned the EC2 instances within the public subnets. Adhering to best practices, we have securely housed the database within a private subnet, effectively restricting access beyond our specifically created VPC.

To optimize resource utilization and maintain cost-efficiency, we will implement an autoscaling group for the two EC2 instances. Additionally, a single NAT gateway will be deployed to ensure prudent budget management, facilitating secure connectivity between the EC2 instances and the RDS database.

![IMG-1480](https://github.com/rania-w/ibu-devops-engineering-on-aws-cloud-group-11/assets/92021975/76cd7f46-dfe0-4385-bce4-9beb6d54eeb5)

# Phase 2

We initiated the creation of a Virtual Private Cloud (VPC) to establish a secure network environment for our application. Within the VPC, we configured two private subnets and two public subnets, enabling us to separate and manage different components effectively. An internet gateway was implemented to facilitate connectivity between the VPC and the internet, while route tables were set up to direct traffic within the VPC. Furthermore, a NAT gateway was deployed to enable secure outbound internet access for resources within the private subnets.

Furthermore, we deployed an EC2 instance in a public subnet, configuring it to include both the application and the database. This setup allowed us to conduct tests on the application by inserting a small number of student records into the database.

![IMG-1481](https://github.com/rania-w/ibu-devops-engineering-on-aws-cloud-group-11/assets/92021975/c1d8d402-384f-4703-b929-37f766bec11c)

# Phase 3

During phase 3 of the project, we made the decision to create a new EC2 instance dedicated solely to running the application. In this phase, we utilized the script specifically designed for phase 3, excluding the creation of a database. Furthermore, we successfully established an RDS MySQL database, configured to allow traffic exclusively from the EC2 instance where the application is deployed. This ensures secure and controlled access. To facilitate the development process, we set up a Cloud9 environment. In this particular phase, the environment was primarily utilized to create a secret that securely stores the database credentials. This secret may potentially be utilized in phase 4 for load balancer testing. Regarding the database migration, we employed the following procedure: on the EC2 instance from phase 2, we extracted the database and its corresponding data into a file. Subsequently, we imported this file into the newly created RDS database to ensure a seamless transition.

![IMG-1482](https://github.com/rania-w/ibu-devops-engineering-on-aws-cloud-group-11/assets/92021975/ac4c6988-1070-4de0-b71f-4450eb6732ec)

# Problem statement:

## Opportunity Statement:

The opportunity is to develop a comprehensive understanding and practical application of AWS services by successfully completing a project that encompasses various aspects of architecture design, cost estimation, web application deployment, network configuration, security settings, high availability, scalability, and access permissions.

## Problem Statement:

The challenge is to create a solution using AWS services without step-by-step guidance, requiring the application of acquired skills throughout the learning process. The project involves multiple tasks, including creating an architectural diagram, estimating costs using the AWS Pricing Calculator, deploying a functional web application with a relational database, separating layers of the application, configuring a secure and publicly accessible virtual network, deploying the web application with load distribution, implementing high availability and scalability, and setting up access permissions between AWS services.

The problem to be solved is to successfully complete each task and demonstrate proficiency in designing, deploying, and managing a complex web application infrastructure using AWS services, while adhering to best practices for security, scalability, and cost optimization.

