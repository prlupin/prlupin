

## Executive Summary

NationalHealthCare.gov is a network-centric software system. Its system architecture is complex and could not be described from a single viewpoint. The Department of Defense Architecture Framework (DoDAF) models are used to create the multiple viewpoints architecture for this system. By using DoDAF models, the system architecture is represented by:

- Operational Viewpoint (OV)
	- OV-1: High-Level Operational Concept Graphic
	- OV-2: Operational Resource Flow Description
	- OV-5b: Operational Activity
- System Viewpoint (SV)
	- SV-1: Systems Interface Description
	- SV-2: Systems Resource Flow Description
	- SV-4: Systems Functionality Description
- Service Viewpoint (SvcV)
	- SvcV-1: Services Context Description
	- SvcV-2: Services Resource Flow Description
	- SvcV-4: Services Functionality Description


## Introduction

On March 23, 2010, President Obama signed into law The Patient Protection and Affordable Care Act (ACA), which require every American to obtain health insurance or pay a penalty[[1]](#ref1). The purpose of the ACA is to make insurance more affordable by reducing insurance premiums and out-of-pocket cost for Americans who previously could not afford insurance[[1]](#ref1). Furthermore, the law prevents insurance companies from denying Americans health insurance based on pre-existing conditions. Additional benefits of the ACA includes but not limited to no-cost preventative care, coverage for young adults under the age of 26, and no cancellation or lifetime limits on care.

The purpose of this Architecture Specification Document (ASD) is to describe the operational, system, and service views of the healthcare marketplace. The healthcare marketplace provides American individuals and families another way to purchase healthcare insurance online through state or federal healthcare marketplace. Low and middle class Americans will have the option to purchase federally regulated and subsidized insurance through the online marketplace. For individuals who fall below the Federal Poverty Level, the marketplace will help them determine the amount of subsidies or Premium Tax Credit.  

The healthcare marketplace (referred to as the healthcare.gov) shall provide Americans with online capabilities to compare health plans, enroll in a chosen health plan, and calculate any subsidies or credits. The marketplace shall display available plans to User based on the types of plans including Bronze, Silver, Gold and Platinum. The marketplace shall provide an intuitive user interface that allows User to compare the different types of plans based on their medical needs. In addition, the marketplace shall provide User the option to enroll in the chosen health plan. The marketplace shall validate User’s eligibility including but not limited to the validity of the SSN, legal resident, employment status, income, and citizenship.  Furthermore, the marketplace shall calculate any subsidies and/or credits that the User qualifies based on employment and income levels.

Currently, there are no web-based healthcare marketplaces that are available for the general public to purchase healthcare plan to meet the ACA requirements.  Hence, the government is seeking a contractor to build a cloud-based healthcare marketplace that allows users to browse, apply, and purchase healthcare plans.  Specifically, the healthcare marketplace needs to address the following challenges:

1.	Provide users with a user-friendly web application interface to browse, compare, apply, and purchase healthcare plans online using the Internet
2.	Establish call centers including faith based organizations, government affiliates, etc. to help users requiring assistance or those who do not have sufficient Internet connection/bandwidth access to the healthcare marketplace
3.	Collect and update healthcare plans from healthcare providers and make the plans available on the healthcare marketplace
4.	Create login accounts for users to manage their healthcare plans and user profile
5.	Ability for the user to apply for the ACA
6.	Calculate healthcare subsidies in real-time as defined by the ACA requirements
7.	Leverage third-party services and products to streamline the application and plan purchase process including verification and online payment services
8.	Report individuals and their employers to the Internal Revenue Service

Moreover, healthcare providers will offer users’ healthcare plans through the marketplace. These plans will be received and updated by the healthcare.gov system.  BPC intends to leverage commercial-off-the-shelf provides and services to expedite the development effort and minimize capital cost. These third-party services include employment and income verification, address verification, and e-commerce payment.

The development of this healthcare marketplace will be funded through the Department of Health and Human Services (HHS) [[2]](#ref2). Specifically, the Centers for Medicare and Medicaid Services (CMS) have obligated in excess of $840 million dollars to develop the healthcare marketplace. It is the intent of the Blue Point Consulting to develop the healthcare marketplace in concert with Accenture; and to maintain the website on an ongoing basis.

Blue Point Consulting (BPC) was founded in 2005 and headquarters in Reston, Virginia as a software development company. BPC was awarded their first contract through the Small Business Innovation Research (SBIR) program. BPC received Phase I and Phase II funding by the US Navy to research and develop innovative methods to seamlessly integrate a common operating picture across various government agencies using cloud computing technologies. Through the initial SBIR program, BPC have grown to a 400 employees with annual revenue exceeding $50 million dollars.  We believe with our software development and cloud computing expertise will help the Accenture team build a user-friendly, robust, and highly available online healthcare marketplace.

In support of this project, BPC has hired 35 new information technology professionals, in addition to our current team, to design and develop this web-based healthcare marketplace.  The team consist but not limited to a program manager, project manager, requirements analysts, system architecture, software developers, network engineers, quality assurance and control specialist, release and deployment engineers.  The team will support all phases of the software development life-cycle until the initial baseline release.  After the initial production release, BCP will reduce the team size to address bug fixes and future enhancements and commensurate with the price schedule.

BPC intends to maintain and enhance the healthcare marketing place after the initial development effort.  This effort is part of the three base year contract. The maintenance and enhancement of the healthcare marketplace includes new functionality, bug fixes to the website, data updates from third-party providers, generate and deliver reports to the internal revenue service, resolve account management issues, and address payment processing problems.  The intent of these services are: 1) to provide users of the healthcare marketplace with a good buying experience, 2) provider users numerous options to purchase the healthcare plans, 3) provide the latest healthcare plans and cost, 4) provide a highly-available, reliable, and intuitive application, and 5) meet the ACA requirements.

