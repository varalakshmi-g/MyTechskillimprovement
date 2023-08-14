![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/6461284f-f8e1-414b-92d3-fbcf33dc8fbf)

	--> One of the key principles of this methodology ( AGILE ) was delivering working software frequently. The focus moved to releasing incremental software, rather than big bang waterfall releases which took months and years.
	
	Continuous Integration :
	
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/fb4d3f72-ce24-458f-9dab-698371558987)

	--> CI is an agile engineering practice originating from the extreme programming methodology. It primarily focuses on the continuous build and test for every change commited to the version control system by the developers
	
	--> CI requires the following :
	
	Version control system :
		- It stores all the source code checked in by the teams, and acts as the single source of truth.
	Automated build and unit test
		It is not sufficient if the code written by a developer works only on his/her machine. Every commit that makes it to the version control system should be built and tested by an independent continuous integration server.
	Feedback
		Developers should get feedback on their commits. Anytime a developer’s change breaks the build, they can take the necessary action (example: email notifications).
	Agreement on ways of working :
		It is important that everyone on the team follows the practice of checking-in incremental changes rather than waiting till they are fully developed. Their priority should be to fix any build issues that may arise with the checked-in code.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/75b8e2a9-1dfd-49d0-9141-694a7e9a8f93)

		
	Continuous Delivery
	- Continuous Delivery is a logical extension of Continuous Integration. While Continuous Integration lets you automate the software build and test process, Continuous Delivery automates the full application delivery process by taking any change in code (new features, bug fixes, etc.) all the way from development (code commit) to deployment (to environments such as staging and production). It ensures that you are able to release new changes to your customers quickly in a reliable and repeatable manner.

Continuous Delivery is a software development discipline where you build software in such a way that the software can be released to production at any time.

You are doing CD when :  

>> your software is deployable throughout its lifecycle
>> your team prioritizes keeping the software deployable over working on new features
>> Anybody can get fast, automated feedback on the production readiness of their systems anytime somebody makes a change to them.
>> You can perform push-button deployments of any version of the  software to any environment on demand.

To achieve CD we need :
>>  A close, collaborative working culture among all the people involved in the delivery ( often referred to as a Devops Culture )
>> Extensive automation of all possible parts of delivery process, usually using  a deployment pipeline.

---- > Incorporating Continuous Delivery practices will make your overall release process painless, reduce the time to market for new features, and increase the overall quality of software thereby leading to greater customer satisfaction. It can also significantly reduce your software development costs as your teams will prioritize releasing new features over debugging defects.

Continuous Deployment :

>> Continuous Deployment, however, is an automated way of deploying your releases to production. You need to be doing continuous delivery in order to be able to perform automated deployment. Companies like Netflix, Amazon, Google, and Facebook automatically deploy to production multiple times a day.

![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/783810a3-3ab1-479d-98b0-e4ea7a56934a)


	Deployment Pipeline :
	
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/20dac3f6-a3ae-4432-8a07-5d93fa2624f0)
	
	
	Deployment pipelines (or Continuous Delivery pipelines) are the cornerstone of Continuous Delivery as they automate all the stages (build, test, release, etc.) of your software delivery process.
	
	There are numerous benefits to using Continuous Deployment pipelines. An automated pipeline allows all stakeholders to monitor the progress, eliminates the overhead of all the manual work, provides quick feedback, and more importantly builds confidence on the code quality.
	
	 
	The deployment pipeline run starts with a developer committing source code change into a version control repository. The CI server detects the new commit, compiles the code, and runs unit tests. The next stage is deploying the artifacts (files generated from a build) to staging or a feature test environment where you run additional functional, regression, and acceptance tests. Once all the tests are successful, you are ready to deploy into production. In case of failure during any stage, the workflow stops and an immediate feedback is sent back to the developer.
	
	Tools for deployment pipeline : 
	
	In order to automate the various stages of your deployment pipeline, you will need multiple tools. For example:
	• A version control system such as Git to store your source code
	• A Continuous Integration (CI) tool such as Jenkins to run automated builds
	• Test frameworks such as xUnit, Selenium, etc., to run various test suites
	• A binary repository such as Artifactory to store build artifacts
	• Configuration management tools such as Ansible
	• A single dashboard to make the progress visible to everyone
	• Frequent feedback in the form of emails, or Slack notifications.
	
	
	
	CI/CD Tools :
	
	Jenkins, cloudbees, AWS Codepipeline, Azure Pipelines, Circle CI, Atlassian Bamboo, Bitbucket Pipelines, Github actions, Git lab CI/CD, Travis CI
	
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/580c3329-c715-432e-bc15-bd7fadb6cc13)

	**JENKINS**
	# what is jenkins ?
- jenkins is an opensource, continuous integration tool. It is cross platform and can be used on windows, linux, mac os and solarisis environment. It can be used to automate all sorts of tasks such as building, testing, and deploying software.
- It is mainly used for automation purpose.

## important features of jenkins :
- jenkins is easy to install either using direct installation through .exe file or through .war file to deploy using application server.
- jenkins keep track of all changes done in repository for future references
- it is very easy to configure jenkins inorder to send email for every build status
- jenkins can be configured to run the automation test build on TestNG after every project build
- jenkins can be configured to distribute the build on multiple machines
- 3 rd party plugins can be configured with jenkins inorder to use additional features.

### example 
- the jenkins server checks the source code repository at regular interval of time.
- when the developer commits the code to the source code repository. the jenkins server detects the changes that have occured in the source code repository.
- jenkins will detect and pull the changes and will start preparing new build
- if the build gets failed, the developer will be communicated about the failure of the build so that they can check the code at their end.
- if the build is successful. jenkins will deploy the build in test server.
- after smoke testing, the development team is communicated about the successful deployment of the code to test server.
- jenkins will continue to check the source code repository for any changes make in the source code and keeps on repeating the entire process.


## advantages of jenkins

jenkins is used for continuous integration of the software. Below are some of the benifits of using jenkins.
- it is an opensource and easy to install. can be plugged in with more than 1000 plugins.
- helps to achieve continuous integration for agile projects
- It helps to implement the test driver deployment
- It can be integrated with LDAP mail server to provide automatic build report notification.
- It helps to detect the defects easily in the development cycle.
- It is free of cost.
- portable for all major platforms, since it is written in java
- if a defect is detected, the respective developer can quickly fix the detect.

