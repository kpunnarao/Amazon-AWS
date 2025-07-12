# Compute and Application Hosting:

## Introduction to the Module:

* Welcome to Section Compute and Application Hosting, a critical component of building dynamic and scalable solutions on AWS. 

* This module focuses on the diverse range of compute services and application hosting options available in the AWS Cloud. 

* Understanding these services is paramount for selecting the right compute strategy, optimizing performance, managing costs, and ensuring the high availability of your applications.

* In this module, we will explore everything from virtual servers to serverless functions, container orchestration, and platform-as-a-service offerings. 

* We'll delve into the nuances of each service, helping you determine when to use which, how to scale your applications effectively, and how to manage the underlying infrastructure (or let AWS manage it for you). 

* By the end of this module, you will be well-equipped to design and implement compute solutions that meet various architectural requirements.

## Key AWS Services for Compute and Application Hosting:

This section provides a brief introduction to the essential AWS services covered in this module, which are vital for designing and implementing compute and application hosting solutions.

<hr style="border: 0; height: 3px; background: #0078D4; margin-top: 12px; margin-bottom: 12px;">

### Amazon Elastic Compute Cloud (EC2):

* Amazon EC2 provides resizable compute capacity in the cloud. 

* It allows you to launch virtual servers (instances) with various operating systems, storage options, and network configurations. 

* EC2 gives you granular control over your computing resources, making it a foundational service for many AWS architectures.

#### Key Concepts:

* **Instances:** Virtual servers that run your applications. You choose instance types based on CPU, memory, storage, and networking capacity.

* **Amazon Machine Images (AMIs):** Templates that contain the software configuration (operating system, application server, applications) required to launch your instance.

* **Elastic Block Store (EBS):** Persistent block-level storage volumes for EC2 instances, providing high-performance and durable storage.

* **Security Groups:** Act as virtual firewalls to control inbound and outbound traffic for your instances.

* **Key Pairs:** Used to securely connect to your EC2 instances.

* **Instance Types:** Optimized for different workloads (e.g., General Purpose, Compute Optimized, Memory Optimized, Storage Optimized, GPU Instances).

* **Pricing Models:** On-Demand, Reserved Instances, Spot Instances, Savings Plans.

* **Auto Scaling:** Automatically adjusts the number of EC2 instances in your application based on defined policies and demand.

<hr style="border: 0; height: 3px; background: #0078D4; margin-top: 12px; margin-bottom: 12px;">

### AWS Lambda:

* AWS Lambda is a serverless, event-driven compute service that lets you run code without provisioning or managing servers. 

* You upload your code, and Lambda automatically handles the underlying infrastructure, scaling, and high availability. 

* You only pay for the compute time consumed when your code is running.

#### Key Concepts:

* **Functions:** The units of code you upload to Lambda.

* **Event-Driven:** Lambda functions are triggered by events from other AWS services (e.g., S3, DynamoDB, API Gateway) or custom events.

* **Stateless:** Functions should be designed to be stateless, as Lambda can invoke multiple instances of your function concurrently.

* **Concurrency:** Lambda can automatically scale out to handle a large number of concurrent executions.

* **Integrations:** Deeply integrated with a wide range of AWS services for various use cases.

* **Billing:** Billed per invocation and duration of execution, in 1ms increments.

<hr style="border: 0; height: 3px; background: #0078D4; margin-top: 12px; margin-bottom: 12px;">

### Amazon Elastic Container Service (ECS):

* Amazon ECS is a highly scalable, high-performance container orchestration service that supports Docker containers. 

* It allows you to easily run, stop, and manage Docker containers on a cluster of Amazon EC2 instances or using AWS Fargate (serverless option).

#### Key Concepts:

* **Clusters:** Logical groupings of tasks or container instances.

* **Task Definitions:** Blueprints for your application, specifying the Docker image, CPU, memory, and networking settings for your containers.

* **Tasks:** An instance of a task definition running on a cluster.

* **Services:** Define how many tasks should run, how they are launched, and how they interact with load balancers.

**Launch Types:**

* **EC2 Launch Type:** You manage the EC2 instances that host your containers.

* **Fargate Launch Type:** Serverless compute for containers; AWS manages the underlying infrastructure.

* **Registries:** Integrate with Amazon Elastic Container Registry (ECR) for storing Docker images.

<hr style="border: 0; height: 3px; background: #0078D4; margin-top: 12px; margin-bottom: 12px;">

