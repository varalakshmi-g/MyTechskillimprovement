
what is ngnix ?
- It is a high performance, open source server that powers millions of websites and applications.
- It excels at  
- The main purpose of using nginx is to server websites effeciently and reliably. 
#### Apache HTTP vs Ngnix

simmilarities :

- Both are free and open source
= Wide range of world wide community
- Added functionality through dynamic module
- proxy servers
- Event based processing for simultaneous connections


|Apache | Ngnix|
| --- | --- |
|config : XML syntax | config : C-like syntax |
|Distributed .htaccess file | Centralized location blocks |
|Dynamic content is natively processed with modules | Dynamic content requires external processing |
|serving static content is less effecient | More effecient at serving static content |
|caching and loadbalancing capabilities with modules | Native caching and load balancing capabilities |

 #### features of Ngnix
 
 - It has high performance and a very low overhead
 - It can be cache responses and reduce the load on the backend servers
 - It can be used as a Reverse proxy
 - It can balance the load across multiple servers
 - It can compress the content before sending thus bettering
 - It can rewrite URLs are forward the apt request in the apt format
 - It has rate limiting capabilities to prevent platform abuse DDOS
 - It can handle SSL/TLS termination and pass unencrypted requests to the backend servers.

why choose ngnix ?
 - Quickly became the leader in the web server market
 - Effecient and consistent under the heavy load
 - Easy to configure


## craating an ubuntu instance in aws

