


Advantages of cloud computing :
1. Trade upfront expense for variable expense
2. stop spending money to run and maintain datacenters
3. stop guessing capacity
4. Benefit from massive economies of scale
5. Increase speed and agility
6. Go global in minutes


cloud computing models :

1. Infrastructure as a service ( IAAS )
2. Platform as a service ( PAAS )
3. Software as a service ( SAAS )

1. Infrastastructure as a service ( IAAS ) :
- It contains the basic building blocks for cloud IT. It typically provides access to networking features. Computers (virtual or on dedicated hardware ) and data storage space.
- Infrastructure as a service provides the highest level of flexibility and management control over your IT resources.

EX : amazon EC2, Amazon S3, Amazon RDS, Amazon Route 53 are considered as IAAS services 

2. Platform as a service ( PAAS ) :
- It removes the need for organizations to manage the underlying infrastructure ( usually hardware and operating systems ).
- They can focus on the deployment and management of applications.
- These tools give developers the ability to be more effecient because they don't need to worry about resource procurement, capacity planning, software maintainance, and patching.

EX : AWS Elastic Beanstalk . These service is used for quickly deploying and scaling web applications.

Software as a service ( SAAS ) ;
- It is a completed software product that the service provider runs and manages with a SAAS offering. you do not have to think about how the service is maintained or how the underlying infrastructure is managed. 
- you only need to think about how you will use that particular piece of software

EX: video meeting sites, Email sites, file sharing sites and messaging apps

Deployment strategies include :
- Cloud
- Hybrid
- On-premises

1. cloud : In a cloud based deployment model, you can migrate existing applications to the cloud, or you can design and build new applicatioons in the cloud.
- you can build those applications on low-level infrastructure that requires your IT staff to manage them.
- Alternatively, You can build them by using higher-level service that reduce the management, architecting, and scaling requirements of the core infrastructure.

EX: a company create an application that consists of virtual servers, databases, and networking components that are fully based on the cloud.

2. Hybrid :
- cloud based resources are connected to on-premises infrastructure.
- You can integrate cloud-based resources with legacy IT applications. You might want to use this approach in a number of situations.
- EX: you have a legacy applications that are better maintained on premises, or government regulations require your business to keep certain records on premises.

For suppose that a company want to use cloud service that can automate batch data processing and analytics.
However, the company has several legacy applications that are more suitable on premises and will not migrated to the cloud with a hybrid deployment, the company would be able to keep the legacy applications on premises while benefiting from the data and analytics service that run in the cloud.

3. On-Premises : It is also known as private cloud deployment. In these model resources are deployed on premises by using virtualization and resource management tools. Increase resource utilization by using application management and virtualization technologies.

EX: you might have applications that run on technology that is fully kept in your on-premises data center. Though this model is much like legacy IT infrastructure, its incorporation of applications management and virtualization technologies helps to increase resource utilization.


AWS Global Infrastructure

- AWS has an extensive, reliable and secure global cloud infrastructure with over 175 services for a wide range of use cases. These services are built on a robust infrastructure where the customer and AWS share the responsibilities for programming and security. 
![image](https://user-images.githubusercontent.com/89054489/236588662-114f82c6-ba9a-449b-a075-bb1e8018e7a4.png)

AWS Regions :
- AWS has  the concept of a Region, which is a physical location around the world where data centers are clustered together.
- A group of logical datacenters is called Availability Zone
- Each AWS Region consists of multiple, isolated and physically separated Availability Zones within a geographical area.

Availability Zone :
- An availability zone is a zoned area within a region that can harbor one or more data centers (typically three ) availability zones house all the hardware devices that AWS offers
- with their own power infrastructure, the AZ are physically separated by a meaningful distance ( upto 100 to 60 miles ) from any other availability zone in the Region
- AZ are interconnected with high-bandwith, low-latency networking, to provide low-latency networking between zones that is sufficient to accomplish synchronous replication ( same time replication )

Edge locations :
- Edge locations are connected to AWS regions through the AWS network across the globe. They link with tens of thousands of networks for improved origin fetches and dynamic content acceleration
- Edge locations cache copies of your content for faster delivery to users at any location. They support AWS services like Amazon route 53 and Amazon CloudFront
- AWS has over 200 edge locations that are placed in 90 cities, across 47 countries.

AWS Services :
- AWS offers a broad set of global cloud based products including compute, storage, databases, analytics, networking, mobile, developer tools, management tools, security and enterprise applications. These services help you build elastic, agile, resilient architectures. 

** Monolithic Architecture**
- Applications are made up of multiple components. These components communicate with eachother to transmit data to fill request and keep application running. 
- Tightly coupling of components in the application is called as Monolithic applications.
- If single component failed, The whole application will fail.

** Microservices Architecture **
- To make applications highly available we need to design our applications on microservices architecture.
- Having loose coupling among components in the application is called as **Microservices Architecture**
- Even if a single components failed, the application will run successfully.

AWS has three types of services. They are 
<br>1. Managed Services<br>2. Fully-Managed Services <br> 3. Serverless Service

1. Managed Service :
- A managed Service is a way to describe the service that requires you to manage infrastructure management tasks like patching, backup and repair.
- These services grant you virtual access to the underlying operating system and servers. 
- With Managed services, you are responsible for scaling and building for high availability.

2. Fully Managed Service :
- A fully Managed Service is a way to describe the services that automate infrastructure management tasks that AWS handles like patching, backup and repair. 
- These services do not grant you any virtual access to the underlying operating system or servers
- With a fully managed service, you are still responsible for scaling and builidng for high availability.

3. Serverless Services :
- Serverless is a way to describe the services, practices, and strategies that you can use to build more agile applications. 
- In this way, you can innovate and respond to change faster
- With serverless services, AWS handles infrastructure management tasks like capacity provisioning and patching so that you can focus on building applications that serve customers.
- Serverless Services come with automatic scaling, build-in-high availability and pay for value billling model.

![image](https://user-images.githubusercontent.com/89054489/236654443-56b59a21-56c0-467d-99a0-61ec32a58941.png)