![image](https://user-images.githubusercontent.com/89054489/218329642-d40b24ea-e2ae-4efa-9d5c-b6b64dd3375d.png)

dev1-> git repository = commit changes to the source code<br>
under jenkins server = jenkins check the shared repository at periodic intervals and every check in is pulled and then build.<br>
under selenium = Jenkins deploys the build application on the test server.<br>
under production server = The build application is then deployed to the test server.

![image](https://user-images.githubusercontent.com/89054489/218328249-24244da3-6bc3-41fc-83cc-4003722d03ce.png)

**3. pre-requisite for using jenkins :**
- **Source code repository:** a source code repository is required which can be accessed from jenkins ex: git.
- **Build script:** working build script checked into the repository e.g; Maven

**4. Useful plugin in jenkins:**
- Maven Project
- Git
- Amazon EC2
- HTML Publisher
- Copy artifact
- Join
- Green Balls

![image](https://user-images.githubusercontent.com/89054489/218331290-3174b56d-272c-49ab-b8b5-f5f8385d2f5f.png)

**4. Commands used to start with Jenkins:**
- To start jenkins manually open console/command line, then go to the jenkins installation. over there below commands are used.

> To start jenkins: jenkins.exe start
> To stop jenkins: jenkins.exe stop
> To restart jenkins: jenkins.exe restart

Below screen will appear on successful start of the jenkins tool:

![image](https://user-images.githubusercontent.com/89054489/218332197-227b48d0-4756-443e-8d6e-bde56a93993b.png)

**4.2 setup jenkins job:**
- Go to jenkins top page, select "new job" then choose "Build a free-style software project" now you can define the elements of this freestyle job.
  >> optional SCM , such as CVS or subversion where the source code resides on the local machine.
  >> optional triggers to control when jenkins will perform the builds
  >> Build script that performs the build e.g; ant, maven, shell script, batch file etc
  >> collect information out if the build e.g; archiving the artifacts and/or recording javadoc and text results. This is optional setup.
  >> Notify other people/systems with the build result by sending emails, IMs, updating issue tracker etc. This is also optional step


  **Backup and job:**
  - periodically copy your JENKINS_HOME directory. This directory contains all the build job configurations. slave node configuration, and the build history. To create a backup just copy this directory.

  **Secure Jenkins:**
  
  Below are the few ways jenkins can be secured

- Ensure global security on. The teams are distributed globally.
- Jenkins to be integrated with company's user directory with appropriate user plugin.
- Ensure that the matrix/project matrix is enabled to fine tune access
- Automate the process of setting rights/privileges in jenkins with custom version controlled script
- Limit physical access to jenkins data/folders
- periodically run security audits on same.

**6. Relationship between Hudson and Jenkins ?**
- Hudson was the previous name of current jenkins. After some issues the project name is changed to jenkins.
**Difference between Maven, Ant and Jenkins**
- Maven is automation build tool. It is written in java language. It is used to build projects written in almost all languages like c#, Ruby etc. Maven can be used to manage processes like builds, documenation, reporting, dependencies , SCMs, releases, distribution and mailing lists.

![image](https://user-images.githubusercontent.com/89054489/218349537-ffb0bf8f-e0ff-41a0-9c8d-3a598c45e1e7.png)

- Ant is a java based build tool. This tool is developed by Apache Software Foundation. Ant's build file is easy to understand and are written in XML. This is used to automate the build and deployment process. It can be executed from the command line. It can be integrated with free IDE's

- Jenkins is a continuous integration tool written in java language. It is an open source tool and used for continuous integration. It helps with the continuous delivery of the software.

**SCM tools Jenkins support**

- AccuRev
- CVs
- Subversion
- Git
- Mercurial
- Perforce
- ClearCase
- RTC(Rational Team Concert)

- Jenkins is mainly integrated with :
> version control system like GIT, SVN
> Build tools like Apache and Maven.



















![image](https://user-images.githubusercontent.com/89054489/218289268-58f48bc3-96e7-4db7-b569-64200d282b6a.png)

![image](https://user-images.githubusercontent.com/89054489/218289287-f5b4c9f4-fbf4-4358-a657-84ada32435cc.png)

![image](https://user-images.githubusercontent.com/89054489/218289304-95f9b010-e013-478e-b56e-38df979a396a.png)

![image](https://user-images.githubusercontent.com/89054489/218289349-d400d797-57ce-462c-a43d-8cc5ddf1a105.png)

![image](https://user-images.githubusercontent.com/89054489/218289371-1d90debc-0240-40ca-825f-96d3ce61e761.png)

![image](https://user-images.githubusercontent.com/89054489/218289389-6afe46fc-5b46-4834-9abd-556b4e2ac788.png)

![image](https://user-images.githubusercontent.com/89054489/218289408-d2668b8e-1830-4f7f-8396-97db0caad191.png)

![image](https://user-images.githubusercontent.com/89054489/218289433-405af164-4781-43fa-af1f-1621e5793ceb.png)

![image](https://user-images.githubusercontent.com/89054489/218289447-237b3233-0ca1-458c-9035-3b9b9046ddd7.png)

![image](https://user-images.githubusercontent.com/89054489/218289477-ad29cd0c-d7fa-45c1-9292-e09a0b5bb720.png)

![image](https://user-images.githubusercontent.com/89054489/218289248-4b69cba5-9a6a-49aa-8c4a-f15d03b2d0cb.png)

![image](https://user-images.githubusercontent.com/89054489/218289498-e31cc2b5-ec37-4ff2-a20e-82ef62bb332e.png)

# jenkins from linkedin learning

## Introduction
- In software development and system administration automation saves time and helps you work more effeciently.
- Jenkins is the framework that which we can use to manage all sorts of automation including software builds,application testing deployments and much more

why to choose jenkins ?
- Ease of use
    - intuitive web interface
    - easy to navigate
    - Documentation and examples included
- Free and Open Source
    - free to install and use
    - open source
- Extensibility
    - Plugins add functionality
    - New features can be developed
- Community
    - Jenkins users around the world
    - Conferences and events
## Key terminologies
#### Project or job
- A user configured description of the work that jenkins will manage
- job and project used interchangeably
#### Build
- It is what happens when jenkins runs through the instructions in a job[one run of a project]
#### Build step
- It should be checking out source code or running a script. Jobs can contain as many build steps as needed [A task inside a project]
#### Build Trigger
- Trigger is the event that starts the build. Builds can be started manually or automatically [Criteria for starting a build]

#### plugins
- A software package that extends jenkins core functionality.
- Plugins can enhance jenkins functionality in many ways like adding features to the interface or defining new types of build steps.

- Jenkins is a web-based application that can be installed on any number of systems from laptop to servers.

### Requirements
#### Hardware Requirements
- 256 MB RAM
- 1 GB disk space
#### Software Requrirements
- java 11
- Java Runtime Environment
- Java Development Kit

### Install jenkins on Windows
see in the above steps

Now,let's create a new hello world jemkins freestyle project.

![image](https://user-images.githubusercontent.com/89054489/224275933-ed1b4141-60bd-4acc-95a1-b2f1a9337168.png)

![image](https://user-images.githubusercontent.com/89054489/224276523-fb808924-4302-43b4-8705-caab27dee1f0.png)

![image](https://user-images.githubusercontent.com/89054489/224277692-2dd51c95-52da-4823-97c9-78b7eebb19f6.png)

![image](https://user-images.githubusercontent.com/89054489/224278150-67360992-101b-47f8-8530-6c0af7e82684.png)


![image](https://user-images.githubusercontent.com/89054489/224278893-2fdd41f2-2a09-466a-9c9d-f2350c9da875.png)


![image](https://user-images.githubusercontent.com/89054489/224279209-cb0eef93-8853-4201-847d-7d729239b5bd.png)


![image](https://user-images.githubusercontent.com/89054489/224279594-c39d11e2-6165-4d7d-aeef-90300a6e917c.png)

![image](https://user-images.githubusercontent.com/89054489/224280019-404e05e0-639f-43a6-b8c4-a95a2ca9acdf.png)

Congratulations, we have created our first jenkins job successfully. With this motivation let's goooo..

Now, let's explore about the different types of jobs in jenkins.
1. Freestyle project
2. pipeline
3. Multiconfiguration project
4. Folder
5. Github Organisations
6. Multibranch pipeline

**1.Freestyle project**
- It is the most commonly used job
- It freely controls the way jenkins manages the tasks that you want to automate
  
**2.Pipeline**
- pipeline jobs are useful for projects that are more complex than freestyle jobs
- for example, pipelines can build steps in parallel, use logic to skip steps and even use different compute platforms for different steps.
  
**3.Multi-configuration project**
- It is useful when you have multiple jobs that do the same thing but for different combinations of parameters. Instead of creating many jobs for each set of parameters, you can use the multi-configuration project to create one job that applies the parameters for you.
  
**4.Folder**
- it isn't a job. Jenkins uses folders to group things together.
  
**5.Github Organisations**
- Github Organisation jobs are configured to scan github repositories for files that jenkins uses to configure jobs automatically.
  
**6.Multibranch pipeline**
- It can be used to configure jobs for different branches belonging to same repo.

5 & 6 job types are especially suited for working with code repositories. 

Let's talk about the configuration page 
The first option/button is General

![image](https://user-images.githubusercontent.com/89054489/224300894-1c84ba05-48a1-47c8-92c4-27c3fab1c3a1.png)

![image](https://user-images.githubusercontent.com/89054489/224301223-94b35623-2073-40ee-a112-b2de77b1f8cb.png)

**source code management**

![image](https://user-images.githubusercontent.com/89054489/224302137-cafb7877-7ad5-4bf3-9c16-3158fd3e3ecd.png)

**Build triggers**
![image](https://user-images.githubusercontent.com/89054489/224302903-c2d7d53e-ef08-469f-b7f2-1f1d196e9151.png)

![image](https://user-images.githubusercontent.com/89054489/224303119-df323d88-505a-4b8c-bfed-8b60ffc5d7cc.png)

![image](https://user-images.githubusercontent.com/89054489/224303220-4e233c9d-6f0f-4ecc-9b66-98eeb58ca629.png)

![image](https://user-images.githubusercontent.com/89054489/224303425-ccfe7bee-59df-4906-9bbe-fc21d63dbf00.png)

![image](https://user-images.githubusercontent.com/89054489/224303735-203cf2e9-63e8-42ec-b701-1c7b49a4b3dd.png)

**Build Environment**
![image](https://user-images.githubusercontent.com/89054489/224305260-dd3273be-da5d-4a38-aa54-abed4e02e93c.png)

![image](https://user-images.githubusercontent.com/89054489/224305373-e5aef49d-5acf-4fc1-ad96-580d5a1a2dcb.png)

![image](https://user-images.githubusercontent.com/89054489/224305517-91c3c181-bdd3-4e46-b57a-02cf45ad8cfd.png)

![image](https://user-images.githubusercontent.com/89054489/224305723-5cf79fa3-f6fc-4067-9da4-8a35ab930462.png)

**Build Steps**

![image](https://user-images.githubusercontent.com/89054489/224306989-64221a27-3dfc-415b-b7cd-fb659b895a18.png)

**Post-build Actions**

![image](https://user-images.githubusercontent.com/89054489/224307253-277beeff-e33a-4713-8737-176e9e62b20a.png)

**Run and monitor jobs**

- Build id is a unique number that lets jenkins organise the builds associated with a job.

- ![image](https://user-images.githubusercontent.com/89054489/224312133-63f41b4a-4648-4056-b4ff-d3384ebfc7c2.png)


- Most jenkins jobs will create some sort of product at the end of the each build.It could be a compiled executable like exe. An archive like jar file or a report in the text file. These products are refered to as **artifacts** .


**Scheduling jobs**
- Sometimes, we need to do our jobs automatically. one of the ways we can do that is by running jobs on schedule.
- Running jobs on schedule helps with automating things
like updating software, Monitoring system details and downloading and processing data.

**cron**
- A time based job scheduler in unix-like operating systems.
- Jenkins uses a format simmilar to cron for scheduling jobs
- Execution times are defined by an expression representing the schedule.
**Jenkins Schedular format**
- The order of jenkins schedular format from left to right are *****
Minutes(0-59),Hour(0-23)
Day of Month(1-31)
Month(1-12 or Jan-Dec)
Day of the week (0-6 or sun-sat)

**Jenkins Scheduler Aliases**
- use H for hashed values to spread out jobs around the desired time.
- use simple aliases for general times
@hourly
@daily
@midnight
@weekly
@monthly
@annually

![image](https://user-images.githubusercontent.com/89054489/224355917-ec2d4532-0ee6-4d74-b309-48373c852fb5.png)

Time Zones
- Time Zones are relative to the server
- Many servers use the UTC timezone
- plan your schdule accordingly

**views and folders**
- Views provide a way of associating jobs on the dashboard and displaying them together.
- you can think of view as a type of filter that looks at all of the jobs and displays particular jobs based on the criteria that you define.
- using the view, you limit the jobs that are displayed to only the ones you want to see at that time.

**folders:**
- folders group things together
- folders contain jobs, views, and other folders
- folders also contain completely separate namespaces from other folders, allowing you to create hierarchies that have simmilar characteristics,like jobs with the same name, for example.

**Pipelines**
- jenkins allows us to configure jobs as code. These types of jobs are called **pipelines**
- A pipeline written into a text file is called as jenkins file.
- can be versioned in a code repository.
- configure jenkins jobs
- Contain stages and steps
**pipeline stages**

pipeline{

    stages{
    
        stage('Build'){
	
        }
	
        stage('Test'){

        }
        stage('Deploy'){

        }
    }
}

- stages are sections of the pipeline
- steps are the actions taken in each stage.

- The process of automating the build, test step processes by using any tool like jenkins is called **continuous integgration**
- Usage of automation in the release and deploy stages in Devops life cycle is called as **continuous delivery**
- If the end to end process i.e; from plan to monitor is completely automated then it is called as **Continuous deployment**

##### continuous integration
- It is often called as CI
- It involves two steps they are 1. Build 2. Test
<br>1. Build : Create artifacts and reports
<br>2. Check features for correctness

- The main goal of CI is to find and resolve problems early in the development cycle.

- The artifact generated here in CI process can be a docker image,java war/jar file , a windows executable or any other sort of software package.

##### Continuous Delivery and Deployment
- It involves 2 steps
1. Release  : Make artifacts available.
2. Deploy   : Check features for correctness. 

- These stages take an artifact and make it available for use or actually put into work.
The release stage is where the delivery happens.
- ultimately delivering the artifact means that a version of the application is available and ready to be used.
<br>The next step is to deploy
In some cases the deployment is manual<br>
For continuos deployment all steps are automated and completed with no or very little human interaction.

**Deploy a jenkins server**
- There are 3 requirements
1. use the latest version of Ubuntu Server.
2. Install NGINX as a proxy to jenkins
3. finally, install and configure jenkins

Try to use a public cloud service.
using Amazon web Services :
>> create a key pair for SSH connections
>> Create an EC2 instance using ubuntu AMI
>> Create an elastic IP for persistent DNS assignment
>> Connect to the server and install NGINX and Jenkins

https://charanwrites.hashnode.dev/deploying-a-jenkins-server-in-aws-cloud-platform

**Jenkins Pipelines:**
- Jenkins supports two pipeline formats. They are 1. scripted and 2. declarative

|scripted pipeline | Declarative pipeline |
|-------|---------|
|It starts with node keyword<br>node {} | It starts with pipeline keyword <br>pipeline {} |
|It uses Domain specific language (DSL) or Groovy based DSL <br> groovy is a scripting language for the java virtual machine | These are evalution of DSL pipelines <br>The declarative syntax was developed to more easily capture the complete configuration of a project as code |

Declarative pipeline :<br>
A declarative pipeline has three sections namely 1. agent section, a stages section and inside stages section atleast one step

//code

pipeline {
    agent any
    stages{
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
}

**Pipeline configuration : agent**
- It specifies where pipeline steps will be run. we can use several parameters to specify an agent.some of the parameters we use are <br>
any<br>label<br>docker<br>none
<br>
- if we use the any agent that means we are letting jenkins know that it can run the pipeline using the first available executer<br>
In systems where jenkins is running jobs on the controller, this is likely the agent you would use the most.<br>agent any   Run on the first available system<br>when we need to be specific about the agent that runs the pipeline we can use the label parameter. This is helpful when we need to run or on a server where a specific tool or a resource is installed
<br>agent { label 'linux' }  Runs on a system with this label<br>agent {
    docker {
        image 'maven'    // Run the pipeline inside a docker  container using the specified image
    }
}

This is useful for the projects that need to build environments that are fresh and consistently provisioned on each build.

- The none agent is a special case. since , the agent selection at the top of a pipeline is applied to all commands, the none agent allows us to defer agent selection to stages.
<br>agent none     defer agent selection to stages
<br>so, using none allows you to use a different agent for each stage in the pipeline.

**pipeline configuration: stages and steps**
stages {
    stage('Build') {
        steps {
            echo 'This is the build step'
        }
    }
    stage('test') {
        echo 'This is test step'
    }
    stage('Deploy') {
        echo 'This is deploy step'
    }
}

- we identify specific parts of the process being automated.
- If we were developing a CICD pipeline, for example we could use stages named build, test and deploy to represent the action needed for an application deployment.
- Each stage must contain atleast one steps section.
In steps section, we list the commands that actually do something. This is where we run programs, scripts and commands that interacts with the compute platform that the pipeline is running.
- We can have multiple commands in each step
**Pipeline steps :**
- echo --print message 
<br>git --checkout code from git repo
<br>sh  -- Run a shell script or a local command
<br>archiveArtifacts --Archive artifacts

**Pipeline syntax generator :**
- jenkins provides a pipeline syntax generator that we can use to create snippets of code that we can copy into a pipeline.

**pipeline variables**
- variables let us use dynamic values in our pipelines. jenkins exposes three different types of variables that we can use : **environment variables, current build variables and parameters.**

###### Environment variablees :
> Named with all capital letters
> Can be set globally or locally
> Environmental variables will be globally scoped

pipeline {
    agent any {
        environment {
            MAX_SIZE = 10
            MIN_SIZE = 1
        }
    }
}

Locally scoped 

pipeline {
    stages {
        stage('Scale by 10x') {
            environment {
                MAX_SIZE = 100
                MIN_SIZE = 10
            }
        }
    }
}

- Using an environmental block at the beginning of a pipeline exposes the variables to all pipeline steps.
- Using an environmental block of a stage only exposes variables to steps within that stage.
- environmental variables can be referenced in a few different ways in a pipeline depending on how they're being used.
- They can be preceded with the word env in lowercase followed by a dot and then the name of the variable or they can be referenced by their name
- if an environmental variable is being used in a string the value must be prefixed with a $ sign can be followed by curly braces that wrap the entire variable name.
<br>echo env.MAX_SIZE        echo MAX_SIZE
<br>echo "$env.MAX_SIZE"      echo "$MAX_SIZE"
<br>echo "${env.MAX_SIZE}     echo "${MAX_SIZE}"

**current build variables**
> currentbuild variables allow pipeline steps to reference the state of a build while it's running. This can be useful for dynamic operations that needs to do something specific based on a previous step or a certain step in the build
> All of the currentbuild variables are actually properties of one variable named **currentbuild**

> To access the current build properties the values are proceeded by currentBuild a dot and then the name of the property.
> The properties are also case sensitive and follow the camelcase format.with a lowercase letter to start, and a capital letters for each additional word in the variable name.
> for each additional word in the variable name
<br> 
**properties of the variable named currentBuild : **
<br>currentBuild.startTimeInMills
<br> currentBuild.duration
<br>currentBuild.currentResult

**parameter variables :**
- parameters are another type of variables that get their values at the time job is triggered.
- parameters are triggered in a parameters block which is placed at the begining of the pipeline code.
- parameters are proceeded by the params prefix
and if they are used in a string they need to have a dollar $ sign at the begining and can also be wrapped in curly braces.

params.PARAMETER_NAME
"${params.PARAMETER_NAME}"


pipeline {
    agent any {
        parameters {

        }
    }
}
> assign values to a variable when a job is triggered.

- Each parameter must include a name, default value and description.
- Use all capital letters for easily identification
- For pipelines we use five different types of parameters we use they are 
<br>
1. string<br>2. Text<br>3. Boolean<br>4. choice <br>5. password

string(name: 'FATHER,
    defaultValue: 'Vader',
    description: 'Enter your father's name.')


text(name: 'PHRASE',
    defaultValue: 'It was the best of times, it was the worst of times,...',
        description: 'Enter your favorite phrase from a Charles Dickens book.')

- string parameters are best used for single word values.
- text parameters are used if you need to pass in a long block of text that contains multiple lines.
- Boolean parameters let us pass in true or false values and are represented by a checkmark in the jenkins interface.


booleanParam(name: 'RUN_TESTS',
    defaultValue: false,
    description: 'Toggle this value to run tests.')

- Choice parameter present the user with a list of options to choose from 

choice(name: 'AWS_REGION',
    choices: ['us-east-1',
        'us-east-2',
        'us-west-1',
        'us-west-2'],
    description: 'Select a region for deployment.')

- password paramters can be used to enter a sensitive values


password(name: 'DATABSE_PASSWORD',
    defaultValue: 'DATABASE_PASSWORD',
    description: 'Enter the database password.')

- pipeline parameters aren't available immediately after being defined.
- jenkins applies parameters after the first run
- The first run may encounter errors, if default values are not available.
- if you modify or add a parameter the pipeline will need to be run once before the change is applied.

##### conditional expressions and manual approvals

conditions for when:
> branch
> environment
> expression

pipeline {
    agent any 
        stages {
            stage('XYZ') {
                when {}
            }
        }
}

- if the specified condition evaluates to true, then the stage will be allowed to run. otherwise the stage will be skipped.
- Branch conditions are useful when a pipeline is interacting with a version control system like github.
- This can be useful for building different projects that can be interact with different environments.

when { branch 'default' }

when {
    environment name: 'DEPLOY_TO', value: 'production'
}

- expressions conditions provide the most flexibility for conditional statements
<br> we can use groovy expressions along with parameters

when {
    expression {
        params.ENVIRONMENT == 'PRODUCTION'
    }
}

**Manual Approvals**

pipeline {
    agent any {
    stages {
        stage('xyz'){
            steps {
                input message: 'Confirm deployemnt to production..',
    ok: 'Deploy'    
                }
            }
        }
    }
}

- we use input step to control the pipeline. The input step pauses a triggered pipeline and waits for a manual interaction to determine if the pipeline should proceed, or abort.
- we can also configure an input step with a custom message to give more information on what will happen if the job were to proceed.
- 

## Integrate jenkins with version control systems
[Connect jenkins with github practical guide](https://charanwrites.hashnode.dev/connecting-jenkins-to-github)

## Agents and distributed build
**Distributed build with agent :**
>> Jenkins server which is also refered to as jenkins controller provides a web interface to manage configuration.
>> A best practice is to limit jobs that are run on the controller to free up resources and do this on other servers which are refered to as agents or nodes.
>> This approach frees up cpu, memory, harddrive space on the jenkins controller so it can use those resoures for management tasks like scheduling jobs. 
>> A node is another server or system connected to a jenkins controller over a network.
>> **Node :**A server or system connected to a jenkins controller
- Nodes provide the jenkins controller with a compute resource for running jobs.
>> **Agent:**A process running on a node that manages jobs and reports status to the jenkins controller.
- The agent runs the commands in the job definition and reports the status back to the jenkins controller.
- In reality nodes and agents are different parts of a Jenkins system but you will often hear either term used to refer to an external system where jenkins runs jobs.
- There are many types of nodes and agents that jenkins can use as compute resources. one of the most common nodes is a secure shell or SSH node.  

## SSH nodes :
- connect to servers using SSH Keys
- System must accept SSH connections
- A user and key must be in place for jenkins to use
- Java must be installed

## Docker nodes :
- Run jobs in new containers on each build
- Docker process must be running on the node

## Tips for using nodes and Agents
**Agent configuration:**
agent {
    label 'linux'
}
agent {
    docker ..
}

## Tool configuration
tools {
    maven 'Maven-3.8.4'
}

## cheking out code :
git branch: 'master'
    url: 'https://github.com/jenkinsci/jenkins.git'

- when jenkins uses a pipeline from a repository, the first checkout is on the jenkins controller. This allows jenkins to read and process the jenkins file to get the project configuration.
- when jenkins start running job on an agent, the code that was initially checked out won't be available.


**Add an SSH agent to Jenkins :**

**Add docker agents to Jenkins :**

Challenge : Improve a Docker agent pipeline

## Artifacts and Testing

#### Artifacts and fingerprinting
- when a jenkins job creates an object that needs to be saved. we refer to that object as an artifact.
- Artifacts can be compiled binaries like docker images and zip files or an artifact may be a text file like a report or some sort of document.

### Fingerprinting
- when an artifact is created or used, jenkins generates an MD5 checksum using the artifact.
- This checksum and job where it was created are tracked in an internal database.This becomes the file's **fingerprint**
- jenkins can then use the fingerprint to determine what jobs either created or accessed a file.


- To determine the effectiveness of a test, developers often use a technique called **code coverage** 
- code coverage tracks the lines of code that are accessed during a test. 
- if more code is exercised during the test, bugs are more likely to be discovered. 
- Two popular code coverage formats are JaCoCo and Cobertura.
- jenkins uses codecoverage API Plugin to collect and publish multiple code coverage report formats includes jacoco and cobertura.


	
	Jenkins Installation :
	
	Jenkins is written in Java, a platform-independent programming language. Like with any other Java application, it can be installed on a variety of operating systems such as Linux, Windows, MacOS, etc.
	
	Prior to installing Jenkins, you need to ensure that your system at least meets minimum hardware and software requirements:
	• 256MB RAM
	• 1 GB of disk space (10 GB if running as a Docker container)
	• Java 8 or Java 11
	• Modern web browsers - Google Chrome, Mozilla Firefox, Microsoft Internet Explorer, Apple Safari.
	
	To complete installation follow steps in https://www.jenkins.io/doc/book/installing/.
	
Jenkins Dashboard :
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/cd1e25e4-4375-442b-848b-457bd16ad55c)


Jenkins Dashboard mainly consists of :
	1. Header
	2. Side Navigation
	3. All view for jobs/projects
	4. Monitoring Builds
	5. Footer
	
	1. Header 
	The main header includes the following components:
	• Breadcrumbs
	• Add/edit description
	• Context search box 
	• Logged in user dropdown 
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/4589945d-17ca-4309-9884-b9d4500bb5a7)
	
	
	
	 
	Breadcrumbs are a secondary navigation system that show a user's location on the Jenkins user interface. These allow you to quickly navigate to specific pages (or links) within the current hierarchy.
	
	Add/Edit Description :
	
	You can use this to add/edit some text to the Jenkins dashboard, jobs, build, etc. The text can be a note, a reminder, or anything that can be useful to your team.
	
	Content Search Box :
	
	- The context search box lets you search for content Jenkins wide. By default, the search is case-insensitive, and it comes in very handy as you can quickly search for specific text, Jenkins jobs, builds, etc.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/7ef2709a-db90-497f-b8b5-fa1f92e1fcf3)
	
	
	
	
	Logged in user dropdown 
	
	--> At the very top-right corner of the header, you will notice a dropdown menu linked to your username.
	
		Builds
		This displays all the builds for the user.
		Configure
		This gives you the ability to configure your own settings, ssh keys, email address, custom views, and many more.
		My Views
		The "All view" is the default view for all users. However, you can create your own custom view and set your default view to your custom view.
		Credentials
		You can view user credentials for your own account or any other authorized credentials.
	![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/be13a202-794c-455d-9f6b-04eb8b86ec45)
	
		
		
		
	2. Side Navigation
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/73efa8a5-7108-4fed-9850-bbbc2fec1c43)

The side navigation bar provides initial top level configuration options. At minimum, you should be able to view the default configuration items.
• New Item
This is used to create new Jenkins jobs.
• People
This lets you view/modify all the user accounts that have access to the Jenkins UI.
• Build History
Clicking this will open a new subpage, which displays the build jobs, their status, and trend.
• Manage Jenkins
This is where you can perform a variety of administration tasks such as configuring Jenkins, managing plugins, configuring global tools, security, etc.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/5c525ea7-57c8-4a2d-9d00-9086e1ed9f59)



Note that any plugins you install may add additional configuration items here. It is also worth noting that each subpage within Jenkins will have its own configuration options




All View for Jobs/Projects

This view lists every single job that is configured on the Jenkins instance. It also displays the overall state of each Jenkins job.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/70ee205b-babe-4912-82be-943f2116b125)






For a given job in this list, the following information is indicated:

Build Status :
	Uses color codes  ( described below in more detail )
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/24930e81-23d1-457c-ad3a-1a6aa75f4fc4)

Health/Build Stability (W)
	Uses weather icons (described below in more detail).
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/62385143-4c1e-4456-b3ef-61d536b932a7)

Job Name
Last Success
	Displays when was the last time the job built successfully, and the related build number.
Last Failure
	Displays when was the last time the build failed, and the related build number.
Last Duration
	How long did the latest build take to run?

 (icon)
To start a build.


 
Jobs Table footer :
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/1173613e-252d-4dc7-baea-16a29b7760b0)

The jobs table footer lists links to the legend of all the icons on the jobs table and their definitions, as well as RSS feeds for all builds, failed builds, and latest builds.

Monitoring Builds

This section provides overall visibility into your jenkins job executions. It lets you know if your jenkins server has too many or too little resources, and can be useful for IT capacity planning purposes. Monitoring builds has two  subsections 
	1. Build Queue
	2. Build Executor Status
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/d5015889-14c7-49cc-9dc2-bc0bee01b1de)

	1. Build Queue :
	
	The Build Queue section displays all the jobs that are currently queued and waiting for an executor to free up. 
	You can click on the queued job to retrieve more information on the job. Alternatively you can cancel the job by clicking on the red colored X icon, which is displayed next to the job.
	
	2. Build Executor Status
	
	The Build Executor Status lists all the builds that are currently in progress by each configured agent.
	You can click on the progress bar to view the build console output.
	You can also view the jenkins Node dashboard which lists all the nodes ( controller, agents ) by clicking on the build executor link.
	
	
Page footer 

-> At the very bottom right corner of the jenkins UI is a link for Rest API. 
This link will provide you with some basic information on how to use Rest API to programatically interact with Jenkins. 
Using Rest API is an alternative to performing various operations via the jenkins UI.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/00e647fc-2c11-417e-ba44-f1fc127f642c)







Plugins :

--> Jenkins uses plugins to provide much of the user-needed functionality. Many Jenkins features such as integrating source code management tools, build tools, reporting tools, code coverage, static analysis, notifications are all implemented as plugins.

-->   Essentially, all the Jenkins plugins are Java Archive (JAR) files with either an .hpi or .jpi extension. For example, Git plugin (git.hpi), Maven plugin (maven-plugin.jpi).


-->  Currently, there are 1800+ plugins available for use. You can view a list of all the available plugins on the Jenkins Plugins Index page.

Managing Plugins :

--> you can administer plugins using Plugin Manager . You can easily navigate to plugin manager from jenkins > Manage jenkins > Manage plugins

![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/43f304d3-09b3-47bf-9022-1cc271f821b5)


 
Using the Plugin Manager, you can perform a variety of administrative tasks such as installing, deleting, updating, enabling or disabling plugins.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/bbe0e4fb-e1ec-408e-bea2-577f17c9097e)
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/6eb30787-2dd2-476a-afa1-e090f2260554)




Install Plugins

>> The Available tab under the plugin manager lists all the plugins that are available for installation. This list can be pretty long, so make use of the filter to search for specific plugins you would like to install.

>> You can install and start using most plugins almost immediately by checking the box adjacent to the plugin and clicking Install without restart. However, we recommend that you always restart your Jenkins controller after installing a new plugin by clicking Download now and install after restart. Application restart ensures all components are properly initialized.

Manual upload :

Another way to install plugins is to manually upload an .hpi or .jpi file using the upload plugin option on the Advanced tab.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/1bf5fbba-987e-4b03-8385-cdf9632ce3a6)



So, when should you use this option ?
- This especially useful in cases where you are using an older version of plugin not currently available on the jenkins update site, or if you developed your own custom plugin.
- If your plugin has dependencies on some other plugins, be sure to install those plugins as well, Otherwise your plugin may not work as expected.

Installed Plugins :

The Installed tab under Plugin Manager lists all the plugins installed on your Jenkins instance. It can be used to quickly verify if a specific plugin is already installed, or if you need to confirm which version of a plugin is installed, etc.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/09295f21-3437-40c9-b615-65fb3e02dfea)



Uninstall Plugins :

If you no longer need a plugin, you can uninstall it by selecting the specific plugin on the Installed tab and clicking the Uninstall button.

Please note that uninstalling a plugin may leave behind some plugin configuration data. Navigate to Jenkins > Manage Jenkins > Manage Old Data. You can view and purge all the unwanted data here.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/d3cf0c1e-e75a-489d-a305-be8ef60028b1)


Disable Plugins :

Sometimes, you may not want to remove a plugin altogether, but you just want to  be able to disable its functionality. 
You can do so on the Installed tab by searching for the plugin, and unchecking the toggle under the Enabled column.

![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/d3e08397-e7c9-4f41-b14f-9bfe561a0418)

You might want to note that when you disable a plugin, it will still show up under the list of installed plugins. However, Jenkins does not really start the plugin, and any extensions contributed by this plugin are not visible.


If you need to re-enable the plugin at a later time, you just need to check the toggle under the Enabled column and restart your Jenkins server to make the plugin operational.

Update Plugins :
	-- It is always a good practice to update the plugins frequently. New releases of plugins add enhanced functionality, security fixes, etc. Also, older versions of plugins may not be compatible with newer versions of Jenkins core.
	-- The Updates tab lists all the installed plugins for which an update is available. You can update a specific plugin by checking the toggle under the Installed column, and clicking Download now and install after restart button.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/6529a867-b8bc-4a58-85a3-bd3015814a57)
	
	
	Jenkins Security 
	
	-- For any organization, their intellectual property (IP) is a valuable data and it is important to protect it. Confidentiality, availability, and integrity, also known as the CIA triad, are the fundamental principles of information security.
	• Confidentiality determines the secrecy of your IP, and prevents unauthorized access to restricted data.
	• Integrity ensures that your IP is accurate and reliable, and it has not been modified from its original state while in transit or at rest.
	• Availability is the ability of the users to access your IP. Information is of no use if it cannot be accessed.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/5aad3153-3287-45c1-ad6a-56b1c3249a97)

	
	Your Jenkins server hosts your organizational intellectual property (IP) such as your source code, build artifacts, etc. Your Jenkins environment is also a fully distributed build system with Jenkins server and agents (more on this in a later section of this course) and each network connection is a potential point of entry.

	
Securing Jenkins :

Many of the global security features are configured on the Configure Global Security page.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/759beb89-0bdf-472c-a4d4-8ec4e58faa69)



CSRF Protection 
- Cross site Request Forgery ( CSRF ) is an attack that forces an end user to execute unwanted actions on a web application in which they are currently authenticated.

Enabling CSRF protection will protect your Jenkins environment from malicious attacks.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/3217e962-209e-4ce2-903c-eb8eb3907533)



Agent-to-Controller Security

In a distributed build environment where jenkins server leverages additional resources ( Agents ) for running the builds, Agents can request any information from the server such as 
 content of files, or request a Controller to run specific commands.

-- Enabling Agent > Controller Access Control allows a jenkins administrator to control which specific information is allowed by agents.

-- Note that this feature is enabled by default and it is recommended that jenkins administrators do Not disable it. An alternative could be to tweak the rules to exempt built-in rules.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/7a204c5e-24f6-45d2-88d7-24354592575b)

	
	

TCP Port
	
	- In a distributed setup, jenkins can use a TCP port to communicate with the agents. This port is disabled by default. If needed, you can enable it by selecting either a Fixed port or a Random Port.
	Choosing a fixed port is recommended as it makes it easier to manage the firewall rules and avoid port collision
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/0aa242ea-a7d2-4f77-b9d0-4781667a6e33)
	
	
Markup Formatter

	Jenkins allow user input in many configuration areas, setting the Markup formatter to plain text by default will eliminate any unsafe HTML or Javascript
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/594ea02a-9ca1-405a-a56d-1f247e34d743)
	
	
	
	
Authentication
	- Authentication is an act of validating that users are who they claim to be, essentially confirming the identity of users. Usernames and passwords are the most basic form of authentication.
	- Jenkins supports many different authentication systems through security realms. A security realm tells jenkins which referential to use for authentication.
	- There are 4 security realms which are supported out of the box. These are :
		- Delegate to servlet container
		- Jenkin's own user database
		- LDAP
		- Unix User/group database
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/211d0854-b47a-48bd-9d00-5025bf9e9e38)


		Delegate to servlet container :
			This realm delegates authentication to the servlet engine running Jenkins. For instance, Tomcat , Jboss, Websphere ,etc. have their own authentication mechanisms.
			- If using this realm, you will need to look into the servlet container's authentication documentation. Ex: Apache Tomcat 9 configuration documentation
		Jenkins own user database :
		- This security realm uses jenkins local database and is enabled by default when you initially install jenkins
		- If you select this security realm, you do have the option of letting your user's signup. However, please refrain from assigning any significant privileges, such as edit, administrator, etc. to authenticated users, as this can pose a big security risk.
	Note : If you deselect the signup option, only users with overall administrator privileges can create users.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/6d6e1225-69f9-417f-9409-5dea15d6524a)

	
	LDAP :
	- This authentication delegates authentication to an external LDAP service. Most companies already have a Directory service for authentication. This option is more common for larger installations in organizations which already have configured an external identity provider such as LDAP. This also supports Active Directory, OpenlDAP installations.

Key features of LDAP include :
- It is highly tunable
- Its binding can be sub-authenticated
- You can take advantage of the caching mechanism to leverage load on LDAP servers.
- There's support available for LDAP replicas

There are various other security realms available through plugins such as Github Authentication, Active Directory and BitBucket Oauth, to name few. We can find more on plugins page of jenkins.

Unix User/group database :
- This realm delegates authentication to the underlying Unix/Linux machine, and it only works if you are running jenkins on a Unix Server.

If you enable this realm, your end users will have to login to jenkins by entering their operating system username and password.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/0f805866-b589-4543-93b8-0fed0d886012)


	
Authorization
- Once a user/group is authenticated, you need to determine the actions this user/group should be able to perform. Authorization always occurs in the context of authentication.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/0a62b210-18ea-41c9-b40d-ac8baad93c62)



Some of these are lightweight authorization strategies and some offer granular access controls.


Lightweight Authorization
- Anyone can do anything
This allows both authenticated and anonymous users to do anything.

- Legacy mode
This allows administrators to perform any action. All other users are restricted to read only mode

- Logged-in users can do anything
This is the default authorization strategy, It allows all Authentication and provide no fine-grained access control.


Matrix Based security
- This authorization strategy allows you to define actions allowed for each user or group globally by using a matrix. On the vertical axis are the users or groups, and on the horizontal axis, you configure the actions for the corresponding users/groups.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/612b6292-b112-422a-8197-0b4ec0aa4212)


- You can add a new user or group by clicking the Add user or group button.
Hover the cursor over each privilege to display information about what that privilege entails and click the appropriate boxes to define the access that is allowed for each defined user or group
- Notice that two rows are defined by default. The first row defines permissions for Anonymous users ( unauthenticated users ) who access the Jenkins UI, and the second row defines permissions for Authenticated Users who access the Jenkins UI.
- Note that all the permissions granted are additive, and they are grouped into various categories :
	- Overall
	- Credentials
	- Agent
	- Job
	- Run
	- View
	- SCM
	- Lockable
	- Resources
	Also, any plugins you install could add additional groupings.

Project based Matrix Authorization Strategy

- Project based Matrix Authorization is an extension of Matrix Authorization. In addition to assigning permissions globally, project-based Matrix Authorization lets you define permissions for the  individual Jenkins Jobs.
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/6ed1e412-3cde-4e48-857c-6c2935f2b419)


Permissions that are granted in the global configuration apply to all of jenkins jobs, until they opt out of inheriting global permissions.

Credentials
- Jenkins needs to authenticate itself against other services :
	- SCM repositories for retrieving source code (or pushing it)
	- Binary repositories for storing artifacts or fetching dependencies
	- Remote secured services for authentication such as LDAP
	- Deploy to secured environments.
- With the credentials plugin, you can centrally manage credentials to authenticate to various services. When a credential is created, jenkins knows it and allows for easy selection.

How to create credentials :
Create Credentials
- Inorder to create credentials, you need to have the Credentials-Create permissions . This is configured in the Authorization section of the Configure Global Security page. The image below illustrates using the matrix Authorization Strategy to assign Credentials-Create Permission to a user named "John".
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/eee12e83-1ee4-4b03-a868-a5b14be61d38)

Next Navigate to < your user-name > > Credentials from the Jenkins dashboard header , 
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/603356af-1ea1-4e75-9b13-9ed9a734bdc9)


Click User under stores scoped to your username followed by Global Credentials ( Unrestricted ) Domain.


Create a new credential by filling in the details on the Add Credentials Page


Jenkins Projects 

What is jenkins project ?
- Jenkins project is a sequential set of tasks that are defined by a user. Typical steps include retrieving the latest source code from version control, compiling it, running unit tests, building and storing the artifacts, and notifying the end users of the outcome of the build.

- On the jenkins UI, the term "project" has been synonymously with "job". Note that both of these are runnable tasks controlled and monitored by jenkins.

Types of Jenkins Projects 
There are many different project types available in jenkins including :
- Freestyle Project 
	- This is the default project type, most flexible to configure, and is included as part of the core jenkins
- Maven Project
	- This one is useful for building Maven Projects. It requires Maven Integration Plugin to be installed.
- Pipeline and Multibranch Pipeline
	- These are useful for creating end-end CI/CD pipelines. These requires pipeline and multibranch plugins to be installed.
- Multi-Configuration Project 
	- This is useful for projects with a large number of configurations. It requires the matrix project plugin to be installed.

Create a new jenkins Project :
To create a new Jenkins project, click Jenkins > New Item on the side navigation bar of the Jenkins dashboard.


- This opens up a new subpanel listing various project types. Enter a name for the Jenkins project, select the appropriate project type from the list, and click OK. The image below illustrates creating a new Freestyle project called "myapp".


Anatomy of a jenkins Project :

A Jenkins project typically includes the following components.
• Global Project Options
• Source Code Management
• Build Triggers
• Build Environment
• Build
• Post-build Actions


Global Project Options
	Meta-information
	Meta-information is basically information about the project. For a Jenkins project, project name and project description are meta-information. Be sure not to input any JavaScript in the description field as it can pose a security risk.
	
	Build history management
	Every time you run a Jenkins project, it stores the build log, artifacts, metadata, etc., on the disk. Over a period of time, this can take up a lot of disk space. To cap disk space consumption, you can set a build log retention by clicking the box adjacent to Discard old builds. Then you will be presented with two options of setting a policy for discarding builds:
	• Days to keep builds
	• Max # of builds to keep
	Note that these two policies can be active at the same time. For example, you can keep builds for 7 days, but only up to a limit of 30 builds, as illustrated in the image below. If either limit is exceeded, then any builds beyond that limit will be discarded.
	You can also set a retention policy for build artifacts by clicking the Advanced button.
	
	
	Build management
	The General section also provides configuration options for general build management. Click the Advanced button to view all the options.
	
	
	Some of the most common configurations are listed below.
	• Quiet period
Setting a wait time between builds.
	• Retry Count
Setting a count for the number of times Jenkins will try to checkout from the configured SCM system until it succeeds.
	• Disable this project
Disable a project if you no longer need to build it. You can always enable it if needed at a later time.
	Any additional plugins you install may add to the list of global options.
	
	
	
	Source Code Management
	
	
	This is the section where you specify the details of the version control repository for building your source code. You have the flexibility to select the SCM tool of your choice, but be sure to install the necessary plugin.
	
	
	 Build Triggers
	
Jenkins allows you to trigger builds automatically. Let's take a look at some of the options under the Build Triggers section.

Build periodically
    You can schedule periodic builds using cron-like syntax. Here is an example of scheduling a build every 15 minutes.



Build after other projects are built

You can also automatically build a project after another dependent project has been built successfully.

Poll SCM
You can poll SCM at a certain frequency using cron-like syntax. Jenkins will poll SCM at the set times to detect new commits. If there are any, then Jenkins will go ahead and run the build.


It is worth noting that polling adds extra overhead as it scans the entire workspace before checking with the SCM system for any new changes.

Webhooks
Ideally, you would want to trigger a new build as soon as a source code change is detected so as to align with CI/CD goals. At the same time, you do not want to add polling overhead. The best way to navigate this is to let your SCM system handle it by configuring Webhooks. Here is a GitHub example describing how to configure Webhooks.

Build Environment

The Build Environment section allows you to specify additional options for your builds - cleaning up the workspace prior to starting a build, setting up the required environment variables used in the build, aborting builds that are stuck, adding timestamps to the build logs, etc.
These options are provided by various plugins - Workspace Cleanup, Credentials Binding, Build Timeout and Timestamper to name a few. The more plugins you install, the more options you will see under this section.


Build

The Build section comprises the actual steps to build your source code, run various tests (unit, integration, etc.), code quality, code coverage, and many more.


Note: Your source code should include the test cases, and your build tool should be able to generate the required report for it. Jenkins can be used to display build tool generated test reports and trends.


You can add one or more build steps, and re-order them however you like simply by dragging and dropping them.

You may also choose to install plugins that suit your specific needs. Such plugins can contribute to additional build steps.

Post-Build Actions

- Post-build actions are performed based on the result of the build status. Examples include notifying developers, publishing test reports, archiving build artifacts, triggering other build projects, automated deployment, etc.


The list of post-build steps can vary depending on the plugins installed.

Freestyle Project

What is freestyle Project ?
--> A Freestyle project is far the most versatile of all the Jenkins Project types, It allows you to build any type of project ( Ant, Maven, Gradle , Shell Script, Mark file etc.) and it is included in the jenkins by default, There is no need to download  any other plugin. 

Creating a Free Style Project 
--> For our example Freestyle project, we will use a small Java application. We will configure all the necessary tasks for this project such as retrieving the Java source code from version control, compiling and building it, running tests, publishing the code coverage and static analysis reports and notifying the team about the status of the build.


To Create a new freestyle project, click Dashboard >New item on the sidenavigation bar of the Jenkins Dashboard.


This will take you to the configuration page for the new Freestyle project you have just created.
Next, we will configure our Freestyle project java-app to build a Maven project. Maven is a software project management tool used to build Java projects.

Configuring Free Style Project 
The java-app project requires Java version 8. You can specify this dependency under the General section of java-app project configuration. However, you need to ensure that Java 8 is first installed on your Jenkins server.
Jenkins allows you to easily manage various tools and their versions all under Dashboard > Manage Jenkins > Global Tool Configuration page.


On this page, click the Add JDK button under the JDK installations section to configure multiple JDK versions.



Next, follow these steps:
• Add a Name for the Java version you are trying to install.
• Check the toggle for Install automatically.
• Choose the JDK Version from the dropdown.
• Enter the credentials for your Oracle account.
• Check the License Agreement checkbox.
• Click Save.


Note that you can also use other Installers to install different versions of JDK. Just click the downward arrow on the Add Installer dropdown to view all the available options.


You will have to add at least two JDK tool versions in order for them to show up under JDK versions in the General section of your java-app project configuration page.


Source Code Management

o build the java-app project, you need to fetch its source code from a version control system.
First, create your own repository:
• The source code for the Java app is hosted in a GitHub repository (click here to create your own GitHub repository)
• Enter the Repository name
• Enter an optional Description
• Set it to Private
• Click Create repository from template
Below is an illustration showing how to create your own repository.



Next, we need to configure the Git repository under the SCM section of the demoapp-freestyle project:
• Scroll down to the Source Code Management section.
• Select "Git".
• Enter Repository URL (enter your GitHub repository URL).
• Select Credentials to authenticate to the SCM repository.
• Click Add > Jenkins to add the SCM credentials.


There are a number of ways to add credentials. We will cover this in a later section of the course. For now, you can choose to configure your SSH Username with private key credential as shown below.


NOTE on the SSH Key: You will need to create a SSH key locally on your machine if you don't already have one, and then add the SSH key to your GitHub account.
Here's more information on how to check if you have an existing SSH key.
Here's information on how to generate a new SSH key.
Here's information on how to add your SSH key to your GitHub account.
Once you are done setting up your SSH key, you can configure the credentials.
Make sure to select SSH Username with private key for the credentials kind. Enter the private portion of your key (id_rsa file content) under the Private Key section.
Once the credentials are added, you can view and select them from the credentials dropdown list.


For our java-app project, we will select the master branch.



NOTE: You can also choose a specific branch in a repository, a repository browser, and advanced options for integrating with your repository.
Click Save to save your SCM configuration.
Next, we will configure the build triggers for our java-app project.

Build Triggers 

- For our java app project ,we will be using Poll-SCM build trigger and set the pooling to every 15 minutes. 



Build Environment
We will just add a timestamp to the build console output. To enable this, check the toggle for Add timestamps to the Console Output.





Build :

In this section, we will compile and build our java-app project, run tests, and generate the required reports for code quality and code coverage.
We will start with adding a build step, Add build step > Invoke top-level Maven targets.

This will add a new build step and configure it as follows:
Maven Version: maven3
Note that we are using Maven version 3. To use this version, you need to install the Maven 3 version via Dashboard > Manage Jenkins > Global Tool Configuration.
Goals: clean verify site

A note on the options:
• clean: will wipe out any existing compiled sources in the target directory and start the build from a clean state
• verify: will run any checks to verify the package is valid and meets quality criteria
• site: will generate java-app project code coverage and static analysis reports
Next, click on the Advanced button.


This will display additional configuration options. We will just specify the location of the POM file.
POM: java-demo-app/pom.xml
Leave all other fields set to their default values. 




Click Save to save your configuration.
We are done configuring the build step. Next, we will configure the post-build actions.

Post-Build Actions

For our java-app project, we will configure the following post-build actions:
• Archive the build artifacts so we can use them later.
• View code coverage trends so we can see the percentage of code that is executed as part of the tests.
• View static analysis trends so we can measure the code defects.
• Notify the team on the build status so that developers and team members can get quick feedback on the build, and take any necessary actions.

Archive Build Artifacts

Our java-app project generates a Java ARchive (JAR) file. To archive the file for later use, choose Add post-build action > Archive the artifacts...


and specify the location of the JAR file.
Files to to archive: **/target/*.jar
This will look for all files with .jar extension recursively under all target directories from the workspace’s root.


Next, we will configure publishing the code coverage reports that are generated as part of the build step.
Publish Code Coverage Report

For our java-app project, we are using JaCoCo, a code coverage tool for Java. To enable publishing JaCoCo reports, you first need to install the JaCoCo plugin. This will add a new option to record code coverage reports under post-build actions.
Next, choose Add post-build action > Record JaCoCo coverage report.


Configure the following and leave all other fields set to their default values:


Next, we will add a new step to publish static analysis reports. 

Static Analysis Reports

--> Our java-app project uses the following two tools: SpotBugs and PMD. Both of which help detect defects in Java code.
First, ensure that the Warnings Next Generation plugin is installed. Upon plugin installation, you will be able to view a new option to record your static analysis reports under post-build actions.
Choose Add post-build action > Record compiler warnings and static analysis results.



From the drop down Tool menu, select SpotBugs. Set Report Encoding to UTF-8. Leave all other fields set to their default values.


Static Analysis Reports :

Next, we will add the second tool - PMD. Under the configuration for Static Analysis Tools, click Add Tool.




Select PMD from the tool dropdown. Set Report Encoding to UTF-8. Leave all other fields set to their default values.  


Finally, we will configure email notifications for our java-app project.
Email Notifications

Jenkins provides out of the box email support to send notifications to team members.
Choose Add Post-build action > Email Notification, and specify the target recipients for the emails. This is illustrated below.

You might want to take a look at the Email Extension plugin, if you are looking to customize your email notifications.
Click Save to save your configuration.
We are now done configuring the java-app freestyle project. It’s time to start a new build and see things in action!

Build History

Click Build Now on the side navigation of the java-app project to trigger a new build.


Once the build is completed, you should be able to view all the relevant information such as build number, build date, SCM changes, name of the user who started the build, console output, artifacts, code coverage report, static analysis report, etc.


When you run this project more than once, you can view the build history, code coverage and static analysis trends, etc., on the java-app project page.


PIPELINE Projects :

Freestyle vs Pipeline Projects
You should have noticed by now that Jenkins is mostly UI-centric, meaning all the projects are manually configured through the UI. If you recall from Chapter 1, Continuous Delivery heavily relies on seamless end-to-end automation. Although Freestyle projects provide you with a lot of flexibility to configure projects, they are not quite suitable to orchestrate complex CD scenarios. For example, if you want to build and test on a variety of OS platforms in parallel, or when you are waiting for some manual approval prior to deployment, etc.
Although you can create project hierarchies with Freestyle projects for representing multi-stage workflows, such strategy requires you to spread project configuration across multiple projects. Thus making it difficult to manage and maintain them as a simple change in one project might adversely affect the others. But that's not all, you might find it challenging to visualize a workflow spanning multiple Freestyle projects.
This is where Jenkins Pipelines come to your rescue by helping you:
• Create a set of instructions written as a code to model complex workflows.
• Provide a single-place visualization of different stages of your workflow.
• Keep all the Pipeline code stored in SCM, so you can apply SCM best practices such as versioning, tracking and auditing to the project configuration itself.


Pipelines

-- Pipeline is a new Jenkins project type and a new way to model and visualize CI/CD workflow for a project. It is created by writing a bunch of instructions in a file called Jenkinsfile. The Jenkins Pipeline uses a domain-specific language based on Apache Groovy to create, edit, view, and run CD pipelines.

-- A Jenkinsfile can use either of the following two syntaxes:
• Declarative Pipelines
They require the Blue Ocean plugin to be installed. You can easily create your Jenkinsfile using the Blue Ocean graphical pipeline editor. It also provides you with a great visualization of your pipeline runs.
• Scripted Pipelines
With scripted pipelines, you have the option of creating the Jenkinsfile using the classic Jenkins UI. This means you will be creating the Jenkins project using the Pipeline project type. While scripted pipelines offer a lot of flexibility, they also require you to have a knowledge of Apache Groovy.

-- It is worth noting that there is a lot of commonality in the syntactical components between declarative and scripted pipelines.
-- It is best to start out with declarative pipelines, and as you get comfortable with them, you can move on to scripted pipelines. For the remainder of this chapter, we will focus on declarative pipelines.

Pipelines Terminology
Prior to creating Pipelines, you need to know a few basic pipeline-related terms. Let's take a look at them:
• Controller
A machine where Jenkins is installed. It centrally stores all the configurations, loads plugins and renders the Jenkins UI.
• Agent
A machine which connects to the Jenkins Controller and performs various operations as directed by the Jenkins Controller.
• Node
A machine that can allocate an executor and run Jenkins Pipelines. Examples are Jenkins Controllers and Agents.
• Step
A single task that tells Jenkins what to do at a given point in time. Examples include: executing a simple shell script and windows batch script.
• Stage
It is composed of logically distinct steps. Build, Test, Deploy are all examples of Stages. Stages are used for visualization of the Pipeline status/progress.
For a complete list of pipeline-related terms, see Jenkins' Pipeline Glossary.

Creating a Pipeline

We will now talk about creating pipelines using the Blue Ocean graphical editor. Let's start by creating a Pipeline to simulate a CI/CD workflow with the following set of stages:

• Build
In this stage, source code is compiled and built, and an artifact is generated.
• Test
In this stage, tests will be run in parallel on two different OS platforms, Linux and Windows.
• Deploy Staging
In this stage, the artifacts will be deployed to a staging environment (essentially a pre-production server). If everything is good, we will request for approval to deploy to production.
• Deploy Production
In this stage, artifacts will be deployed to the production environment.
 


We will also configure two post-build actions:
• Archive build artifacts
• Email notification in case of a build failure
Let's get started with creating the Pipeline.

Creating a Pipeline: Open the Blue Ocean Editor

-- Once you install the Blue Ocean plugin, you should be able to view the Open Blue Ocean link on the side navigation. Click on this link to navigate to the Blue Ocean UI.
Note that Jenkins officially supports the latest versions of Google Chrome, Mozilla Firefox, Microsoft Internet Explorer, and Apple Safari web browsers. However, Chrome and Firefox seem to be the most consistent performers.


In the Blue Ocean UI, click Create a new Pipeline. If you don’t see this option, select New Pipeline in the top-right corner.



Configure SCM 
 
Next, you will see a screen prompting you to configure your source code repository.
The source code for the pipeline project is hosted in a GitHub repository. This repository includes all the required build scripts. Click here to create your own GitHub repository.
• Sign in to GitHub
• Enter the Repository name
• Enter an optional Description
• Set it to Private
• Click Create repository from template
The following screenshot illustrates how to create your own repository.

 

Once you have set up your own repository, you are ready to proceed with the next steps to create your Pipeline. Determine:
• Where do you store your code?
• How do you connect to your Git repository?
Based on your SCM preference, you can choose how you would like to connect to your SCM repository. Let’s take a look at two different ways to connect Git repositories.
Choosing Git:
• Choose Git for Where do you store your code?
• Enter the Repository URL
• Click Copy to clipboard to copy the SSH key (be sure to register the SSH key onto your Git server)
• And finally, click the Create Pipeline button.

An illustration of choosing Git is shown in the figure below.


• Choose GitHub for Where do you store your code?
• Next, enter your GitHub access token. If you do not have one, click on Create an access token here link. Be sure to copy the token.
Click on the Connect button.


Next, choose a GitHub Organization the repository belongs to. An illustration is shown in the figure below.


Next, choose the repository that you want to use for this project. This is the repository you set up from the template earlier.


And finally, click on the Create Pipeline button.

If you put these steps together, your configuration should look similar to this:


Since this is the first time you are creating a Pipeline, you will see a pop up message stating that there are no Jenkinsfiles in the SCM repository. Once you create and configure your Pipeline, its configuration code will get stored in the SCM repository as a Jenkinsfile.


Next, we will go ahead and configure the various stages for our Pipeline.

Creating a Pipeline: Build Stage

If you recall Pipeline terminology, stages are composed of steps. As part of the Build stage, we will add two steps.
	1. Print Message: This will print Build demo-app
	2. Shell Script: This will run a build shell script

This will open a configuration panel for the new stage. Enter "Build" for Name your stage. Click on the Add step button below which opens the Choose step type panel.




 
In this panel, choose the Print Message step. This will open the Print Message configuration panel.

Enter Build Demo Application for the value, and click the top-left back arrow icon (←) to return to the main Pipeline editor.



Next, we will add another step to incorporate our build script. Choose Shell Script from Choose Step type. This will open the Shell script configuration panel.


Enter sh run_build_script.sh in the configuration panel.


This completes the Build stage configuration.

Creating a Pipeline: Test Stage

Next, we will add two parallel stages: Linux Tests and Windows Tests.

Linux Tests Stage
In the Pipeline editor, click the + icon next to the Build stage to add a new stage. This will open a configuration panel for the new stage. Enter "Linux Tests" for Name your stage and click on the Add step button below, which opens the Choose step type panel.
We will add two steps similar to the build stage.
• Print Message: Specify Run Linux tests in its configuration panel.
• Shell Script: Specify sh run_linux_tests.sh in its configuration panel.


Next, click the + icon below the Linux Tests stage to create a parallel Windows Tests stage.

Windows Tests Stage
As part of this stage, we will just configure a single step Print Message, and specify Run Windows tests in its configuration panel.


Once both tests are successfully run, we will deploy the artifacts to a staging environment. Click the + icon next to the Linux Tests stage to add a new stage and specify "Deploy Staging" for the name.


Creating a Pipeline: Deploy a Staging Stage

As part of this stage, we will add two steps.

The first step is Print Message. Specify Deploy to staging environment in its configuration panel.

Please note that it's a common practice to seek approval prior to deploying in a production environment. And while deploying to the staging environment cannot be accomplished in the Freestyle project, we can easily add this as a step in our Pipeline project.
In order to do that, click on Add Step and choose Wait for interactive input step from Choose step type. Note that the list of step types can be long. You may want to use the search filter available on the Choose step type panel to quickly find the step



 
In the Deploy Staging / Wait for interactive input panel, specify Ok to deploy to production? in the Message field. Leave other settings with their default values. Click the top-left back arrow icon (←) to return to the Pipeline stage editor.


Next, we will configure the Deploy Production stage, which is the last stage in the Pipeline. Click the + icon next to the Deploy Staging stage to add a new stage.



 
Specify Deploy Production for the name.

Creating a Pipeline: Deploy a Production Stage

As part of this stage, we will add a single step, Print Message, and specify Deploy to Prod in its configuration panel.


Creating a Pipeline: Post-Build Actions

At the time of this writing, the post-build actions cannot be configured through the UI. You need to add them to the Jenkinsfile directly. You can open Jenkinsfile from the Pipeline editor by clicking Command+S on MacOS, Ctrl+S on Windows, or the equivalent on other operating systems.
Add the following code snippet after the stages block to archive build artifacts, and send out an email notification in case of a build failure. Please be sure to replace the email address in the code block.

post {
  always {
   archiveArtifacts(artifacts: 'target/demoapp.jar', fingerprint: true)
  }
failure {
      mail to: 'YOUR EMAIL ADDRESS',
      subject: "Failed Pipeline ${currentBuild.fullDisplayName}",
      body: " For details about the failure, see ${env.BUILD_URL}"
     }
  }

Click on the Update button to update the Jenkinsfile for our pipeline project.


Your Jenkinsfile should look like this.
Click on the Save button at the top right to save your Pipeline configuration.


In the Save Pipeline dialog box, specify the commit message First Pipeline in the Description field. Leave all other fields set to their default values.

Click Save & run to run your pipeline. This will accomplish the following:
• Jenkinsfile which contains your Pipeline code will be committed to the master branch of the Git repository. You can also specify any other branch. If the branch does not exist, one will be created automatically.
• Jenkins will queue the Pipeline project.
• It will start executing the first stage (Build) defined in our Pipeline.


When the main Blue Ocean interface appears, click on the row to see Jenkins build your pipeline project.


At the very end of the Deploy Staging stage, you will be asked to decide if it is OK to deploy to Production? Click on the Proceed button to advance to the Deploy Production stage.


Creating a Pipeline: Pipeline Visualization

The Blue Ocean UI displays different colors based on the status of a Pipeline run...
and a weather icon for the build trend.




Upon a successful pipeline build run, you will notice that the Blue Ocean interface turns green.
You will also be able to view the various stages of your pipeline project as well as different steps, build metrics and download logs per stage—all displayed in one place. In case there is an issue with a certain stage, you can restart this specific stage without having to re-run the entire pipeline.
 



In this chapter, we have only scratched the surface of Jenkins Pipelines. In reality, Pipelines allow you to orchestrate much more complex applications.

Why Distributed Build Architecture?

Up until now, we have run all the builds on the Jenkins Controller. So far it worked well for us. However, what if you need to run hundreds of builds every day? Well, you can try scaling your Jenkins Controller vertically by adding more resources (CPU, memory, etc), but you will eventually cap out of resources as you can scale a server vertically only up to a certain point.
The next thing that probably comes to your mind is adding more Jenkins Controllers. There are two major issues with this approach. First, it is going to create an administrative overhead to configure and keep track of all the Jenkins Controllers, and their corresponding builds, configurations, etc. Secondly, you may be developing applications that need to be supported on a variety of OS platforms, and you may need to run builds on various platforms. For instance, consider a situation when your application needs to be built and tested on Linux, Windows and MacOS. You won’t be able to achieve this because each Jenkins Controller is tied to a specific operating system.
Besides scaling, there is also a major security flaw associated with running your builds on the Jenkins Controllers. All Jenkins projects run with administrator privileges, and a malicious actor can potentially access or delete any private information compromising the security of your data.
The solution to the above problems is a distributed build architecture that allows you to have a single Jenkins Controller and leverage additional servers to perform the builds.

Distributed Builds Terminology

Before we deep dive into distributed build architecture, let’s quickly review some terminology related to it.
• Controller
A machine where Jenkins is installed. It centrally stores all the configurations, loads plugins, and renders the Jenkins UI.
• Agent
A machine that connects to the Jenkins master and performs various operations as directed by the Jenkins Controller.
• Node
A machine that can allocate an executor and run Jenkins projects. Examples are Jenkins Controller and Agents. You will notice that nodes and agents are sometimes used synonymously.
• Executor
A Jenkins executor is one of the basic building blocks which allows a build to run on a node. You can configure more than one executor for every node. The number of executors is set based on the number of CPUs, IO performance and other hardware characteristics of a node and the type of builds you have configured to run. The number of executors determines the number of concurrent builds that can be run at any given point in time. It is Jenkins security best practice to set the number of executors to 0 on the Jenkins Controller, and not run any builds on it.

Distributed Builds Architecture

In a distributed environment, all the Jenkins projects are configured centrally on the Jenkins Controller. The Jenkins Controller accepts all the requests for builds and manages the build environment, but offloads the bulk of work (execution of the builds) to the configured agents.

There are many advantages to this approach:
• It allows you to run builds for multiple OS platforms. For example, if you need to run a build on Windows platform, all you need to do is add a new Windows agent and connect it to your Jenkins Controller.
• It lets you scale your build infrastructure on demand by adding more build agents.
• It helps you mitigate security risk by restricting the information that an agent can request from the Jenkins Controller.

Please note that there are some requirements for this setup.
The Jenkins Controller needs to be able to communicate with the agent to offload the work of building the project. The agent executes all the tasks, and passes information (artifacts, build log, etc.) back to the Jenkins Controller which essentially requires a bi-directional communication between the Jenkins Controller and the agents.
All Jenkins agents require Java to be installed as there is a slave.jar file that needs to be run on all the agents. The Java version of the agent must be the same as the Java version installed on the Jenkins Controller.

The slave.jar file is located at <Your Jenkins URL>/jnlpJars/slave.jar.
Other than these requirements, there is no need for a shared file system, a shared subnet, etc.






Connect a Build Agent

To connect a new Jenkins agent, you will need to navigate to Dashboard > Manage Jenkins > Manage Nodes and Clouds.


Next, Select New Node



Enter Node name, select Permanent Agent and click OK to proceed to the configuration screen.

On the configuration screen, you are required to enter the following:
• Description
A meaningful description of the agent.
• Number of executors
Set this number based on the CPU cores on the agent.
• Remote root directory
An absolute path to a root directory on the agent. This directory will be used as a temporary root directory for building projects.
Configure a Build Agent: Labels

Labels are used to group multiple agents into one logical group. For example, if you need to run builds on a Linux agent, you can assign each Linux agent a label called "linux". You can also use multiple labels for each agent. For example, a Linux agent that also runs Ruby builds can have two labels, "linux" and "ruby". Be sure to not use special characters for label names.
How do we use these labels in Jenkins projects? Let's see.

For Freestyle Projects
Check the toggle for Restrict where this project can be run under the General section, then enter the label name for the Label Expression.
 

For Pipeline Projects
Bring up the Pipeline editor for your Pipeline project. Under Pipeline Settings, select the type of agent from the Agent dropdown menu and enter a name for the Label.



Configure a Build Agent: Usage

You have two options to choose from:
• Use this node as much as possible
This is rather self-explanatory.
• Only build projects with label expressions matching this node
Reserve this node for all the projects that are restricted to certain nodes using node names and labels.

Configure a Build Agent: Launch Method

You can choose one of the following launch methods based on your requirement:
• Launch Agents via SSH
• Launch Agent by connecting it to the master
• Launch Agent via execution of command on the controller
We will now discuss each of these methods in more detail.


Launch Agents via SSH

As the name suggests, SSH connectivity is used to launch an agent. This is supported by default on all Linux and MacOS systems. You can also install OpenSSH on the latest versions of Windows systems (see Microsoft Documentation to learn more).
In order to use this launch method, you need the following:
• Install SSH and ensure that the SSHD is running successfully on the agent
• Set up a user account that can be used to log into the agent
• Add Jenkins Controller’s public key to the agent’s authorized_keys file.
Note that once the connection is established Jenkins will automatically copy the slave.jar file onto the agent.


Launch Agent by Connecting It to the Master

This launch method is useful for cases where agents are Windows OS-based, or they are behind a firewall and unable to use SSH to connect.
In order to use this launch method, you need to configure the port that Jenkins Controller will use to listen for incoming agent connections on the Configure Global Security page.



Once you configure the agent, you have the option of launching it with or without the GUI. It is best to run the agent without using the GUI.



Launch Agent via Execution of Command on the Controller
You can use a command on the Controller to launch an Agent as long as the Jenkins Controller is able to execute commands remotely using SSH, RSH, etc. Both this and the Launch Agents via SSH method have similar requirements for setup.
Instead of using a single command, you can also create a shell script on the agent which includes a set of commands such as setting JDK path, location of slave.jar file, etc., to be run on the agent and execute this script remotely from the Jenkins Controller.








Configure a Build Agent: Availability

You can choose one of the following options:
• Keep this agent online as much as possible
• Bring this agent online and offline at specific times
• Bring this agent online when in demand, and take offline when idle.
Optionally, you can specify additional Node Properties such as environment variables, tool locations, etc. Once you are done configuring, click Save to save the configuration.



View and Manage Jenkins Agents

You can view and manage all the configured agents from Dashboard > Manage Jenkins > Manage Nodes and Clouds page.



Next, you can click on the selected agent to view all the projects associated with this agent.






Verify Project Execution on an Agent

If you restrict a project to use a certain agent or a label, you can verify if the project is picking the right agent from the Build Executor Status on the main Jenkins dashboard.





Load Statistics

You can view the overall load on your build infrastructure by going to the Jenkins Dashboard > Manage Jenkins > Load Statistics page.



Load statistics provide you with the following metrics:
• Number of online executors
A total number of executors that have been configured to run a build and are currently online.
• Number of busy executors
Number of executors currently running a build.
• Number of available executors
Number of executors currently available to run a build.
• Queue length
Number of projects in the build queue that are waiting for an executor to free up.

Organizing jenkins Projects
-- making use of Folders and views

Monitoring with Jenkins
-- we can do monitoring by using plugins like prometheus, Nagios etc.

Security
-- Github authentication. LDAP, Active Directory and Role based authorization via rolebased authorization strategy plugin supports granular permission for roles. 

This strategy allows permissions to be assigned at a business function level (role) rather than individual user/group level.

Distributed Builds

Jenkins pipeline as code Using DSL programming language















 

















 



















 


 

 

 

 

 

 

 

 

 





 




 


 




























	
	
	
	
	
	
	

Freestyle Projects
Pipeline Projects
Distributed Builds Architecture
 
![image](https://github.com/Charan-happy/MyTechskillimprovement/assets/89054489/bac84e4b-06c0-4725-975e-e894d5306d86)