![image](https://user-images.githubusercontent.com/89054489/229964483-b6999cb9-c495-454b-96b1-0d09744cde3c.png)

![image](https://user-images.githubusercontent.com/89054489/229964695-44150fa4-3bf9-4ea0-9281-323dac70349f.png)

![image](https://user-images.githubusercontent.com/89054489/229964768-ca2be42e-9f29-4940-a990-24649e756238.png)


![image](https://user-images.githubusercontent.com/89054489/229964891-d73dd2fe-d83c-4027-ba25-585ff3dfefbe.png)

![image](https://user-images.githubusercontent.com/89054489/229965096-2c96c577-aa8e-49e2-b0af-edfefabe07b7.png)

![image](https://user-images.githubusercontent.com/89054489/229965368-7ff0f9cc-7e80-4991-9a15-f1ff476f3ce7.png)
![image](https://user-images.githubusercontent.com/89054489/229965506-df0187af-b7a4-4c68-8374-b4f51007dca9.png)

![image](https://user-images.githubusercontent.com/89054489/229965605-55f5f8d2-8c8d-44f0-a347-e4b36dd25576.png)


#### Assigning Elastic IP

![image](https://user-images.githubusercontent.com/89054489/229966052-7e4937e4-efe5-4811-ae85-e0cd17efe230.png)

![image](https://user-images.githubusercontent.com/89054489/229966212-574185ab-80d5-462e-84cc-31a0b35e9f16.png)
![image](https://user-images.githubusercontent.com/89054489/229966370-7c1e6c35-9b9b-44ef-a759-e136eb2575e9.png)
![image](https://user-images.githubusercontent.com/89054489/229969492-f25d05a1-50c4-48d9-bf8a-e0d1610d885b.png)


![image](https://user-images.githubusercontent.com/89054489/229966478-812d61fe-746b-43f3-9f2d-d7595015b346.png)

![image](https://user-images.githubusercontent.com/89054489/229966697-ea8daa8d-d5ee-41b6-80dc-17742f50580f.png)

#### connecting server via ssh

![image](https://user-images.githubusercontent.com/89054489/229967014-973ea762-eebe-479f-9554-859c9b25d404.png)
![image](https://user-images.githubusercontent.com/89054489/229971901-a4d6f438-94ca-436f-955f-2d69a9d8c725.png)

![image](https://user-images.githubusercontent.com/89054489/229971964-acd4e62c-63ec-431d-831b-356b2f716dad.png)

### installing nginx in ubuntu in AWS

![image](https://user-images.githubusercontent.com/89054489/229972633-2ccea78d-2b49-42d4-9bf6-d8adb3e6d0e7.png)

![image](https://user-images.githubusercontent.com/89054489/229972761-481eb40a-8baa-4c37-a5a8-164378fb2000.png)

![image](https://user-images.githubusercontent.com/89054489/229972856-2ec50c00-71bd-4e26-8408-54fe434b4c17.png)
![image](https://user-images.githubusercontent.com/89054489/229972998-30d22d63-89ee-4311-8b76-44762ef150b1.png)

final confirmation that nginx is installed in our instance is by giving the elastic IP address in the browser

![image](https://user-images.githubusercontent.com/89054489/229973426-14fe3d14-3b31-4f30-aa7f-d255c167f2cf.png)

#### nginx command line interface

- use the cli to control NGINX
- Elevate your session to use root permissions: `sudo` command /`sudo su -`

**CLI commands**
- Check status
- stop and start the service
- Check the service configuration

![image](https://user-images.githubusercontent.com/89054489/229973856-ad2869f6-d9ba-4ace-9dd7-4019e8c346db.png)

![image](https://user-images.githubusercontent.com/89054489/229973936-d35b7163-c7b5-46b9-9d57-103e2b032398.png)

![image](https://user-images.githubusercontent.com/89054489/229974174-b6c73ac6-593f-4dff-bdea-4c894dbd69e7.png)
Althouth both start and reload will not produce any output by using start nginx at the bottom we can observe the chnage status


![image](https://user-images.githubusercontent.com/89054489/229974564-afc3bc11-0d8e-444a-b533-e2739e6802b9.png)
To get listing of switches we will run the above command

![image](https://user-images.githubusercontent.com/89054489/229974929-fc58bcc5-3104-4123-b602-031dcf53b9ef.png)


### NGINX files and directories

- ![image](https://user-images.githubusercontent.com/89054489/230016722-7c762b31-3482-42b6-a5c2-9d27dc797ccc.png)

![image](https://user-images.githubusercontent.com/89054489/230017521-a68752e3-1a83-492e-b9c4-7582d4a1a5f6.png)

![image](https://user-images.githubusercontent.com/89054489/230017868-5e571603-7bf4-4ba9-bc4c-80d181589e1c.png)

it is the default directory where nginx stores the errors and log data files.
![image](https://user-images.githubusercontent.com/89054489/230018275-1b726c88-c138-4522-9427-6ff157f8cf9b.png)

The access log records, any accesses that the web server has processed along with the details like time access , IP address of the requestor and path that was requested.


NGINX uses the error log to record the any web server encounters and in addition to any operational messages llike restarts and configuration reloads and finally, var/www

This location contains the files that get served to client, including HTML images and any other documents that are stored on the server.

![image](https://user-images.githubusercontent.com/89054489/230021267-899997f8-dcd8-4cc3-9c08-98f7b9e38f99.png)


### INside nginx.conf

we need to go to the `etc/nginx` and type `view nginx.conf`
- 
![image](https://user-images.githubusercontent.com/89054489/230022004-84a6011e-b293-4e0c-9d8c-d3d33c1fcf8f.png)

directives and blocks are present in the nginx.conf file

![image](https://user-images.githubusercontent.com/89054489/230023078-af3805cd-11f4-4e63-b0e6-bff3a93b2854.png)
we can close this page by typing `:q!`

![image](https://user-images.githubusercontent.com/89054489/230024084-480ec5e8-f9b1-4fe1-8a25-d15d1949a292.png)

#### Configure a virtual Host

- since, default configuration is linked to a file in "sites available" we can remove that with unlink commnand which is shown below


![image](https://user-images.githubusercontent.com/89054489/230025386-ac32b31e-a1c8-4f21-aba1-83438dd81823.png)

We will be setting up an demo site for an online store called Binaryville.

It is good practice to name the config file after the site to keep things organised. since a single nginx server can run multiple sites, naming the configuration file the same as the site make things easier to manage.

It is also important that we use .conf extension. so that the configuration gets picked up by nginx when we reload a site. if there's ever a configuration that we don't want to use, we can either remove the file or just rename it so, that .conf isn't the extension

![image](https://user-images.githubusercontent.com/89054489/230157103-4f0f86ad-fe6a-4889-825c-c9629f3178ae.png)

![image](https://user-images.githubusercontent.com/89054489/230158600-a470cf37-cbeb-4a3b-9441-77b78e602198.png)


![image](https://user-images.githubusercontent.com/89054489/230159638-4c39ca0e-de50-467b-bd9e-2bd4b9f84cef.png)
![image](https://user-images.githubusercontent.com/89054489/230160526-9b5d00f1-5a60-4825-ae25-b4fbfa1d7d84.png)

![image](https://user-images.githubusercontent.com/89054489/230161295-0b3f6a2a-4d81-4454-9790-1086ec6b71f3.png)

![image](https://user-images.githubusercontent.com/89054489/230161362-b0304ac7-1f47-4867-93f1-78e432e3865e.png)

![image](https://user-images.githubusercontent.com/89054489/230162487-c10c272f-10e6-4ceb-9258-c60f26893163.png)

![image](https://user-images.githubusercontent.com/89054489/230162203-1a1c204a-d0c6-48c7-aef8-2fa3f5530540.png)

### Adding files to the root directory

![image](https://user-images.githubusercontent.com/89054489/230169879-61c649fd-7829-4483-a501-15eab513dfd8.png)
![image](https://user-images.githubusercontent.com/89054489/230170228-13a6b3d9-d25b-4398-8516-4e656730dee9.png)

![image](https://user-images.githubusercontent.com/89054489/230170400-d67aa40c-e209-4528-afd5-cbe82db642b3.png)

### challenge
**scenario** :
- A web developer has just completed the design for a new website. It works perfectly on their laptop. and they wanted to share it with the rest of the team from a web server that everyone can access. They've asked you to setup an NGINX server for the new website. Once the server is in place, they'll take it from there to upload the final design.

- use a server running the latest version of ubuntu
- install NGINX
- Test the status of the NGINX service
- Test the default configuration
- Make sure the default website is accessible

**solution**
`sudo su -` >> `sudo apt update` >> `apt install -y nginx` >> `systemctl status nginx` >> `nginx -t` >> `go to chrome and reload the website by the dns of the instance that you have created`

- settings for NGINX are listed as simple directives on one line or in blocks on multiple lines. Block start with a directive and are followed by an open bracket, more directives, and then a closing bracket.

- The /etc/nginx directory holds the configuration for the entire NGINX installation. Inside this directory, you'll find the files that control the way the web server runs along with the files that define the web sites being served.

## Additional NGINX configurations

- Location directive allow us to extend our configuration, based on the Uniform resource indicator (URI)
- These are formatted as blocks inside the server blocks

EX: server {
      location [modifier] location_definition {
      ...
      location [modifier] location_definition {
       ...
       }
       }
   }
   
   The location directives uses modifiers, prefix strings and regular expressions.
   
   location Modifiers
   
   | Modifier | Application to Location Definitions |
   | --- | --- |
   | None | The location definition is interpreted as a prefix for the URI |
   | = | The URI must be an exact match to the location definition |
   | ~ | The location definition is used as a case-sensitive regular expression |
   | ~* | The location definition is used as a case-insensitive regular expression |
   | ^~ | If the longest prefix matches, then no regular expressions are checked |
   
   **Prefix String**
   - "=" modifier is optional
   - Checked first

  **Regular Expression**
  - Modifiers are required
  - Checked in order of appearance

**Location Processing**
- Nginx processes the location in the below order 

  Exact match location (`=/index.html`) --> prefix location (`/index.html`)--> Regular Expression location (`~*/index.html`)
  
#### Configure locations
- Now let's add locations for :
  - Site root
  - Images
  - Error Pages

![image](https://user-images.githubusercontent.com/89054489/230440079-a854299c-718e-4c30-b67c-2656fc032487.png)

Before Test
![image](https://user-images.githubusercontent.com/89054489/230440363-31df2213-4ef0-49da-b0fe-364870efdc6d.png)
After Testing for images
![image](https://user-images.githubusercontent.com/89054489/230440520-27cf67cf-9654-4a4f-8671-c0a84a496e7e.png)

![image](https://user-images.githubusercontent.com/89054489/230440659-2cff08e8-6493-4267-a598-25b0890a0bd5.png)

![image](https://user-images.githubusercontent.com/89054489/230440893-d0552572-7a64-46ac-893d-c879fcff9ec0.png)

Now we are confident that our location configurations are working as expected.

### NGINX Logs
- nginx uses log files to record various operational details, These logs are useful for monitoring normal operations and tracking down issues if a problem occurs.

Please have a look at the below log file type along with the details inside that particular log file
###### Access logs :
- Time of the request
- Result of the request
- Client IP address
- Client Browser

###### Error Logs :
- Configuration errors
- Service stops and starts
- service errors

The default log configuration is in the main configuration file, nginx.conf

/etc/nginx/nginx.conf

http {
   ...
   access_log /var/log/nginx/access.log;
   error_log /var/log/nginx/error.log;
   ...
 }

let's set up a custom logging to the website in our server

![image](https://user-images.githubusercontent.com/89054489/230443816-f7c31efe-c79a-462f-89ff-12da582706b4.png)

![image](https://user-images.githubusercontent.com/89054489/230444425-c94372ed-4134-428d-8945-bf33d3589bde.png)

![image](https://user-images.githubusercontent.com/89054489/230444511-bddb6d58-79b6-40ff-8f0e-d88845fcb1d2.png)

![image](https://user-images.githubusercontent.com/89054489/230445170-3648424c-3a6c-4208-81f8-84064d2cf562.png)

![image](https://user-images.githubusercontent.com/89054489/230445295-c1f9c006-11b7-49f7-8e41-b3057328fb8e.png)

This conclude us that we have custom logging is also working as expected.

### Troubleshooting NGINX

check for configuration file errors by using `nginx -t` This is especially useful after making changes to any NGINX config files.

check for configuration file typos `root /var/www/htm1`

let's say you made some changes to your site but, you can't reach your site at all.  Then you need to do the following troubleshooting steps:
- `systemctl status nginx`  and then `systemctl reload nginx` 
Now go to browser and check the status.

- If nginx is up and running but you aren't seeing anyting served, you wanted to make sure the standard port for web traffic are open, ports 80 and 443 by using `sudo lsof -i :80 -i :443 | grep nginx` `sudo apt install net-tools` `sudo netstat -plan | grep nginx` LSOf - list open files

`net stat gives us information on all of the network connections for the system` 

Tail the logs --- `tail -f /var/logs/nginx/*.log`

## challenge --customize an NGINX configuration
**scenario : ** 
- A member of your team has deployed an NGINX server and needs your help adding a custom configuration for status page. They asked you to remove the default configuration and add a new one. The new configuration needs to have a one rout named /complete that returns the message your request is complete.  The route should exactly match the word in lower case. Along with the message NGINX needs to write each request to a log file that separate from any other logs collected by NGINX. 

Steps to solve this issue.

1. Remove the default NGINX configuration
2. Add a provided configuration file to the correct location.
3. Add an exact match location for "/complete"
4. update the location to write logs to "complete.access.log".

**solution**

- connect to the server and login as root

![image](https://user-images.githubusercontent.com/89054489/230457106-ffa1fa49-0303-4d00-b89c-a447e00b35c2.png)

now first, i will remove this default configuration . first, we removed the default NGINX configuration means we basically unlinked the default file that was linked into /etc/nginx/sites-enabled.

![image](https://user-images.githubusercontent.com/89054489/230457840-1552e3c0-9476-4811-a410-2a11860e89a8.png)

![image](https://user-images.githubusercontent.com/89054489/230459069-46f2f6f3-3ed2-417c-acfe-3c2e1f74c8d9.png)

Now let's go to the browser and check the changes
![image](https://user-images.githubusercontent.com/89054489/230459347-3c3c67cf-554e-4bc7-b867-3443034dea6a.png)


Now reload the browser multiple times, just to fill up the log files with some information
After that let's come back to our terminal window and do the following commands
![image](https://user-images.githubusercontent.com/89054489/230459795-331298e0-8ac4-4895-aa4c-4db7ed4d1c14.png)

Now, it shows all the data from log files which means we have customized the nginx configuration 


![image](https://user-images.githubusercontent.com/89054489/230458741-c3d638bd-bac3-418a-ad28-8a5394bd24fe.png)

Q&A

-> Location directives are formatted as blocks and are defined inside server blocks. They can also be nested inside other location blocks
-> Default loggings are configured in the http context and can be overridden in the server and location contexts
-> Nginx uses log files to record various operational details like the date, time and name of a file that was served. These logs are useful for monitoring normal operation and tracking down issues if a problem occurs.
-> The try_files directive gives NGINX a list of files or directories to look for, relative to the location. The first file or directory that matches gets processed. If no items in the list match. Then the last item in the list is used as a URI or an error code.
-> when nginx can't find any content to respond to a request, it displays a 404 error page.

## Reverse Proxies and load balancers

**Reverse proxies and load balancing**
![image](https://user-images.githubusercontent.com/89054489/230463493-d9fe04d9-3cbd-46f3-8341-b863daa5d92b.png)
![image](https://user-images.githubusercontent.com/89054489/230463642-5bed7884-22e6-440b-8ce3-da81630a3b85.png)
![image](https://user-images.githubusercontent.com/89054489/230463729-ab5cd343-44fe-40f6-8d22-d3dc47530ee0.png)

- proxies and load balancers provide very simmilar functions. In
- client connects the proxy or loadbalancer on the front end then the proxy connects to the server or resource on the backend and returns the response to the client. 

Reverse proxies usually applied in the cases where there is only one server on the backend. In these type of cases nginx is great at simplyfying things that might be harder to implement in other technologies like SSl termination and logging.

Nginx proxies are also good for accelerating the response from backend servers by caching content. By storing frequently requested content, NGINX can reduce the load on back-end servers and responds to the client requests more frequently.

Nginx also has capabilities to compress data which can reduce the amount of network bandwidth needed to fulfil the request. 

Nginx by acting as a loadbalancer act as a proxy to a single server as well as multiple backend servers to handle large nubmer of client requests/high volume of request.

Load balancers also supports session persistence . This is useful when client needs same server to accept and respond on the same server.

##### configuring NGINX as a Reverse Proxy
- upstream Directive is one of the key components used to configure nginx for proxying and load balancing. 
- Upstream direcives group together servers allowing other directives to reference all of the servers as a single unit.
- It defines group of servers that can be referenced by other directives

There are certain context where we can apply directives in the global context that affects all of nginx.
Nginx configuration :
`global context
http {

      server {
              location {
              
              }
      }
 }`
 
 with http protocol and inside the HTTP context , the server and location context that specify configure virtual hosts and URIs used to access them.
              
- Upstreams are defined in the HTTP context. This is useful so that one upstream can be defined and then reused by multiple servers and locations.
- we will be connecting to location context by using the proxy_pass directive.

![image](https://user-images.githubusercontent.com/89054489/230553409-e1a87709-6c94-41ff-b418-fa4f4c4317a1.png)

![image](https://user-images.githubusercontent.com/89054489/230554764-961c2e1b-4504-461a-8cb7-d87f6f27dfbd.png)


## Configuring nginx as a loadbalancer

--Nginx uses 3 methods to connect to upstream servers. Round-robin, Least connections, Ip hashing  These methods are indicated with directives applied within upstream block. Nginx also uses weight directives to modify these three methods.

Servers connected one after another. The defauilt one is Roundrobin.

**Round robbin method**
upstream example {
  Server 127.0.0.1.7001;
  Server 127.0.0.1.7002;
  Server 127.0.0.1.7003;
}

servers with fewest connections is favored.
upstream example {
  least_conn;
  server 127.0.0.1.7001;
  server 127.0.0.1.7002;
  server 127.0.0.1.7003;
}


Ip hash method is used for session processings. Connection is based on the cient's IP address.

upstream example {
  ip_hash;
  Server 127.0.0.1.7001;
  Server 127.0.0.1.7002;
  Server 127.0.0.1.7003;
}

weight directive is used to influence the others
upstream server with higher weight is favored.

upstream example {
  Server 127.0.0.7001 weight=2;
  Server 127.0.0.7002;
  Server 127.0.0.7003;
 }
 
 
### challenge -- set up a load balancer using NGINX

**scenario** : Your company has developed a cloud service for generating universally unique identifiers (UUID's). Your team is concerned that once the server is gets rolled out they won't be able to take the service offline for update. You have been asked to demonstrate how the UUID generator can be placed behind a load balancer.  So that changes can be made without 
 swapping individual requests to the service. one of the developers from your script shared the script that simmulates how the UUID generator can run on multiple servers. But, they need your help to setting up the load balancer. 
 
 Steps to complete this challenge
 > Install NGINX and remove the default NGINX configuration
 > use the provided configuration file
 > Add a configuration named "uuid" that alternates traffic across three ports: 9001, 9002, 9003
> Add a location that proxies requests from the group on "/uuid"
> start the UUID generator using the provided Python Script. `python3 uuid-generator.py`
> Test your NGINX configuration in a browser using the address for your VM.
> correct configuration should show the port numbers in sequence along with a UUID.

#### Solution
- first i am making sure my server is having nginx and it's running up and fine.
- 
![image](https://user-images.githubusercontent.com/89054489/230749288-723d7a52-8eea-47cd-90ea-bc00aec5ede6.png)

- Remove default configuration of the nginx by using `unlink /etc/nginx/sites-enabled/default`
![image](https://user-images.githubusercontent.com/89054489/230749567-74c5508a-f1d5-4ce5-a70c-e540946e959c.png)
![image](https://user-images.githubusercontent.com/89054489/230749589-ffd6cbd4-d211-4421-8056-0ebd24823831.png)

- Copy the
-  configuration file to the correct location 
`cp loadbalancer.conf /etc/nginx/conf.d/`
![image](https://user-images.githubusercontent.com/89054489/230749710-4955d61d-b256-4c80-879b-48387fa96b4b.png)

![image](https://user-images.githubusercontent.com/89054489/230749923-cfec11be-fe8a-4e5a-9dfc-3420b561b2b3.png)

![image](https://user-images.githubusercontent.com/89054489/230749902-a8dfa9df-3a2d-4aaf-82e2-e385a217bb84.png)

 Now let's test configuration with `nginx -t` and reload the nginx with `systemctl reload nginx`
 ![image](https://user-images.githubusercontent.com/89054489/230750010-a4506d52-9e5b-4cdd-8db3-fb8b2796288c.png)

Now let's start the appserver
![image](https://user-images.githubusercontent.com/89054489/230750021-52261584-17df-4385-81b6-8438e8845123.png)

Now go to the browser
![image](https://user-images.githubusercontent.com/89054489/230750046-9f4bd43d-73c1-49dd-a6a4-28d32d9ddd8d.png)

- The weight directive is used to influence load balancing methods. Since each server is considered evenly in the round robin method and by connections in the least connections method, a weight can be applied to a server to give it a higher preference.
- If there is only one server in an upstream, NGINX will operate as a reverse proxy. If more than one server is in an upstream, NGINX will operate as a load balancer.
**You are supporting a web application that requires frequent deployments. When the application is updated, customers see it as being "offline" for several minutes. As a result, the application is receiving poor reviews. How can you improve the reliability of the application and increase customer satisfaction, while maintaining the deployment frequency?**
- this is the best choice. With multiple servers behind a load balancer, a site or application can be more reliable by continuing to respond to requests if one server goes down. This also gives site administrators some flexibility for maintenance since they can take one server offline to update software, for example, without taking the entire site offline. Depending on the needs of the application, as long as one server is online, the site will still be up. This will keep customers happy.


## NGINX security

- securing sites with nginx involves the following things :
  - Keep your os and software patched and updated.
  - Restrict access where possible
  - use passwords to protect sensitive information 
  - Use TLS(Transport layer security)/SSL(secure socket layer) to identify your sites and encrypt transmissions

#### Configure Allow and Deny directives
- HTTP access module has 1. Allow and 2. Deny 
- allow and Deny rules can be used in http server and location context of nginx configuration.
- Each allow and Deny specific patterns to match incomibg requests.
   - all
   - single IP address 192.168.1.1
   - CIDR(classless interdomain routing) block 192.168.1.0/24
   - CIDR is a method for representing a range of IP addresses

- Rules are applied in the order they are defined
- Deny rules should be placed after allow rules.

![image](https://user-images.githubusercontent.com/89054489/230754617-074ed110-5ada-4f2b-9bf6-9158155b20d6.png)



### secure a website with nginx
**scenario:** Secure a website with nginx
Solution :




## using NGINX with Docker

### Build a nginx container image


### Troubleshooting

Basic Nginx troubleshooting
This article shows some basic troubleshooting for Nginx, one of the most popular HTTP servers. The purpose is to fix some of the most common errors that may be present in your Nginx configuration.

Search for syntax errors or warnings in the configuration
Through a simple command you can verify the status of the Nginx configuration file: $ sudo systemctl config nginx The output will show if the configuration file is correct or, if it is not, it will show the file and the line where the problem is.

$ sudo systemctl config nginx
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
$ sudo systemctl config nginx
"worker_connections" directive is not allowed here in /etc/nginx/nginx.conf:12
nginx: configuration file /etc/nginx/nginx.conf test failed
In case you do not have the service command available in your system you can opt to use the -t Nginx parameter, which also tests the configuration file for correct syntax and then tries to open the files that are referred to in the configuration. $ sudo nginx -t

Check that Nginx is running
To check the Nginx service status you can use the following command: $ sudo systemctl status nginx You can also use the generic commands to validate the status of the service: $ sudo /etc/init.d/nginx status

Verify that the ports are open and the service is listening
Verify that you have the needed ports are open and to verify that the Nginx service is listening through them you can use the lsof command, ideally in the default ports 80 and 443.

$ sudo lsof -i :80 -s TCP:LISTEN
nginx   1305 nginx    6u  IPv4 1613873      0t0  TCP *:http (LISTEN)
nginx   1305 nginx    7u  IPv6 1613874      0t0  TCP *:http (LISTEN)
nginx   1306 nginx    6u  IPv4 1613873      0t0  TCP *:http (LISTEN)
nginx   1306 nginx    7u  IPv6 1613874      0t0  TCP *:http (LISTEN)
Check if Nginx processes requests
If Nginx is actually listening to the appropriate ports, the next step is to check if it is processing requests, which can be made by using the curl tool by using the IP, URL, or localhost if your setup listens on localhost:

$ curl -i http://127.0.0.1/nginx_status
HTTP/1.1 200 OK
Server: nginx/1.11.1
Date: Wed, 08 Aug 2021 11:36:43 GMT
Content-Type: text/plain
Content-Length: 97
Connection: keep-alive

Active connections: 1
server accepts handled requests
3 3 3
Reading: 0 Writing: 1 Waiting: 0
Check the logs
Check the last logs of the Nginx service. $ sudo tail -f /var/log/nginx/access.log /var/log/nginx/error.log

Check permissions
Make sure that Nginx has the appropriate permissions for accessing the needed files.

$ namei -om /usr/share/nginx/html/index.html
f: /usr/share/nginx/html/index.html
drwxr-xr-x root root /
drwxr-xr-x root root usr
drwxr-xr-x root root share
drwxr-xr-x root root nginx
drwxr-xr-x root root html
-rw-r--r-- root root index.html
Reload the service
In case you made changes to the configuration file that have not been applied you can reload the service, starting new Nginx processes, and shutting down gently the old workers to avoid a quick and aggressive shutdown. $ sudo service nginx reload For the quick shutdown that does not wait for processes to end, you can restart Nginx. $ sudo service nginx restart

Enable de debug mode
In the configuration file (usually /etc/nginx/nginx.conf) change the log level for the error_log directive:

server {
# stuff
error_log /var/logs/nginx/error.log debug;
# stuff
}
You can debug rewrite rules to see the processing results in the error log:

server {
# stuff
error_log /var/logs/nginx/error.log notice;
rewrite_log on;
# stuff
}
Verify the DNS resolution
Rules on /etc/hosts have priority over DNS resolutions. You can verify the DNS records with: $ host -t A website.com You can aslo check the complete DNS resolution: $ dig +trace website.com


## Using nginx with docker
- Container images are digital artifacts that has everything needed to run an application. includes Operating system , software, configurations, content that application needs to run
- Docker is one of the most popular frameworks for building, running and managing container images

`docker run` - use a container image to run a command
`docker build` - Build a container image from a dockerfile specification

Run an NGINX container image

`docker run --publish 80:80 nginx`

Here 80 is local port and 80 is container port respectively. nginx is the container image

**Build an NGINX container image**

Inorder to do this we are using Dockerfile. 

A **Docker file** is a text document that has instructions for building a container image.
 - It contains base image, commands needed to update and configure the base image, any commands needed to add the contents to the image.

Docker file

# #commnt
INSTRUCTION arguments
...
INSTRUCTION arguments

- As a best practice all Instructions are in capital letters and all arguments in lower case letters

|Common Instructions ||
|----|----|
| FROM | specifies the base image |
| RUN | Runs commands inside the container |
| COPY | copy the files from local system into the container |

Docker - NGINX Base image

#Dockerfile with NGINX<br>
FROM- nginx:latesh <br>
COPY ./index.html /usr/share/nginx/html/index.html

## Build an NGINX container image

docker build --tag myimage .

Here myimage is the image name and . is the build pathu

## challenge

Build an NGINX container image

The robots of Binaryville have asked you to build a container image for their website. Everything you need to build the image available in the exercise files. once you build the image. Use it on the container so, you can explore the Binaryville website  on your local system.

### Build an NGINX container image

1. Clone the execise files to your local system and review them <br>
2. Build an image with the "docker build" command <br>
3. Run the image with the "docker run" command <br>
4. use ports 443 on the container and your local system <br>
5. Browse the site to find familiar locations <br>






