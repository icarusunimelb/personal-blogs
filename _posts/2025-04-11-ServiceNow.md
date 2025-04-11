---
title: "Getting started with ServiceNow: A developer perspective"
date: 2025-04-11
---

## Table of contents
1. [Introduction](#introduction)
2. [ITIL](#itil)
3. [Cloud](#cloud)
4. [App Engine](#app-engine)
    1. [Request-fulfill workflow](#request-fulfill-workflow)

## Introduction <a name="introduction"></a>
ServiceNow is a cloud based platform, which was mainly developed for workflow and process automation as per the Information Technology Infrastructure Library (ITIL) principles. However, it is highly customisable and also can be used for other purposes. This tutorial will primarily focus on its basic concepts, App Engine, NowAssist AI, and Strategic Portfolio Management modules.

## ITIL <a name="itil"></a>
ITIL is a library of best practices that are employed in IT service management (ITSM)—the practice of planning, implementing, managing and optimizing information technology services to meet the needs of users and help organizations achieve their business goals.

ITIL can be divided into five main stages, including **Service Strategy**, **Service Design**, **Service Transition**, **Service Operation**, and **Continual Service Improvement**. Every stage has a specific role to play in a service life cycle and form the skeleton of ITIL. For the details, please check <a href="https://www.tutorialspoint.com/servicenow/servicenow_itil.htm"> Ref. [1] </a>. 

The lastest ITIL edition, ITIL 4 consists of 34 practices that are grouped into 3 main categories: 1. **General management practices**, 2. **Service management practices**, and 3. **Technical management practices**. For the details, please check <a href="https://www.ibm.com/think/topics/it-infrastructure-library#:~:text=ITIL%20stands%20for%20Information%20Technology,practices%20in%20IT%20service%20management"> Ref. [3] </a>. 

The benefits of ITIL are as follows:
* Stronger alignment between IT and business strategy
* Improved customer satisfaction and service delivery
* Increased transparency and visibility into IT processes and services
* Budgeting guidance
* Reduced IT costs
* Enhanced communication within teams and across stakeholders

## Cloud <a name="cloud"></a>
Here we briefly introduce cloud service models, which are categorised based on the services offered by the cloud service providers.
* **Infrastructure as a service (IaaS)**. This is the most fundamental level of cloud service, where in customer only takes computing resources or virtual hardware like storage, CPU, RAM, etc. from the cloud service providers.
* **Platform as a service (PaaS)**. This is one level further to IaaS. Here, along with the computing resources/virtual hardware, operating system, some software service and tools are also provided by the cloud service providers.
* **Software as a service (SaaS)**. This service model offers fully functional, ready to use software over the internet.

ServiceNow is a highly flexible application which provides the option of PaaS as well as SaaS. Its SaaS offering provides fully functional workflow automation and ITSM tools, while its PaaS offering, allows the user to develop a custom application on the top of existing suite, as per the business requirement.

## App Engine <a name="app-engine"></a>
Access developer mode using  <a href="https://dev315586.service-now.com/"> https://dev315586.service-now.com/</a>.

### Request-fulfill workflow <a name="request-fulfill-workflow"></a>
The request-fulfill workflow is the backbone of ServiceNow applications, as it provides a structured mechanism for managing service requests and incidents. In the request-fulfill workflow, ServiceNow generally categorizes the users into two distinct personas: Requestors and Fulfillers.
* **Requestors**. A Requestor is an end user who submits service requests and interacts with the platform primarily to seek assistance or resources. Their role is focused on initiating requests. 
* **Fulfillers**. A Fulfiller is responsible for processing, managing, and resolving service requests or incidents submitted by requestors. They ensure that business operations run smoothly by addressing user needs efficiently.

Starting with a request-fulfiller workflow is an effective way to achieve positive outcomes by aligning platform capabilities with business needs and enabling rapid application development. This approach allows you to tailor an application to meet specific requirements. The recommended first phase includes:
1. **Creating a Tailored Data Model**: Designing data structures that align with the department’s unique processes and requirements.
2. **Developing Record Producers**: Setting up user-friendly request submission forms to streamline how users make service requests.
3. **Creating Fulfiller Workspace**: Configuring dashboards and views to enhance productivity for fulfillers.
4. **Automating Processes Using Flow Designer**: Implementing automation rules to reduce manual work, enforce business policies, and ensure timely resolution of requests.

Some key operations:
* **Create the data model**

<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/Data-model.png?raw=true" alt="Data" title="Create the data model" width="100%" height="100%">
<div style="text-align: center;">Fig.1. Create the data model</div>
</p>

* **Build the request form**

<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/Request-form.png?raw=true" alt="Form" title="Build the request form" width="100%" height="100%">
<div style="text-align: center;">Fig.2. Build the request form</div>
</p>

* **Create the request record producer**

<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/Request-record-producer.png?raw=true" alt="Request-record-producer" title="Create the request record producer" width="100%" height="100%">
<div style="text-align: center;">Fig.3. Create the request record producer</div>
</p>

* **Create the fulfiller workspace**




For the details, please check <a href="https://www.servicenow.com/community/app-development-blog/begin-with-a-request-fulfill-workflow/ba-p/3189777"> Ref. [4] </a> and <a href="https://www.servicenow.com/community/app-development-blog/app-engine-getting-started-guide-custom-application-development/ba-p/3223491?attachment-id=273369"> Ref. [5] </a>.

## References
[1] https://www.tutorialspoint.com/servicenow/index.htm \
[2] https://www.servicenow.com/community/app-dev-get-started/ct-p/app-dev-get-started \
[3] https://www.ibm.com/think/topics/it-infrastructure-library#:~:text=ITIL%20stands%20for%20Information%20Technology,practices%20in%20IT%20service%20management. \
[4] https://www.servicenow.com/community/app-dev-get-started/ct-p/app-dev-get-started \
[5] https://www.servicenow.com/community/app-development-blog/app-engine-getting-started-guide-custom-application-development/ba-p/3223491?attachment-id=273369