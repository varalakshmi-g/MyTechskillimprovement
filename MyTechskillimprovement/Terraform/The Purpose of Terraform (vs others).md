**2a. Explain multi-cloud and provider-agnostic benefits**

- First, lets learn some of the basics here


**cloud native :**
- As the name suggests it helps to build and run applications by taking advantage of services and components tied to the Cloud Service Provider itself. For ex – using CloudWatch for monitoring services with AWS, Azure Monitoring services for Azure & more.
- In short, Building and running applications by using services and components tied to cloud .

Pros of cloud native Architecture:
- scalability
- Resilence
- Performance

Cons of cloud native architecture:
- Service provider lock-in and limited flexibility for growth:
-  Security & Data Management across network
-  Monitoring & Management challenges: 

**cloud agnostic :** 
- It is referred to applications and workloads that can be moved seamlessly between cloud platforms—without being bound by operating dependencies. Cloud agnostic tools can work on any cloud providers/platform.
- In short, Cloud-Agnostic refers to the freedom of choice of the cloud provider

Pros of Cloud Agnostic architecture:
- Limitless portability:
- Consistent performance:
- Avoid lock-in

Cons of Cloud Agnostic architecture :
- High upfront capital cost
- Cloud agnostic applications may not take advantage of all platform features

**Multi-cloud :**
- multi-cloud refers to a multiplicity of hosting arrangements.
- Multicloud refers to using services from more than one public cloud provider at the same time. A multicloud environment allows your cloud environments to be private, public, or a combination of both.

The primary goal of a multicloud strategy is to give you flexibility to operate with the best computing environment for each workload.

Benefits of Multicloud :
- Best of each cloud
- Avoid vendor lock-in
- Cost efficiency

Challenges of multicloud
- Increased management complexity
- Maintaining consistent security
- Integrating software environments
- Difficulty with achieving consistent performance and reliability across clouds


**2b. Explain the benefits of state**

Terraform is a stateful application. This means that it keeps track of everything it builds in your cloud environments so that if you need to change something or delete something later, Terraform will know what it built, and it can go back and make those changes for you.
These state is stored in a state file.

Terraform records information about what infrastructure it created in a **Terraform state file**. By default, when you run Terraform in the folder `/foo/bar`, it will create the file `/foo/bar/terraform.tfstate.`

![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/8be5b6a3-2cbc-4fbf-b1e9-523b5900708c)

