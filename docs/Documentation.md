# Phase 1

In the initial phase, we have developed a budget estimate and envisioned the infrastructure of the application. Upon carefully reviewing the project requirements, we made a strategic decision to establish two private and two public subnets within the Virtual Private Cloud (VPC), spanning across two Availability Zones. The private subnets are exclusively designated for the database, with the second subnet serving as a reliable backup for the primary one. As for the application itself, we have positioned the EC2 instances within the public subnets. Adhering to best practices, we have securely housed the database within a private subnet, effectively restricting access beyond our specifically created VPC.

To optimize resource utilization and maintain cost-efficiency, we will implement an autoscaling group for the two EC2 instances. Additionally, a single NAT gateway will be deployed to ensure prudent budget management, facilitating secure connectivity between the EC2 instances and the RDS database.

## Phase 2

We initiated the creation of a Virtual Private Cloud (VPC) to establish a secure network environment for our application. Within the VPC, we configured two private subnets and two public subnets, enabling us to separate and manage different components effectively. An internet gateway was implemented to facilitate connectivity between the VPC and the internet, while route tables were set up to direct traffic within the VPC. Furthermore, a NAT gateway was deployed to enable secure outbound internet access for resources within the private subnets.

Furthermore, we deployed an EC2 instance in a public subnet, configuring it to include both the application and the database. This setup allowed us to conduct tests on the application by inserting a small number of student records into the database.
### Phase 3

VERGLA

Problem statement:

Opportunity Statement:

The opportunity is to develop a comprehensive understanding and practical application of AWS services by successfully completing a project that encompasses various aspects of architecture design, cost estimation, web application deployment, network configuration, security settings, high availability, scalability, and access permissions.

Problem Statement:

The challenge is to create a solution using AWS services without step-by-step guidance, requiring the application of acquired skills throughout the learning process. The project involves multiple tasks, including creating an architectural diagram, estimating costs using the AWS Pricing Calculator, deploying a functional web application with a relational database, separating layers of the application, configuring a secure and publicly accessible virtual network, deploying the web application with load distribution, implementing high availability and scalability, and setting up access permissions between AWS services.

The problem to be solved is to successfully complete each task and demonstrate proficiency in designing, deploying, and managing a complex web application infrastructure using AWS services, while adhering to best practices for security, scalability, and cost optimization.