BPC proposed a firm-fixed priced contract to support this project, using the labor categories and software development licenses outlined in the General Administration Services (GSA) pricing. All travel expenses will be considered out-of-pocket and billed in the government as required.  All hardware and server software licenses will be considered outside the scope of this project. The price proposal is a three year base contract with 5 option years as specified in the cost proposal. BPC believes that we are offering the government with the best solution and best value to develop a highly robust system within a very aggressive timeframe. In addition, since BPC is a Virginia based company, this project will help generate revenue for the Commonwealth and for US small businesses.


## Architecture Specification

This section describes the system architecture of the healthcare.gov system including the operational views, system views, and service views. This document describes the scope of the architecture, determines the data required to support the system, conducts and analyzes the architectural impact of the system, and identifies key stakeholders.

## Operational Viewpoint

### OV-1: High-Level Operational Concept Graphic

The high-level operational concept view depicted in figure 1 below shows how the cloud-based healthcare marketplace will operate in the context of users, healthcare providers, government agencies, and third-party vendors.

<a href="figures/figure1.png" title="Figure 1 - Operational Concept of the Healthcare.gov"><img src="figures/figure1.png" width="100%" title="Figure 1 - Operational Concept of the Healthcare.gov" alt="Figure 1 - Operational Concept of the Healthcare.gov"></a>

The healthcare marketplace is hosted by an authorized cloud service provider who complies with the FedRamp requirements. By leveraging the FedRamp cloud service provider, the government’s certification and accreditation requirements will be met.  In addition, this will reduce capital cost for hardware and software acquisition, reduce any delays as a result of the procurement process, and maximize the return on investment.

General users will have the ability to browse, apply and purchase health plans using a web-browser.  The healthcare marketplace is accessible from any geographic location using a broadband network connection.  Users who do not have access to the Internet or those who need additional assistance use their local call center. The call center will browse, apply, and purchase on the users behalf. Lastly, the system administrator will have the ability to create, reset, or update the user’s login account.

