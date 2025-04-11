---
title: "ServiceNow Learning Notes"
date: 2025-04-11
---

## Table of contents
1. [Introduction](#introduction)
2. [ITIL](#itil)
3. [Cloud](#cloud)
4. [App Engine](#app-engine)
    1. [Request-fulfill workflow](#request-fulfill-workflow)
5. [NowAssist AI](#nowassist-ai)

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

<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/Workspace.png?raw=true" alt="Workspace" title="Create the fulfiller workspace" width="100%" height="100%">
<div style="text-align: center;">Fig.3. Create the fulfiller workspace</div>
</p>

* **Set up the department approvers**

<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/Dept-approvers.png.png?raw=true" alt="Dept-approvers.png" title="Set up the department approvers" width="100%" height="100%">
<div style="text-align: center;">Fig.3. Set up the department approvers</div>
</p>

For the details, please check <a href="https://www.servicenow.com/community/app-development-blog/begin-with-a-request-fulfill-workflow/ba-p/3189777"> Ref. [4] </a> and <a href="https://www.servicenow.com/community/app-development-blog/app-engine-getting-started-guide-custom-application-development/ba-p/3223491?attachment-id=273369"> Ref. [5] </a>.

* **Add the workflow with flow designer**

<span style="color:red">TODO: Continue go through the App Engine lab from page 22.</span>.

## NowAssist AI <a name="nowassist-ai"></a>

ServiceNow's AI product suite primarily includes the following three components:
1. **Now Assist** – A generative AI tool that instantly creates new content by learning patterns from existing data. It helps users resolve issues, answer questions, and obtain relevant support efficiently.
2. **AI Agents** – Agentic AI systems capable of autonomously performing tasks. These agents assist in troubleshooting, decision-making, and interacting with their environments.
3. **Vitural agent** – An intelligent chatbot.

ServiceNow has developed its own domain-specific LLMs that are trained and fine-tuned on ServiceNow customer use cases on the Now Platform. Additionally, the company supports third-party GenAI models including Microsoft Copilot, Azure OpenAI, IBM WatsonX, OpenAI and Google Gemini. ServiceNow also supports LLMs provided by its customers to give them the flexibility for a wide range of use cases.

This section will focus on NowAssist.

To enable NowAssist, please check <a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-platform/concept/platform-now-assist-landing.html">Guideline for NowAssist</a>.

### NowAssist products

3:20

|Workflow|Business areas|Available product|
|---|---|---|
|Technology|The Technology workflow includes IT applications, such as IT services and operations, managing your strategy to deliver products and services, and platform security.|<a href="https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/concept/now-assist-landing-cmdb.html">Now Assist for Configuration Management Database (CMDB)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-application-portfolio-management/page/product/now-assist-ea/concept/now-assist-ea.html">Now Assist for Enterprise Architecture (EA)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-governance-risk-compliance/page/product/grc-common/concept/now-assist-for-irm.html">Now Assist for Integrated Risk Management (IRM)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-it-operations-management/page/product/now-assist-itom/concept/now-assist-itom.html">Now Assist for IT Operations Management (ITOM)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-it-service-management/page/product/now-assist-itsm/concept/now-assist-itsm.html">Now Assist for IT Service Management (ITSM)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-security-management/page/product/now-assist-security-incident/reference/now-assist-security-incident-landing.html">Now Assist for Security Incident Response</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/concept/now-assist-sgc-landing.html">Now Assist for Service Graph Connectors (SGC)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-it-asset-management/page/product/now-assist-sam/concept/now-assist-sam.html">Now Assist for Software Asset Management (SAM)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-it-business-management/page/product/now-assist-spm/concept/now-assist-spm.html">Now Assist for Strategic Portfolio Management (SPM)</a>|
|Finance & Supply Chain|The Finance & Supply Chain workflow supports purchase requisitions, sourcing requests, and request for products or services.|<ul> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-source-to-pay-operations/page/product/accounts-payable-operations/concept/now-assist-apo.html">Now Assist for Accounts Payable Operations (APO)</a></li> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-source-to-pay-operations/page/product/supplier-lifecycle-operations/concept/now-assist-slo.html">Now Assist for Supplier Lifecycle Operations (SLO)</a></li> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-source-to-pay-operations/page/product/sourcing-procurement-operations/concept/now-assist-spo.html">Now Assist for Sourcing and Procurement Operations (SPO)</a></li> </ul>|
|Employee|The Employee workflow supports HR Service Delivery features.|<ul> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-employee-service-management/page/product/now-assist-health-safety/reference/now-assist-hs-landing.html">Now Assist for Health and Safety</a></li> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-employee-service-management/page/product/human-resources/concept/now-assist-hrsd.html">Now Assist for HR Service Delivery (HRSD)</a></li> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-employee-service-management/page/product/legal-request-management/concept/now-assist-lsd-landing.html">Now Assist for Legal Service Delivery (LSD)</a></li> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-employee-service-management/page/product/now-assist-wsd/concept/now-assist-wsd-landing.html">Now Assist for Workplace Service Delivery (WSD)</a></li> </ul>|
|Customer|The Customer workflow includes applications that support customer service, including field service, financial services, telecommunications and media, and the public service sector.|<ul> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-customer-service-management/page/product/customer-service-management/concept/now-assist-csm.html">Now Assist for Customer Service Management (CSM)</a></li> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-field-service-management/page/product/field-service-management/reference/now-assist-fsm.html">Now Assist for Field Service Management (FSM)</a></li> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-financial-services-operations/page/product/fso-common/concept/now-assist-for-financial-services-operations.html">Now Assist for Financial Services Operations (FSO)</a></li> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-government-industry/page/product/public-sector/concept/now-assist-for-psds.html">Now Assist for Public Sector Digital Services (PSDS)</a></li> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-telecom-media-technology/page/product/tmt-spmc/reference/now-assist-spmc.html">Now Assist for Telecommunications, Media and Technology (TMT)</a></li> </ul>|
|Creator|The Creator workflow supports a variety of Platform tools and builders, including the following: 1. App Engine Studio 2. Now Platform scripting 3. Platform 4. Analytics 5. Service Catalog 6. Workflow Studio 7. RPA Hub 8. Process Mining|<ul> <li><a href="https://www.servicenow.com/docs/bundle/yokohama-build-workflows/page/administer/flow-designer/concept/now-assist-for-creator-landing.html">Now Assist for Creator</a></li> </ul>|

<a href="https://www.servicenow.com/docs/bundle/xanadu-application-development/page/script/now-assist-for-code/concept/now-assist-code-landing.html"> Guideline for code generation. </a>


## References
[1] https://www.tutorialspoint.com/servicenow/index.htm \
[2] https://www.servicenow.com/community/app-dev-get-started/ct-p/app-dev-get-started \
[3] https://www.ibm.com/think/topics/it-infrastructure-library#:~:text=ITIL%20stands%20for%20Information%20Technology,practices%20in%20IT%20service%20management. \
[4] https://www.servicenow.com/community/app-dev-get-started/ct-p/app-dev-get-started \
[5] https://www.servicenow.com/community/app-development-blog/app-engine-getting-started-guide-custom-application-development/ba-p/3223491?attachment-id=273369 \
[6] https://www.servicenow.com/au/ai.html \
[7] https://www.servicenow.com/au/standard/resource-center/infographic/ai-infographic-layout.html \