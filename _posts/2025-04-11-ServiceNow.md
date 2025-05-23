---
title: "ServiceNow Learning Notes"
date: 2025-04-11
category: "ServiceNow"
---

## Table of contents
1. [Introduction](#introduction)
2. [ITIL](#itil)
3. [Cloud](#cloud)
4. [App Engine](#app-engine)
    1. [Request-fulfill workflow](#request-fulfill-workflow)
5. [NowAssist AI](#nowassist-ai)
    1. [NowAssist products](#nowassist-products)
    2. [NowAssist benefits](#nowassist-benefits)
    3. [NowAssist Admin console](#nowassist-admin-console)
    4. [NowAssist context menu](#nowassist-context-menu)
6. [Strategic Portfolio Management](#SPM)
    1. [What is strategic portfolio management?](#what-SPM)
    2. [A tour of main functionalities of SPM](#SPM-functionalities)

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
Access developer mode using  https://dev{developer Id}.service-now.com/.

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
<div style="text-align: center;">Fig. Create the data model</div>
</p>

* **Build the request form**

<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/Request-form.png?raw=true" alt="Form" title="Build the request form" width="100%" height="100%">
<div style="text-align: center;">Fig. Build the request form</div>
</p>

* **Create the request record producer**

<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/Request-record-producer.png?raw=true" alt="Request-record-producer" title="Create the request record producer" width="100%" height="100%">
<div style="text-align: center;">Fig. Create the request record producer</div>
</p>

* **Create the fulfiller workspace**

<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/Workspace.png?raw=true" alt="Workspace" title="Create the fulfiller workspace" width="100%" height="100%">
<div style="text-align: center;">Fig. Create the fulfiller workspace</div>
</p>

* **Set up the department approvers**

<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/Dept-approvers.png?raw=true" alt="Dept-approvers.png" title="Set up the department approvers" width="100%" height="100%">
<div style="text-align: center;">Fig. Set up the department approvers</div>
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

### NowAssist products <a name="nowassist-products"></a>

|Workflow|Business areas|Available product|
|---|---|---|
|Technology|The Technology workflow includes IT applications, such as IT services and operations, managing your strategy to deliver products and services, and platform security.|<a href="https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/concept/now-assist-landing-cmdb.html">Now Assist for Configuration Management Database (CMDB)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-application-portfolio-management/page/product/now-assist-ea/concept/now-assist-ea.html">Now Assist for Enterprise Architecture (EA)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-governance-risk-compliance/page/product/grc-common/concept/now-assist-for-irm.html">Now Assist for Integrated Risk Management (IRM)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-it-operations-management/page/product/now-assist-itom/concept/now-assist-itom.html">Now Assist for IT Operations Management (ITOM)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-it-service-management/page/product/now-assist-itsm/concept/now-assist-itsm.html">Now Assist for IT Service Management (ITSM)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-security-management/page/product/now-assist-security-incident/reference/now-assist-security-incident-landing.html">Now Assist for Security Incident Response</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/product/configuration-management/concept/now-assist-sgc-landing.html">Now Assist for Service Graph Connectors (SGC)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-it-asset-management/page/product/now-assist-sam/concept/now-assist-sam.html">Now Assist for Software Asset Management (SAM)</a> <br/> <a href="https://www.servicenow.com/docs/bundle/yokohama-it-business-management/page/product/now-assist-spm/concept/now-assist-spm.html">Now Assist for Strategic Portfolio Management (SPM)</a>|
|Finance & Supply Chain|The Finance & Supply Chain workflow supports purchase requisitions, sourcing requests, and request for products or services.|<a href="https://www.servicenow.com/docs/bundle/yokohama-source-to-pay-operations/page/product/accounts-payable-operations/concept/now-assist-apo.html">Now Assist for Accounts Payable Operations (APO)</a><br/><a href="https://www.servicenow.com/docs/bundle/yokohama-source-to-pay-operations/page/product/supplier-lifecycle-operations/concept/now-assist-slo.html">Now Assist for Supplier Lifecycle Operations (SLO)</a><br/><a href="https://www.servicenow.com/docs/bundle/yokohama-source-to-pay-operations/page/product/sourcing-procurement-operations/concept/now-assist-spo.html">Now Assist for Sourcing and Procurement Operations (SPO)</a>|
|Employee|The Employee workflow supports HR Service Delivery features.|<a href="https://www.servicenow.com/docs/bundle/yokohama-employee-service-management/page/product/now-assist-health-safety/reference/now-assist-hs-landing.html">Now Assist for Health and Safety</a><br/><a href="https://www.servicenow.com/docs/bundle/yokohama-employee-service-management/page/product/human-resources/concept/now-assist-hrsd.html">Now Assist for HR Service Delivery (HRSD)</a><br/><a href="https://www.servicenow.com/docs/bundle/yokohama-employee-service-management/page/product/legal-request-management/concept/now-assist-lsd-landing.html">Now Assist for Legal Service Delivery (LSD)</a><br/><a href="https://www.servicenow.com/docs/bundle/yokohama-employee-service-management/page/product/now-assist-wsd/concept/now-assist-wsd-landing.html">Now Assist for Workplace Service Delivery (WSD)</a>|
|Customer|The Customer workflow includes applications that support customer service, including field service, financial services, telecommunications and media, and the public service sector.|<a href="https://www.servicenow.com/docs/bundle/yokohama-customer-service-management/page/product/customer-service-management/concept/now-assist-csm.html">Now Assist for Customer Service Management (CSM)</a><br/><a href="https://www.servicenow.com/docs/bundle/yokohama-field-service-management/page/product/field-service-management/reference/now-assist-fsm.html">Now Assist for Field Service Management (FSM)</a><br/><a href="https://www.servicenow.com/docs/bundle/yokohama-financial-services-operations/page/product/fso-common/concept/now-assist-for-financial-services-operations.html">Now Assist for Financial Services Operations (FSO)</a><br/><a href="https://www.servicenow.com/docs/bundle/yokohama-government-industry/page/product/public-sector/concept/now-assist-for-psds.html">Now Assist for Public Sector Digital Services (PSDS)</a><br/><a href="https://www.servicenow.com/docs/bundle/yokohama-telecom-media-technology/page/product/tmt-spmc/reference/now-assist-spmc.html">Now Assist for Telecommunications, Media and Technology (TMT)</a>|
|Creator|The Creator workflow supports a variety of Platform tools and builders, including the following: 1. App Engine Studio 2. Now Platform scripting 3. Platform 4. Analytics 5. Service Catalog 6. Workflow Studio 7. RPA Hub 8. Process Mining|<a href="https://www.servicenow.com/docs/bundle/yokohama-build-workflows/page/administer/flow-designer/concept/now-assist-for-creator-landing.html">Now Assist for Creator</a>|

Now Assist products include some or all of the following foundational platform tools for Now Assist. For more information, see <a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-skills/concept/now-assist-on-now-platform.html">Now Assist skills in the Platform workflow</a>.

* Administrators install plugins, manage skills, and analyze usage and performance with the <a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-platform/concept/configuring-now-assist.html">Now Assist Admin console</a>.
* Users can take advantage of Now Assist skills by using the <a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-platform/concept/now-assist-panel-overview.html">Now Assist panel</a> on the instance.
* Use <a href="https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/ai-search/reference/now-assist-ais.html">Now Assist in AI Search</a> to generate answers for AI Search.
* Use <a href="https://www.servicenow.com/docs/bundle/yokohama-mobile/page/administer/tablet-mobile-ui/concept/now-assist-mobile-landing.html">Now Assist for Mobile</a> to run generative AI skills in a mobile environment.
* Use <a href="https://www.servicenow.com/docs/bundle/xanadu-application-development/page/script/now-assist-for-code/concept/now-assist-code-landing.html">Now Assist for Code</a> for code generation.
* Use <a href="https://www.servicenow.com/docs/bundle/yokohama-conversational-interfaces/page/administer/now-assist-in-va/concept/now-assist-in-va-landing.html">Now Assist in Virtual Agent</a> to create conversational catalog experiences and author topics that use LLM topic discovery.
* Developers can use the <a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/generative-ai-controller/concept/generative-ai-controller.html">Generative AI Controller</a> to integrate generative AI features in custom flows and conversations by using your own third-party large language model (LLM) licenses.

### NowAssist benefits <a name="nowassist-benefits"></a>

|Benefit|Feature|Users|
|---|---|---|
|Leverage the power of search with the Now LLM generative AI model to answer questions in user searches with actionable AI-generated summaries of relevant knowledge articles.|<a href="https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/ai-search/reference/now-assist-ais.html">Now Assist in AI Search</a>|Everyone|
|Install and configure Now Assist applications and the skills they provide.|<a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-platform/concept/configuring-now-assist.html">Now Assist Admin console</a>|Administrators|
|Choose which skills to turn on, and which users can access them.|<a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-platform/concept/configuring-now-assist.html">Now Assist Admin console</a>|Administrators|
|Monitor the usage and performance of generative AI features and capabilities offered under Now Assist.|<a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-analytics/concept/now-assist-analytics.html">Now Assist Analytics</a>|Administrators|
|Access generative AI skills in context through a user-friendly interface.|<a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-platform/concept/now-assist-panel-overview.html">Now Assist panel</a>|Everyone|
|Use Now Assist skills on mobile devices.|<a href="https://www.servicenow.com/docs/bundle/yokohama-mobile/page/administer/tablet-mobile-ui/concept/now-assist-mobile-landing.html">Now Assist for Mobile</a>|Everyone|
|Customize your workflows and use your own third-party LLM license.|<a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/generative-ai-controller/concept/generative-ai-controller.html">Generative AI Controller</a>|Administrators or developers|
|Use Now Assist in other platform features.|<a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-skills/concept/now-assist-on-now-platform.html">Now Assist skills in the Platform workflow</a>|Administrators or developers|
|Monitor Now Assist consumption on your instance.|<a href="https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/subscription-management/concept/monitoring-now-assist-usage.html">Monitoring Now Assist usage in Subscription Management</a>|Administrators|
|Code generation|<a href="https://www.servicenow.com/docs/bundle/xanadu-application-development/page/script/now-assist-for-code/concept/now-assist-code-landing.html">Now Assist for Code</a>|Developers|

### NowAssist Admin console <a name="nowassist-admin-console"></a>
The NowAssist Admin console contains everything that you need to install, configure, and learn about the different generative AI features on the Now Platform.

<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/now-assist-admin-console-overview.png?raw=true" alt="NowAssist Admin console" title="NowAssist Admin console" width="100%" height="100%">
<div style="text-align: center;">Fig. NowAssist Admin overview page</div>
</p>

NowAssist Admin workflow includes five steps:
1. **[Install plugins]** On the **Available for you** tab of the Settings page, you can review the available plugins and install the ones that are relevant to your business needs. Each plugin contains the skills that you can activate to enable generative AI features on your instance. 

**Available for you tab on the NowAssist Admin Settings > Plugins page**

2. **[Turn on the NowAssist panel]** The NowAssist panel integrates the Now Assist skills into the Next Experience UI. By turning on the NowAssist panel directly from the Now Assist Admin console, you enable agents to access skills from anywhere on the Now Platform.

3. **[Activate skills]** Skills are features that are created for a specific use case in a Now Assist application. Use the NowAssist Admin Features page to explore the skills that are available with your installed plugins. By selecting the **View details** button, you can see more information about each skill.

**Available NowAssist features and skills in the Technology workflow**

After deciding which skills best fit your business needs, you can activate them from the console. Some skills require configuration so that you can customize the skill to your needs, such as determining the skill inputs and triggers. You can select the skills that you want to configure in the NowAssist Admin Features page.

4. **[Review your Now Assist account settings]** The Now Assist Admin console Settings page enables you to set up language support, if you have Dynamic Translation enabled on your instance, and review your account details. Get up-to-date information about what plugins are available to you and the status of data sharing on your instance.

5. **[Monitor and analyze skill performance]** Use the metrics available on the Overview page to review the summaries, performance information, and issues that need your attention. 

### NowAssist context menu <a name="nowassist-context-menu"></a> (<a href="https://www.servicenow.com/docs/bundle/yokohama-intelligent-experiences/page/administer/now-assist-platform/concept/now-assist-write-overview.html">source</a>)
The **NowAssist context menu** leverages generative AI to enhance agents' writing tasks by summarizing, creating, and editing content across various applications in ServiceNow.

The NowAssist context menu is available on any field where the floating NowAssist button (<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/wwna-icon.png?raw=true" alt="floating Now Assist button" title="floating Now Assist button" width="2%" height="2%">) appears. If you start typing in the field, a menu appears with the available Now Assist context menu actions.

Something NowAssist context menu can do:
1. Chat window using the NowAssist context menu
2. Change request risk explanation using the NowAssist context menu
3. Content editing in Knowledge Base articles using the NowAssist content menu
4. Change Tone using NowAssist context menu
5. Limit the number of content refinement calls using the NowAssist context menu
6. Use the NowAssist context menu to compose or respond to emails with recommendations from Now Assist with generative AI template suggestions.
7. Use the NowAssist context menu to generate a record summary for the page, using Generative AI application assisted summarization capabilities in workspaces and UI16.
8. Use the NowAssist Context Menu dashboard to monitor the use of NowAssist Context Menu across the different applications. Key features include:
    1. Usage matrix: The count or number of times, NowAssist context menu has been used during the selected duration.
    2. Implicit feedback duration: The breakdown of feedback based on whether the response is inserted and closed during the selected time range. 
    3. Usage trend by skill: The total usage distribution based on the skills that use the NowAssist context menu. 
    4. Capacity Distribution: The capacity distribution based on the different applications that use the NowAssist context menu.
    5. Response by feedback: The feedback field based on the Generative AI logs. 
    6. Insights: View insights and suggestions for NowAssist usage.

<span style="color:red">TODO: Continue go through the NowAssist AI.</span>.

## Strategic Portfolio Management <a name="SPM"></a>

### What is strategic portfolio management? <a name="what-SPM"></a>
Strategic Portfolio Management (SPM) helps companies make smart decisions about where to invest their time, money, and people to support their big-picture goals.

Why is it important?
* It ensures investments (money and effort) are being used for things that truly matter to the business.
* It helps leaders see what's working and what’s not, so they can adjust quickly.
* It gives everyone a clear view of priorities, progress, and impact.

What are the benefits of SPM?
* Faster time to market
* Improved response time to disruptions
* Better alignment between strategy and execution
* Improved efficiency
* Cohesion of multiple disciplines
* Increased agility
* Improved speed overall
* Big-picture focus
* Ability to realise expected business value from digital initiatives

What are the steps in SPM?
* **Inventory**. First, assess and understand the strategic goals of the organisation, including both short- and long-term objectives. Second, take inventory of all available resources, including budgets and people. Lastly, review established priorities.
* **Analysis**. Select key business metrics through which they may gauge success.
* **Planning**.  Organisations develop a strategic portfolio plan that outlines the specific projects, programmes or initiatives that will be included in the portfolio. The plan should clearly define the goals and objectives of the portfolio, along with the key performance indicators (KPIs) that will be used to measure progress. Additionally, the plan must consider the allocation of resources, including budget, personnel and other assets, to ensure that the selected initiatives can be executed effectively. It is likewise important to consider emergent issues or other potential risks that may cause problems.
* **Execution**. This stage involves implementing the projects and programmes according to the established priorities and resource allocations. Post execution, ongoing management is essential to ensure that the portfolio remains aligned with the organisation's strategic objectives and adapts to changing circumstances.

What are SPM components?
* Operating model development
* IT portfolio management and enterprise portfolio management
* Financial management
* Risk and security management
* Enterprise architecture governance

Key applications and capabilitys:

|Name|Description|
|---|---|
|NowAssist for SPM|Break down barriers with generative AI to deliver customer value quickly.|
|<a href="https://www.servicenow.com/au/products/strategic-planning.html">Strategic Planning</a>|Connect strategy to execution with end-to-end planning in a single workspace.|
|<a href="https://www.servicenow.com/au/products/scenario-planning.html">Scenario Planning</a>|Simulate and compare investment scenarios to align your portfolio with your business strategy.|
|Investment Funding|Manage funds based on business needs and your organisation’s strategic objectives.|
|<a href="https://www.servicenow.com/au/products/agile-development.html">Agile Development</a>|Manage scrum or development work throughout the lifecycle from a unified backlog of tasks.|
|<a href="https://www.servicenow.com/au/products/scaled-agile-framework.html">Scaled Agile Framework</a>|Align Agile software and product development efforts for speed and efficiency.|
|<a href="https://www.servicenow.com/au/products/project-portfolio-management.html">Project Portfolio Management</a>|Gain visibility into traditional, agile and hybrid work to optimise portfolios.|
|<a href="https://www.servicenow.com/au/products/demand-management.html">Demand Management</a>|Capture, assess and manage demands from the business in one location.|
|<a href="https://www.servicenow.com/au/products/collaborative-work-management.html">Collaborative Work Management</a>|Empower teams and simplify work with a hub for planning, visualisation and collaboration.|
|<a href="https://www.servicenow.com/au/products/resource-management.html">Resource Management</a>|See staff availability, allocation and capacities for all work tracked in ServiceNow.|
|<a href="https://www.servicenow.com/au/products/innovation-management.html">Innovation Management</a>|Capture new ideas from across your organisation in a single location.|
|<a href="https://www.servicenow.com/au/products/digital-portfolio-management.html">Digital Portfolio Management</a>|Make informed decisions with a unified view of services, products and apps.|
|Release Management|Plan, design, build, configure and test hardware and software and software releases with precision.|
|<a href="https://www.servicenow.com/au/products/predictive-intelligence.html">Predictive Intelligence</a>|Simplify and accelerate everyday work with built-in machine learning.|
|<a href="https://www.servicenow.com/au/products/virtual-agent.html">Virtual Agent</a>|Resolve issues fast with an intelligent chatbot that understands simple, human language.|
|<a href="https://www.servicenow.com/au/products/process-mining.html">Process Mining</a>|Improve outcomes by optimising process flows to streamline work.|
|<a href="https://www.servicenow.com/au/products/performance-analytics.html">Performance Analytics</a>|Anticipate trends, prioritise resources and continuously improve with real-time analytics.|

### A tour of main functionalities of SPM <a name="SPM-functionalities"></a> (<a href="https://www.servicenow.com/au/products/strategic-portfolio-management.html">source</a>)

Portfolio Managers can track progress and monitor the status of all related work, key results and initiatives, as well as **Strategic Priorities**.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM1.png?raw=true" width="100%" height="100%">
</p>

From the roadmap, view your **AI Transformation Journey** to track progress, monitor performance, and prioritize high-impact initiatives that bring the most value to your business.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM2.png?raw=true" width="100%" height="100%">
</p>

Capacity planning ensures better visibility into resource utilization, reduces conflicts and boosts efficiency, allowing your team to focus on the most critical tasks.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM3.png?raw=true" width="100%" height="100%">
</p>

Develop customer-centric products by leveraging insights from statistics and customer sentiment trends while staying in sync with top trending feedback.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM4.png?raw=true" width="100%" height="100%">
</p>

Use **AI-powered Feedback Summarization** to analyze multiple records at once.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM5.png?raw=true" width="100%" height="100%">
</p>

**Multi-Feedback Summarization** allows you to make informed decisions faster and achieve the best outcomes.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM6.png?raw=true" width="100%" height="100%">
</p>

When change happens(it always does),SPM empowers your organization to adapt swiftly.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM7.png?raw=true" width="100%" height="100%">
</p>

Leverage real-time insights and flexible planning tools to pivot and reprioritize with precision.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM8.png?raw=true" width="100%" height="100%">
</p>

Click next to create scenario.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM9.png?raw=true" width="100%" height="100%">
</p>

Leverage real-time insights and flexible planning tools to pivot and reprioritize with precision.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM10.png?raw=true" width="100%" height="100%">
</p>

Simulate and compare alternative scenarios to choose the best path forward.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM11.png?raw=true" width="100%" height="100%">
</p>

With **Project Workspace**, execute work using any methodology like **Waterfall ,Agile or Hybrid** while enforcing standardized processes and best practices.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM12.png?raw=true" width="100%" height="100%">
</p>

Strategic Planning Workspace delivers products faster with improved time-to-market. That’s a real transformation!
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM13.png?raw=true" width="100%" height="100%">
</p>

Click the red pulse and click next to continue.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM14.png?raw=true" width="100%" height="100%">
</p>

With the **Export to PowerPoint** feature, you can share process and status updates effortlessly. Export informative details about your initiatives to PowerPoint instantly.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM15.png?raw=true" width="100%" height="100%">
</p>

Select the required Portfolio template.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM16.png?raw=true" width="100%" height="100%">
</p>

From the **Success Dashboard**, compare your performance against global benchmarks.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM17.png?raw=true" width="100%" height="100%">
</p>

You can also compare your metrics to the industry average of peers in order to measure success.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM18.png?raw=true" width="100%" height="100%">
</p>

Stay ahead of new demands by using **Generative AI** to simplify request capture, ensure data completeness, and streamline the evaluation process.
<p align="center">
<img src="https://github.com/icarusunimelb/personal-blogs/blob/main/_posts/figures/SPM19.png?raw=true" width="100%" height="100%">
</p>

## References
[1] https://www.tutorialspoint.com/servicenow/index.htm \
[2] https://www.servicenow.com/community/app-dev-get-started/ct-p/app-dev-get-started \
[3] https://www.ibm.com/think/topics/it-infrastructure-library#:~:text=ITIL%20stands%20for%20Information%20Technology,practices%20in%20IT%20service%20management. \
[4] https://www.servicenow.com/community/app-dev-get-started/ct-p/app-dev-get-started \
[5] https://www.servicenow.com/community/app-development-blog/app-engine-getting-started-guide-custom-application-development/ba-p/3223491?attachment-id=273369 \
[6] https://www.servicenow.com/au/ai.html \
[7] https://www.servicenow.com/au/standard/resource-center/infographic/ai-infographic-layout.html \
[8] https://www.servicenow.com/au/products/strategic-portfolio-management.html \
[9] https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/resource-center/infographic/info-turn-strategy-to-reality-spm.pdf \