Healthcare Insurance Providers will send BCP monthly insurance plans. The plans will be updated into the healthcare marketplace system and made available within the acceptable timeframe defined in the Service Level Agreement.

The healthcare marketplace will leverage third-party partners who will provide e-commerce payment services, employment and income verification, and address verification capabilities. The address verification is used to ensure that the user’s address is most current, accurate, and within the United States and its territories. The employment and income verification is to mitigate fraudulent activities for the purposes of calculating subsidies and employer reporting. The e-commerce payment service is used to process the health plan payment.  

### OV-2: Operational Resource Flow Description

The purpose of the operational resource flow as depicted in figure 2 is to illustrate how resources flow within the healthcare marketplace system.  General user enters their personal, health, and employment information as part of the application process.  This information is used to determine if the user qualifies for subsidies.  Similarly, the Call Center user can perform the same operation on behalf of the user.  In the event that the user is unable to login or create an account, the System Administrator can create, update, or reset the user’s account including their password.

During the application process, the healthcare.gov system will invoke the address verification web service. The healthcare.gov will send the user’s residential address and expects a result code to be returned. Similarly, the healthcare.gov will send the user’s employer and income information to the Employment & Income verification service. This is to ensure that the user is employed at the company and at the income stated. Lastly, the healthcare.gov will verify that the user’s social security is valid by querying the database that houses the latest social security numbers. The database contains the SSN and active status that the Social Security Administration provides BPC on a monthly basis. After the user selects the healthcare plan for purchase, the credit card or bank information is sent to the e-Commerce payment provider to perform the actual transaction. If successful, the payment is debited from the user’s account and paid to the healthcare provider.  

<a href="figures/figure2.png" title="Figure 2 - Operational Resource Flow of the Healthcare.gov"><img src="figures/figure2.png" width="100%" title="Figure 2 - Operational Resource Flow of the Healthcare.gov" alt="Figure 2 - Operational Resource Flow of the Healthcare.gov"></a>


### OV-5b: Operational Activity Model

The Operational Activity Model in figure 3 and 4 describes operational activities and tasks of the healthcare marketplace system. The figures are grouped into four categories: Users, the healthcare.gov system, the Cloud Service Providers, and the Data Providers. The intent is to delineate the roles and responsibility for each activity.

<a href="figures/figure3.png" title="Figure 3 - Operational Activity Model for the Healthcare.gov"><img src="figures/figure3.png" width="100%" title="Figure 3 - Operational Activity Model for the Healthcare.gov" alt="Figure 3 - Operational Activity Model for the Healthcare.gov"></a>

The User category encompasses both General Users and Call Center Users. Call Center Users will operate the system on behalf of the user in the call centers. The diagram depicts the high-level activities of users including account creation, application login, browse and compare healthcare plans, apply for and review the status of the application results, and purchase and update the healthcare plan.

When the user wants to browse and compare healthcare plans, the request is sent to the healthcare.gov system. The healthcare.gov evaluates the browse criteria, retrieve the plans from the service providers based on the criteria, identify the plans, and format the results and display to the user. The cloud service provider returns the result from a data repository that has been pre-processed containing the healthcare plans and its offerings.

The application request and update invoked by the user is sent to the healthcare.gov system.  The healthcare.gov system perform a series of real-time verification as depicted in the figure 3 including verify the social security number to ensure that it is valid, verify the residential address for completeness and deliverability, and verify the employment and income level. The SSN verification is performed using the healthcare.gov services, which uses the SSA data that is sent to the healthcare.gov on a monthly basis.  The address and employment/income verification services are performed in real-time using third-party providers including USPS and Experian. If the verification process is successful, the system will determine and calculate any applicable subsidies that the user is entitled. The result is delivered to the user and the application data is stored in the healthcare.gov database.

