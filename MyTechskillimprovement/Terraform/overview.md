**what is Infrastructure as code ?**

- The practice of designing , provisioning, managing and operating infrastructure (Network, storage, compute clusters, load balancer etc) by writing code and applying same patterns and processes as used for other forms of source code ( Ex : software ) is called as IAC

or

- Infrastructure as code (IAC) is the managing and provisioning of infrastructure through code instead of manual process to configure devices or systems.

- IaC allows you to build, change, and manage your infrastructure in a safe, consistent, and repeatable way by defining resource configurations that you can version, reuse, and share.
Tools : Terraform, AWS Cloud Formation, Pulumi, GCP Deployment manager, Azure ARM Templates

**IAC Timeline**

![image](https://user-images.githubusercontent.com/89054489/231424700-f2e584c1-510c-403d-8d06-845427a07632.png)

**what is Configuration Management as code ?**
- Configuration as code is the practice of Managing configuration files in the repository. config files establish the parameters and settings for applications, server processing, operating systems.

Tools ⚙: Puppet, Ansible, Saltstack, Chef

Benefits of Using IAC :

- Increased speed and effeciency
- Better Documentation
- Increased Scalability
- More reusability
- Better collaboration
- Less human error
- Better Disaster Recovery
- Reduced costs
- Improved customer experience

Terraform Cloud enables infrastructure automation for provisioning, compliance, and management of any cloud, datacenter, and service.

**What IAC looking to accomplish ?**

![image](https://user-images.githubusercontent.com/89054489/231425977-aeb470ec-3842-4ecb-be08-adca68e1af15.png)


Advantages of Using Terraform :
- Terraform can manage infrastructure on multiple cloud platforms
- The human-readable configuration language helps to write infrastructure code quickly
- Terraform's state allows you to track resource changes throughout your deployment
- You can commit your configurations to version control to safely collaborate on infrastructure

- Terraform plugins called **providers** let terraform interact with cloud platforms and other services via their application programming interface (API). 
- you can Find providers for many of the platforms and services you already use in the Terraform Registry. If you don't find the provider you're looking for, you can write your own.

**standardize your deployment workflow**
- Providers define individual units of infrastructure, for example, compute instances or private networks as resources. 
- You can compose resources from different providers into reusable terraform configurations called **modules** and manage them with a consistent langage and workflow
- Terraform's configuration language is declarative, meaning that it describes the desired end-state for your infrastructure, in contrast to procedural programming languages that require step-by-step instructions to perform tasks. 
- Terraform's providers automatically calculate dependencies between resources to create or destroy them in correct order.

To deploy infrastructure with Terraform :
- **scope** - Identify the infrastructure for your project
- **Author** - Write the configuration for your infrastructure
- **Initialize** - Install the plugins Terraform needs to manage the infrasture
- **Plan** - Preview the changes Terraform will make to match your configuration
- **Apply** - Make the planned changes

![image](https://user-images.githubusercontent.com/89054489/230800921-f8a3ec23-b4b6-4213-b38d-f89fae7c40df.png)

**Track your infrastructure**
- Terraform keeps track of your real infrastructure in a state file, which acts as a source of truth for your environment. 
- Terraform uses the state file to determine the changes to make to your infrastructure so that it will match your configuration.

**collaborate**
- Terraform allows you to collaborate on your infrastructure with its remote state backends. When you use terraform cloud, you can securely share your state with your teammates, provide a stable environment for terraform to run in, and prevent race conditions when multiple people make configuration changes at once
- You can also connect terraform cloud to version control system(VCSs) like github, gitlab and others, allowing it to automatically propose infrastructure changes when you commit configuration changes to VCS. 
- This let's you manage changes to your infrastructure through version control, as you would with application code.

**NOTE :** Terraform files are saved with `.tf` extension.

**Install Terraform**

Go through the `https://developer.hashicorp.com/terraform/downloads` web page and select your os and then follow further steps accordingly to install terraform on your system

![image](https://user-images.githubusercontent.com/89054489/230801050-7a993150-66d3-4188-ac49-b7e58a970e6f.png)

To verify our installation use `terraform version`

![image](https://user-images.githubusercontent.com/89054489/230801185-a418764f-b9e1-4d91-8b82-982ca583875d.png)

**Provisioning NGINX server using docker with terraform on linux** 

First, we need to make sure docker and terraform installed in our system. To verify docker installation use `docker -v` and to verify terraform installation use `terraform version`

Create a directory named `learn-terraform-docker-container`
- This working directory is the storage place of the  the configuration files that you write to describe the infrastructure you want Terraform to create and manage. When you initialize and apply the configuration here, Terraform uses this directory to store required plugins, modules (pre-written configurations), and information about the real infrastructure it created.

Navigate into the working directory

In the working directory, create a file called `main.tf`

![image](https://user-images.githubusercontent.com/89054489/230802131-9cd41514-548b-4197-bcfe-153201fba11b.png)

Inside `main.tf`, we need to write the below code

![image](https://user-images.githubusercontent.com/89054489/230802098-85b2de26-893a-4d6a-954b-1cdac4d69d96.png)

provision the NGINX server container with `apply`. When terraform asks you to confirm type `yes` and press `ENTER`

![image](https://user-images.githubusercontent.com/89054489/230802232-3ae77a38-6976-446d-807f-d282cf87296e.png)

Verify the existence of the NGINX container by visiting `http://localhost:8000` in your web browser or running `docker ps` to see the container.

![image](https://user-images.githubusercontent.com/89054489/230802265-54f6ef88-a9da-494c-9797-06424190e241.png)

![image](https://user-images.githubusercontent.com/89054489/230802392-e89332fc-72de-49de-af81-a1a44ff7b579.png)

To stop container, run `terraform destroy`

![image](https://user-images.githubusercontent.com/89054489/230802487-cd1434c7-49a3-443c-b8cf-6fb395e40f01.png)

Now, we have successfully provisioned and destroyed an NGINX webserver with Terraform.

For installation guide, visit `https://www.terraform.io/downloads`