### Amazon Elastic Kubernetes Service (EKS):

* Amazon EKS is a fully managed Kubernetes service that makes it easy to deploy, manage, and scale containerized applications using Kubernetes on AWS. 

* EKS handles the heavy lifting of managing the Kubernetes control plane, allowing you to focus on your applications.

#### Key Concepts:

* **Kubernetes Control Plane:** Managed by AWS, providing the API server, etcd, scheduler, and controller manager.

* **Worker Nodes:** EC2 instances (or Fargate) that run your containerized applications (pods).

* **Pods:** The smallest deployable units in Kubernetes, containing one or more containers.

* **Deployments:** Define how to deploy and update applications.

* **Services:** Define a logical set of Pods and a policy by which to access them.

* **Integrations:** Deeply integrated with AWS networking (VPC CNI), IAM, and other services.

<hr style="border: 0; height: 3px; background: #0078D4; margin-top: 12px; margin-bottom: 12px;">

### AWS Elastic Beanstalk:

* AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with various programming languages (e.g., Java, .NET, PHP, Node.js, Python, Ruby, Go, Docker) on familiar servers. 

* Elastic Beanstalk handles the infrastructure provisioning and management, allowing you to focus on your code.

#### Key Concepts:

* **Managed Platform:** AWS provisions and manages the underlying EC2 instances, load balancers, Auto Scaling groups, and other resources.

* **Environments:** Specific deployments of your application (e.g., development, staging, production).

* **Versions:** Different iterations of your application code.

* **Configuration:** You can customize the environment and underlying resources without directly managing them.

* **Automatic Deployment:** Simplifies deployment by handling capacity provisioning, load balancing, auto-scaling, and application health monitoring.

<hr style="border: 0; height: 3px; background: #0078D4; margin-top: 12px; margin-bottom: 12px;">

### Amazon Simple Storage Service (S3) for Static Website Hosting:

* While primarily a storage service, Amazon S3 can be used as a cost-effective and highly available solution for hosting static websites. 

* It's ideal for websites that don't require server-side processing, such as single-page applications, blogs, or portfolios.

#### Key Concepts:

* **Buckets:** Containers for your static website files (HTML, CSS, JavaScript, images).

* **Public Access:** Configure your S3 bucket to allow public read access for website content.

* **Website Endpoint:** S3 provides a unique endpoint for your website, accessible via a web browser.

* **Custom Domains:** You can use Route 53 to point your custom domain to your S3 static website endpoint.

* **No Server Management:** No need to manage web servers; S3 handles all the hosting infrastructure.

<hr style="border: 0; height: 3px; background: #0078D4; margin-top: 12px; margin-bottom: 12px;">

### Amazon Simple Queue Service (SQS):

* Amazon SQS is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications. 

* It allows messages to be sent, stored, and received between software components without requiring them to be simultaneously available.

#### Key Concepts:

* **Standard Queues:** Offer maximum throughput, best-effort ordering, and at-least-once message delivery.

* **FIFO (First-In-First-Out) Queues:** Guarantee that messages are processed exactly once, in the exact order they are sent.

* **Message Retention:** Messages are retained in the queue for a configurable period.

* **Visibility Timeout:** Prevents multiple consumers from processing the same message simultaneously.

* **Decoupling:** Enables asynchronous communication between application components, improving fault tolerance and scalability.

<hr style="border: 0; height: 3px; background: #0078D4; margin-top: 12px; margin-bottom: 12px;">

### Amazon Simple Notification Service (SNS):

* Amazon SNS is a highly available, durable, secure, and fully managed publish/subscribe messaging service that enables you to fan out messages to a large number of subscribers, including other AWS services, email, SMS, and HTTP endpoints.

#### Key Concepts:

* **Topics:** Logical access points that act as communication channels. Publishers send messages to topics, and subscribers receive messages published to those topics.

* **Publishers:** The source that sends messages to a topic.

* **Subscribers:** Endpoints that receive messages from a topic (e.g., SQS queues, Lambda functions, email addresses, mobile push notifications, HTTP endpoints).

* **Fan-out:** A single message published to a topic can be delivered to multiple subscribers simultaneously.

* **Decoupling:** Enables loosely coupled, event-driven architectures.

<hr style="border: 0; height: 3px; background: #0078D4; margin-top: 12px; margin-bottom: 12px;">