After the user has selected the healthcare plan for purchase, the request is made by the user and sent to the healthcare.gov system as illustrated in figure 3. The healthcare.gov system processes the request including calculating the final cost, apply subsidies, and invoke a third-party cloud-service payment system to conduct the e-commerce transaction. The confirmation result along is returned to the user.
Users have the ability to create an account on the healthcare.gov website. When the user initiates the request, the healthcare.gov perform a verification process, stores the account information in the data store, emails the user using the cloud service, and returns the result to the user. A similar process occurs when the user logs into the healthcare.gov system. The system authenticates and authorizes the user and logs the user into the system. For a system administrator, the healthcare.gov allows the administrator to update the user’s password and account information as shown in figure 4. The healthcare.gov service emails the updated password to the user while the system stores the information in a data store.

<a href="figures/figure4.png" title="Figure 4 - Operational Activity Model (continued) for the Healthcare.gov"><img src="figures/figure4.png" width="100%" title="Figure 4 - Operational Activity Model (continued) for the Healthcare.gov" alt="Figure 4 - Operational Activity Model (continued) for the Healthcare.gov"></a>

## Systems Viewpoint

### SV-1: Systems Interface Description

The systems design is heavily based on scalable virtual systems. We rely on two types of servers for providing web services. A static web server will be used for serving content that does not require authentication. For example, to access general information about the health care law, the static web server is used.

All images, css files, java script files and other files are stored on a static files server and is distributed with a content delivery system to ensure faster and more reliable content delivery.

All systems that store or serve secure information are located within a firewall and have limited access to outside world.

A web app server provides web services, web interface, mobile web interface and security services. A load balancer launches new instances of the web app if the traffic increases and terminates unnecessary instances.

Automated services are managed by web worker which is scalable similar to the web app server. The capacity will automatically scale if the volume of tasks increases.

A queuing service communicate messages between the web app and the web worker. For example, when the user completes an application, a message is added to the queue or processing the application. The worker will read the application processing message from the queue and run it in the background.

A Redis server is used for caching and performance improvement. Frequently used queries and data are stored with keys and values on the redis server.

A database cluster with multiple master and slave databases is used to store the data. The master/slave setup allow us to scale the database cluster serving capacity based on the volume of traffics.

Each component of this setup use TCP network transport protocol to communicate data packets. The ports used for the communication is shown on the diagram.

<a href="figures/figure5.jpg" title="Figure 5"><img src="figures/figure5.jpg" width="100%" title="Figure 5" alt="Figure 5"></a>

### SV-2: Systems Resources Flow Description

The diagram below shows how the information flows across system resources. The diagram shows how authenticated and unauthenticated requests are directed to different web servers.

For authenticated server, a complex chain of flow is started based on the type of request.

The diagram also shows which system is responsible for accessing third party services such as Address Verification Service, etc.

<a href="figures/figure6.jpg" title="Figure 6"><img src="figures/figure6.jpg" width="100%" title="Figure 6" alt="Figure 6"></a>

### SV-3: Systems Functionality  Description

This diagram shows which functions are available in each system. For example, the web app includes user registration, login, profile editing and making payments.

The diagram also shows how each function interact with other functions. For example, the MMQ system is used for queuing messages and web worker uses the queued messages to run scheduled and automated tasks.

<a href="figures/figure7.jpg" title="Figure 7"><img src="figures/figure7.jpg" width="100%" title="Figure 7" alt="Figure 7"></a>

## Services Viewpoint

In previous section, we have defined the Operational resources in OV-2. Those resources need to be supported by one or more services. In this section, we continue to architect NationalHealthCare.gov network-centric software system from the services viewpoints.

With the service viewpoint models, we could identify and associate the service resources to the operational and capability requirements.

### SvcV-1: Service Context Description

#### Service Concepts and Service Options

The requirement is to design a network-centric software system. For this section, by using Service Oriented Architecture (SOA) design pattern, we could show how the components provide services to other components via communications protocols, the Internet network in this case.

First of all, by going over the conceptual layer of the service architecture, we could identify and to define the major service components.

The NationalHealthCare.gov network-centric software system includes:

