# Launching a website on top of Kubernetes
**Project Description**
- Create container image that’s has Jenkins installed  using dockerfile  Or You can use the Jenkins Server on RHEL 8/7
-  When we launch this image, it should automatically starts Jenkins service in the container.
-  Create a job chain of job1, job2, job3 and  job4 using build pipeline plugin in Jenkins 
-  Job1 : Pull  the Github repo automatically when some developers push repo to Github.
- Job2 : 
    - By looking at the code or program file, Jenkins should automatically start the respective language interpreter installed image container to deploy code on top of Kubernetes ( eg. If code is of  PHP, then Jenkins should start the container that has PHP already installed )
    - Expose your pod so that testing team could perform the testing on the pod
    - Make the data to remain persistent ( If server collects some data like logs, other user information )
-  Job3 : Test your app if it  is working or not.
-  Job4 : if app is not working , then send email to developer with error messages and redeploy the application after code is being edited by the developer

# Let's understand some of the basic things

# What is Kubernetes?

![alt text](https://upload.wikimedia.org/wikipedia/commons/3/39/Kubernetes_logo_without_workmark.svg)

-Kubernetes is a portable, extensible, open-source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation. It has a large, rapidly growing ecosystem. Kubernetes services, support, and tools are widely available.

-The name Kubernetes originates from Greek, meaning helmsman or pilot. Google open-sourced the Kubernetes project in 2014. Kubernetes combines over 15 years of Google's experience running production workloads at scale with best-of-breed ideas and practices from the community.

# Why you need Kubernetes and what it can do
-Containers are a good way to bundle and run your applications. In a production environment, you need to manage the containers that run the applications and ensure that there is no downtime. For example, if a container goes down, another container needs to start. Wouldn't it be easier if this behavior was handled by a system?

-That's how Kubernetes comes to the rescue! Kubernetes provides you with a framework to run distributed systems resiliently. It takes care of scaling and failover for your application, provides deployment patterns, and more. For example, Kubernetes can easily manage a canary deployment for your system.

Kubernetes provides you with:

-Service discovery and load balancing
-Storage orchestration
-Automated rollouts and rollbacks
-Automatic bin packing
-Self-healing
-Secret and configuration management

# What is Jenkins and why we use it?

![alt text](https://www.hopetutors.com/wp-content/uploads/2019/05/jenkins_new_0.jpg)


-Jenkins is an open-source automation tool written in Java with plugins built for Continuous Integration purposes. Jenkins is used to build and test your software projects continuously making it easier for developers to integrate changes to the project, and making it easier for users to obtain a fresh build. It also allows you to continuously deliver your software by integrating with a large number of testing and deployment technologies.

-With Jenkins, organizations can accelerate the software development process through automation. Jenkins integrates development life-cycle processes of all kinds, including build, document, test, package, stage, deploy, static analysis, and much more.

-Jenkins achieves Continuous Integration with the help of plugins. Plugins allows the integration of Various DevOps stages. If you want to integrate a particular tool, you need to install the plugins for that tool. For example: Git, Maven 2 project, Amazon EC2, HTML publisher etc.

**After Knowing these technologies Let's start our project**



