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

Reference Link:

https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html