- **Physical nodes & Transportation:** The network of server and client computers that are connected over the Internet. As mentioned in Operational Viewpoint, the authorized and qualified cloud service providers will provide the based infrastructure for this system. In our design pattern, we will mention but do not focus on the physical infrastructure services.

- **Protocols:** In our design, this software system will use the common protocols for network and web services.

	- Transmission Control Protocol / Internet Protocol (TCP/IP)
	- IPv6 Internet Protocol Version 6 (IPv6)
	-Simple Network Management Protocol (SNMP)

- **Web Core Services:** Those could be considered as the software infrastructure services. The cloud service provider will provide the core services that supports for the main web application services. The web core services are defined depending on the technologies that will be used in the application. Some highlighted services are:

	- Hypertext Markup Language (HTML) is the standard markup language used to create web pages.
	- Hypertext Transfer Protocol (HTTP) is an application-level protocol for distributed, collaborative, hypermedia information systems. HTTP is the foundation of data communication for the World Wide Web (WWW).
	- HTTP over Transport Layer Security (TLS), prefer as HTTPS, is the communication protocol for secure communication over a computer network.
	- Simple Object Access Protocol (SOAP) is an XML-based messaging protocol used to encode the information in web service request and response messages before sending them over a network.
	- Web Services Description Language (WSDL) is an XML-formatted language used to describe a Web service's capabilities.
	- Extensible Markup Language (XML) is a standard that used to describe the data. It is very common used in web application.

- **Enterprise Service Bus (ESB):** The system services that control the internal system activities.

	- Universal Description, Discovery and Integration (UDDI) is a web-based distributed directory that enables listing of web services and discovering each other.
	- Routing (Service Virtualization)
	- Transformation

-	**Orchestration (Automation):** The services that are automated and provide supports for other services of the system.

- **Services Presentation and Management:** The security layer to manage the accessibility to the web application services.

Figure 8 shows the layered architecture of NationalHealthCare.gov

<a href="figures/figure8.png" title="Figure 8"><img src="figures/figure8.png" width="100%" title="Figure 8" alt="Figure 8"></a>

#### Service Integration Planning and Management

Expanding from the conceptual layers viewpoint, the system is made up from multiple service components. There are basic groups of services and the flow of interaction between those groups of services. The services flows are not limited to internal system and application services. The service groups also include the services related to the human interactions and managements.

Below, figure 9, is the SOA overview of the NationalHealthCare.gov. This diagram shows the basic integration of the service components in the system.

The network-centric software system consists of the basic service components as seen above in the conceptual layers. ESB is the central component, which controls and interacts with the system services: Database Services, Security Services, Automation Services, UDDI Registry, Web Core Services, and Web Service Interfaces. Over common protocols, the backend web application and the third-party services (external services from the providers) could access and use the central system resource. Similarly, over the same protocols, the administrator could access and use the web system administration services. The front-end users include the assistant/management users and the generic users. Those users could access the web interface using different devices and over the same protocols. The assistant users also manage the assistant services to assist the generic users.

<a href="figures/figure9.png" title="Figure 9"><img src="figures/figure9.png" width="100%" title="Figure 9" alt="Figure 9"></a>

#### Services Context Description

In addition to the basic layers and the integration of basic service components, the detail service context plays an important role in SOA design pattern. It describes the services layout that required for the operations of the system.

According to the requirement specifications and the Operational View, we have the following services and service components (Figure 10).

<a href="figures/figure10.png" title="Figure 10"><img src="figures/figure10.png" width="100%" title="Figure 10" alt="Figure 10"></a>

### SvcV-2: Service Resource Flow Description

By expanding the Service Context Description, we have the services and service flows that described in Figure 11.

The ESB services provide the core services to coordinate everything happen in the backend of the system. It would process the service request and service reply for accessing or updating the data services and the web core services.

The Interface services contain the interface of the major component of this system such as: Dashboard, Login, User Profile, Application, and Healthcare Plan. Each interface service would interact with multiple functional components. The Interface services could be considered as the action controller of the system: all the functional services are being called from the uses of interface services. During processing the service request, the interface services could send and receive the service requests for accessing or updating the data services and the web core services.

