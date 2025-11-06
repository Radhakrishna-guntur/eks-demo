# What is EKS

Amazon Elastic Kubernetes Service (EKS) is AWS’s managed Kubernetes offering. By handling the control plane—API servers, etcd, schedulers, controllers—EKS lets you focus on deploying and operating your containerized workloads. Unlike a self-managed Kubernetes cluster, Amazon EKS splits responsibilities: AWS manages the control plane, while you maintain the data plane in your own AWS account.

**A standard Kubernetes cluster consists of two main layers:**

## **Control Plane:  **   etcd (the key/value store),      API Server ,     Scheduler,       Controller Manager.

## **Data Plane: **   Worker nodes (EC2 instances or AWS Fargate) ,       Pods and containers


<img width="1320" height="695" alt="Screenshot 2025-11-03 at 2 47 05 PM" src="https://github.com/user-attachments/assets/e8b01859-04a7-4cf8-9a5d-b9f17bde4e6d" />


EKS Shared Responsibility Model "

With Amazon EKS, AWS takes care of the highly available, secure control plane, while you manage your worker nodes and application workloads.

# AWS Manages (Control Plane) :

etcd, API Server, Scheduler	 

Controller Manager	    

Control Plane VPC networking & HA	 

Automatic backups, updates & scaling	                             

# You Manage (Data Plane):

Worker Nodes (EC2 instances or Fargate)

Operating System patches & node upgrades

Kubernetes workloads, Namespaces, RBAC, CRDs

Pod configuration, Security Groups, IAM roles

# Features of Amazon EKS

Amazon EKS provides the following high-level features:

**Management interfaces**
EKS offers multiple interfaces to provision, manage, and maintain clusters, including AWS Management Console, Amazon EKS API/SDKs, CDK, AWS CLI, eksctl CLI, AWS CloudFormation, and Terraform. For more information, see Get started with Amazon EKS and Amazon EKS cluster lifecycle and configuration.

**Access control tools**
EKS relies on both Kubernetes and AWS Identity and Access Management (AWS IAM) features to manage access from users and workloads. For more information, see Grant IAM users and roles access to Kubernetes APIs and Grant Kubernetes workloads access to AWS using Kubernetes Service Accounts.

**Compute resources**
For compute resources, EKS allows the full range of Amazon EC2 instance types and AWS innovations such as Nitro and Graviton with Amazon EKS for you to optimize the compute for your workloads. For more information, see Manage compute resources by using nodes.

**Storage**
EKS Auto Mode automatically creates storage classes using EBS volumes. Using Container Storage Interface (CSI) drivers, you can also use Amazon S3, Amazon EFS, Amazon FSX, and Amazon File Cache for your application storage needs. For more information, see Use application data storage for your cluster.

**Security**
The shared responsibility model is employed as it relates to Security in Amazon EKS. For more information, see Security best practices, Infrastructure security, and Kubernetes security.

**Monitoring tools**
Use the observability dashboard to monitor Amazon EKS clusters. Monitoring tools include Prometheus, CloudWatch, Cloudtrail, and ADOT Operator. For more information on dashboards, metrics servers, and other tools, see EKS cluster costs and Kubernetes Metrics Server.

**Kubernetes compatibility and support**
Amazon EKS is certified Kubernetes-conformant, so you can deploy Kubernetes-compatible applications without refactoring and use Kubernetes community tooling and plugins. EKS offers both standard support and extended support for Kubernetes. For more information, see Understand the Kubernetes version lifecycle on EKS.


# EKS - Create Cluster

## List of Topics 
- Install CLIs
  - AWS CLI
  - kubectl
  - eksctl
- Create EKS Cluster
- Create EKS Node Groups
- Understand EKS Cluster Pricing
  - EKS Control Plane
  - EKS Worker Nodes
  - EKS Fargate Profile
- Delete EKS Clusters 

Amazon EKS: Simplified Kubernetes Management


Amazon Elastic Kubernetes Service (EKS) provides a fully managed Kubernetes service that eliminates the complexity of operating Kubernetes clusters. With EKS, you can:

Deploy applications faster with less operational overhead

Scale seamlessly to meet changing workload demands

Improve security through AWS integration and automated updates

Choose between standard EKS or fully automated EKS Auto Mode

Amazon Elastic Kubernetes Service (Amazon EKS) is the premiere platform for running Kubernetes clusters, both in the Amazon Web Services (AWS) cloud and in your own data centers (EKS Anywhere and Amazon EKS Hybrid Nodes).
Amazon EKS simplifies building, securing, and maintaining Kubernetes clusters. It can be more cost effective at providing enough resources to meet peak demand than maintaining your own data centers. 


Note:

Amazon Elastic Kubernetes Service (Amazon EKS) is a managed Kubernetes service to run Kubernetes in the AWS cloud and on-premises data centers.

In the cloud, Amazon EKS automatically manages the availability and scalability of the Kubernetes control plane nodes responsible for scheduling containers, managing application availability, storing cluster data, and other key tasks.

With Amazon EKS, you can take advantage of all the performance, scale, reliability, and availability of AWS infrastructure, as well as integrations with AWS networking and security services. On-premises, EKS provides a consistent, fully supported Kubernetes solution with integrated tooling and simple deployment to AWS Outposts, virtual machines, or bare metal servers.

# Services to use with Amazon EKS

You can use other AWS services with the clusters that you deploy using Amazon EKS:

## Amazon EC2:

Obtain on-demand, scalable compute capacity with Amazon EC2.

## Amazon EBS:

Attach scalable, high-performance block storage resources with Amazon EBS.

## Amazon ECR:

Store container images securely with Amazon ECR.

## Amazon CloudWatch:

Monitor AWS resources and applications in real time with Amazon CloudWatch.

## Amazon Prometheus:

Track metrics for containerized applications with Amazon Managed Service for Prometheus.

## Elastic Load Balancing:

Distribute incoming traffic across multiple targets with Elastic Load Balancing.

## Amazon GuardDuty:

Detect threats to EKS clusters with Amazon GuardDuty.

## AWS Resilience Hub:

Assess EKS cluster resiliency with AWS Resilience Hub.


## Reference Link:

https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html

