# XL Release Example Templates and Demos

This community project contains a number of XL Release example templates that can be used as a learning tool. Although none of the templates can be used 'as is' to create a runnable release, they can be imported into either your own XL Release instance or the provided docker-ized XL Release, giving you an opportunity to explore and experiment with various XLR template configurations and tasks.

Also listed are links to other projects that include community plugin demos and XebiaLab Blueprints, both offical and community.

## Usage

You can import and then view the templates included in this project by running XLR in docker. The docker-compose file, included in this project, will start up XLR and load any XLR Community plugins that have been placed in the project 'your project root directory'/docker/plugin. You can then log into XLR and then import the example templates.

Note: The examples listed below that are from XebiaLabs Community Plugins or Blueprints will have specific information about running those demos in their respective README files. Once you have a demo running, you can chose to export the XLR demo template using the XLR User Interface.

How to install - prerequisites, including 'Clone this project to your machine'
Installing plugins
How to use the docker image
How to tell what type of task - screenshots too

### To run the included XLR in Docker

1. You will need to have Docker and Docker Compose installed.
2. Clone this project to your machine
3. The XL-Release image will use the community license. Note that by using this license, you are accepting the [End User License Agreement](https://dist.xebialabs.com/public/legal/eula-artifacts-v10.txt). If you prefer to use your own license, modify the docker-compose.yml file.
4. If an XLR plugin is required to import the template, you can place the plugin release file in the xlr-template-examples/docker/plugins directory. When XLR starts up in docker, the plugin will be automatically installed into the running XLR instance.
5. XL Release will run on the [localhost port 15516](http://localhost:15516/).
6. The XL Release username / password is admin / admin. 
7. Open a terminal in the the xlr-template-examples/docker directory and run the following command  

```bash
docker-compose up
```

### Import an example template

After XLR starts up, log in using the admin / admin credentials and then use the XLR 'Import Template' feature to import the template files (.xlr) found in the various folders with the xlr-template-examples/templates directory. [How to import a template file](https://docs.xebialabs.com/v.9.6/release/how-to/import-a-release-template/) These examples are view-only; they are not runnable as configured.



To shut down and remove the docker containers, in the src/test/resources/docker/initialize/data directory, run

```bash
docker-compose down
```


---

## Example Templates Located in this Project

You can run XLR in Docker (instructions included in this project), and then import the template. The templates are 'view only' and are not runnable. Place any necessary jars needed for template importation in the 'cloned project root directory'/docker/plugin directory. Follow the directions shown above to start up and import the .xlr file that contains the template you wish to view.

| Template | Notable Features | Requires Plugin To Import | Derived From |
| --- | --- | --- | --- |
| Webshop - [Master Release](/templates/WebshopYouTube/Webshop%20Master%20Release%20Process.xlr)/[Sub Release](/templates/WebshopYouTube/Webshop%20Subrelease%20Process.xlr) | - Something here <br/> - And another<br/>- Something else | No | [YouTube Video Link](https://www.youtube.com/watch?v=67e4TCRa9Ho) |
| [Local Docker Deployment](/templates/LocalDockerDeployment/localDockerDeployment.xlr) | Deploys an application to local Docker an then optionally undeploys it | No | [XebiaLabs Blueprint](https://github.com/xebialabs/blueprints/tree/master/docker/simple-demo-app)
| Microservice On Amazon EKS - [deploy](/templates/LocalDockerDeployment/test-app-ci-cd.xlr), [destroy](/templates/LocalDockerDeployment/test-app-destroy.xlr) | Deploys an application to local Docker an then optionally undeploys it | No | [XebiaLabs Blueprint](https://github.com/xebialabs/blueprints/tree/master/docker/simple-demo-app)

---

## Demos From Community Plugin Projects

The table contains a list of 'See It Work' plugins, meaning these plugins have been enhanced to include functionality that makes it easy to spin up and configure a dockerized version of the XebiaLabs platform with the plugin already installed. Using the provided test data, you can then try out the plugin features, including importing/viewing templates and creating runnable demo releases.

Links provided go directly to the plugin project where you will find detailed instructions about how to run a demo in Docker.

| Plugin | Notable Features |
| --- | --- |
| [xlr-ansible-tower-plugin](https://github.com/xebialabs-community/xlr-ansible-tower-plugin) | - This plugin enables Ansible Tower job execution from XL Release <br/> - Task: Launch Job<br/>- Task: Synchronize Inventory |
| [xlr-bamboo-plugin](https://github.com/xebialabs-community/xlr-bamboo-plugin) | - This plugin allows XL Release to run a Bamboo plan, create a Bamboo Release or trigger a Bamboo deployment <br/> - Task: Run Plan<br/>- Task: Create Release<br/>- Task: Trigger Deployment |
| [xlr-cherwell-plugin](https://github.com/xebialabs-community/xlr-cherwell-plugin) | - This plugin offers an interface from XL Release to Cherwell Server <br/> - Task: Get Team List<br/>- Task: Create Business Object<br/>- Task: Get Business Object<br/>- Task: Update Business Object<br/>- Task: Poll Business Object for field value change |
| [xlr-release-trigger-api](https://github.com/xebialabs-community/xlr-release-trigger-api) | - The plugin is an enhancement of the standard REST API in that the XLR template for the release and the release folder can be referenced within the POST parameters using an abstracted key name rather than by id  |
| [xlr-selenium-plugin](https://github.com/xebialabs-community/xlr-selenium-plugin) | - The plugin will run python based selenium scripts on a remote host <br/> - Task: Run a Single Selenium Test Case<br/>- Task: Run One or More Tests Retrieved from a Remote Repository |
| [xlr-variable-setter-plugin](https://github.com/xebialabs-community/xlr-variable-setter-plugin) | - The plugin provides a number of ways to dynamically populate Release variables <br/> - Task: Set Variables from Remote File<br/>- Set Variables from another Variable Source |
| [xlr-ucd-plugin](https://github.com/xebialabs-community/xlr-ucd-plugin) | - This plugin offers an interface from XL Release to Urban Code Deploy Server <br/> - Task: Application Process Request<br/>- Task: Application Process Request Status<br/>- Task: Synchronous Application Process Request<br/>- Task: List System Configuration |


---

## Demos From XebiaLabs Official Blueprint Projects

[XebiaLabs Official Blueprints](https://docs.xebialabs.com/v.9.7/release/concept/xebialabs-blueprints/)

| Blueprint | Notable Features |
| --- | --- |
| [Data Lake Solution on Amazon EC2](https://github.com/xebialabs/blueprints/tree/master/aws/datalake) | - AWS offers a sample Data Lake Solution that shows how you can store both structured and unstructured data in a centralized repository on Amazon Elastic Compute Cloud (EC2), which provides resizable compute capacity in the cloud. Use this blueprint to deploy the sample Data Lake Solution on EC2 using CloudFormation, which defines the infrastructure that will run on EC2. |
| [Microservice Application on Amazon EKS](https://github.com/xebialabs/blueprints/tree/master/aws/microservice-ecommerce) | Amazon Elastic Container Service for Kubernetes (EKS) allows you to deploy, manage, and scale containerized applications in the cloud using Kubernetes. Use this blueprint to deploy a sample microservice-based application on EKS. |
| [Amazon EKS Cluster](https://github.com/xebialabs/blueprints/tree/master/aws/basic-eks-cluster) | Amazon Elastic Container Service for Kubernetes (EKS) allows you to deploy, manage, and scale containerized applications in the cloud using Kubernetes. Use this blueprint to provision a simple EKS cluster. The release template that the blueprint generates provisions a new cluster. |
| [Amazon Lambda](https://github.com/xebialabs/blueprints/tree/master/aws/basic-lambda) | AWS Lambda lets you run code without provisioning or managing servers. You pay only for the compute time you consume - there is no charge when your code is not running. Use this blueprint to provision a basic Lambda function using a CloudFormation Stack. |
| [Monolithic Application on Amazon ECS](https://github.com/xebialabs/blueprints/tree/master/aws/monolith-terraform) | Amazon Elastic Container Service (ECS) is a container orchestration service for Docker-enabled applications. It works with AWS Fargate, a compute engine that allows you to run containers on ECS without having to manage servers or clusters. Use this blueprint to deploy a sample monolithic application on ECS with the Fargate launch type. |
| [Basic GKE Cluster](https://github.com/xebialabs/blueprints/tree/master/gcp/basic-gke-cluster) | Google Kubernetes Engine (GKE) allows you to deploy, manage, and scale containerized applications in the cloud using Kubernetes. Use this blueprint to provision a GKE cluster using Terraform. |
| [Microservice Application on GKE](https://github.com/xebialabs/blueprints/tree/master/gcp/microservice-ecommerce) | Google Kubernetes Engine (GKE) allows you to deploy, manage, and scale containerized applications in the cloud using Kubernetes. Use this blueprint to deploy a sample microservice-based application on GKE using Terraform, which defines the infrastructure that will run on GKE. |
| [Basic AKS Cluster](https://github.com/xebialabs/blueprints/tree/master/azure/basic-aks-cluster) | Azure Kubernetes Service (AKS) manages your hosted Kubernetes environment to deploy and manage containerized applications. Use this blueprint to provision a simple AKS cluster using Terraform, which defines the infrastructure that will run on AKS. |
| [Azure App Service](https://github.com/xebialabs/blueprints/tree/master/azure/app-service-docker-app) | Azure App Service allows you to deploy, manage, and scale web applications in the cloud. Use this blueprint to deploy a Docker-based web application to Azure App Service using Terraform. |
| [Microservice Application on Azure Kubernetes Service](https://github.com/xebialabs/blueprints/tree/master/azure/microservice-ecommerce) | Use this blueprint to deploy a sample microservice-based application on AKS using Terraform, which defines the infrastructure that will run on AKS. The release template that the blueprint generates connects to an existing AKS cluster or provisions a new cluster and deploys a sample application to it. |
| [Basic ARM Template](https://github.com/xebialabs/blueprints/tree/master/azure/basic-arm-template) | Azure Resource Manager (ARM) allows users to deploy applications to Azure using declarative JSON templates. In the DevOps as Code CLI, you can use the Basic ARM template blueprint to run blueprints on platforms hosted on Azure, by creating ARM templates. This can greatly simplify the process of provisioning resources from Deploy and Release in an Azure environment. |
| [Local Docker Deployment](https://github.com/xebialabs/blueprints/tree/master/docker/simple-demo-app) | Use this blueprint to deploy a Docker application with front-end and back-end services to Docker running locally. |
| [Docker Single Container Application](https://github.com/xebialabs/blueprints/tree/master/docker/application) | Use this blueprint to define a package that deploys a single Docker container. |
| [Docker Environment](https://github.com/xebialabs/blueprints/tree/master/docker/environment) | Use this blueprint to define an environment for your Docker engine in Deploy. |
| [Composed Docker Deployment](https://github.com/xebialabs/blueprints/tree/master/docker/composable-demo) | Use this blueprint to deploy a simple Docker application to Docker running locally. |
| [DevOps Platform](https://github.com/xebialabs/blueprints/tree/master/xl-devops-platform) | Use this blueprint to create an Deploy instance, an Release instance and a Docker proxy for deploying containers to Docker. |
| [Kubernetes Application](https://github.com/xebialabs/blueprints/tree/master/kubernetes/application) | Use this blueprint to define an environment for a Kubernetes cluster in Deploy. |
| [Run Your DevSecOps Pipeline](https://github.com/xebialabs/blueprints/tree/master/devsecops/security-scanning) | Use this blueprint to configure security scanning tools and an out-of-the-box security dashboard that provides immediate insight into code quality for teams, managers, and auditors. |
| [Dictionaries and Secret Stores](https://github.com/xebialabs/blueprints/tree/master/showcases/dictionaries-and-secret-stores) | This blueprint includes the resources needed to set up a basic deployment of the DevOps Platform to an Azure environment, with the option to store sensitive values either in a password dictionary, or in one of the following secret stores: CyberArk Conjur, HashiCorp Vault |

---

## Demos From XebiaLabs Community Blueprint Projects

[XebiaLabs Community Blueprints](https://github.com/xebialabs-community/xl-blueprints-community)

| Blueprint | Notable Features |
| --- | --- |
| [AWS Wildfly Application](https://github.com/xebialabs-community/xl-blueprints-community/tree/master/aws-ec2wildfly-app-demo) | This blueprint demo will show you how to download, customize and then apply a blueprint to XL Release and XL Deploy. The applied blueprint configures an XL Release \ XL Deploy deployment pipeline that can be used to spin up an instance of an AWS Wildfly AMI in your AWS account and then deploy a simple application to that instance. |