There are the service components to support the interface services and the service components to support the system.

The User Account services would be used to support the User Profile Interface service and some other related services. The User Account services receive the requests related to user managements and send the approximate reply.

The Security services keep a major role in the system. The Security services could interact directly with the Login service. And the Security services could interact indirectly with every other services of the system.

The Application services are being used for handling the application process and interact directly with the Application Interface service.

The Verification services support for the Application services. The Verification services receive the service requests from the Application services, process the request, and reply to the requests.

The Healthcare Plan services work for the Healthcare Plan Interface service. Once receiving the requests for plan purchase, the Healthcare Plan services process and reply with the results.

The Notification services are being used to support for the whole web application and send the approximate notifications per request.

There is also the External Support services, which are the services provided by external service providers.

While accessing the system, each type of user would have different type of service requests.
The Web Access Center would coordinate the service request from the users and send the request to the interface components. The interface components would process and decide the service to handle the request from the Web Access Center. After processing, the interface components would send the replies to the Web Access Center; the Web Access Center would process and send the replies to the user’s requests.

The more detail flows and descriptions could be seen in Figure 11 below:

<a href="figures/figure11.png" title="Figure 11"><img src="figures/figure11.png" width="100%" title="Figure 11" alt="Figure 11"></a>

### SvcV-4: Service Functionality Description

Service Functionality Description describes the functions performed by services and the service data flows among service functions.

This section identifies and describes the allocation of service functions to resources and the flow of resources between service functions.

The overview and the integrations of service functionalities is described in Figure 12 and the detail functionality description is described in Figure 13.

In general, the system consists of Web-based Application service, web core services, ESB services, External Support services, Infrastructure services, and the External Consumer services (Human Interaction services).

As mentioned previously, ESB and Web Core Services provide the core software base for the system.

The Web-based Application services have the following basic functionalities: Operations, Account Management, Application, and Plan Purchase.

The External Support services are the group of system services that linked to the service providers. These services provide the support functionalities to the core web application.

The Infrastructure services, which are provided by cloud service provider and are not in the scope of the current design architecture, provide the base for the whole system.

The External Consumers services maintain the functionality to support and to work with each type of users.

<a href="figures/figure12.png" title="Figure 12"><img src="figures/figure12.png" width="100%" title="Figure 12" alt="Figure 12"></a>

In detail, the NationalHealthCare.gov network-centric web-based system contains of the following core sets of service functionality:

- Front-end Web Services.
- Web-based Core Services.
- Web-based Application Services.
	- Core function Services
		- User Management Services
		- Application Services
		- System Support Services
			- Data Processes & Functions Services
	- Interface Services
		- User Management Interface Services
		- User Dashboard Services
		- Application Interface Services
		- Healthcare Plan Interface Services
	- Information Services
		- Security Services
		- Notification Services
	- External Support Services.
- Infrastructure Services.
	- Data Center Services
	- Networking Services
		- Communication Connectivity Services

<a href="figures/figure13.png" title="Figure 13"><img src="figures/figure13.png" width="100%" title="Figure 13" alt="Figure 13"></a>


## Concluding Remarks

This ASD describes the operational, system, and service viewpoints of the network-centric software system called NationalHealthCare.gov. The DoDAF models have been used to describe and present the architecture viewpoints of NationalHealthCare.gov system.

From the different viewpoints, the architecture of the NationalHealthCare.gov system is complex. It is necessary to review the system from those viewpoints in order to prepare for the steps of software engineering.
The architecture specifications in this document provide the information to continue with the design specifications.


## References

<a name="ref1">[1]</a> “Obamacare Bill: Full PPACA & Related Laws." Obamacare Facts. N.p., n.d. Web. 03 March 2015

<a name="ref2">[2]</a> Pickert,Kate.  “Report: Cost of Healthcare.gov Approaching $1 Billion.” Time.  Time n.d. Web. 30 Jul. 2014
