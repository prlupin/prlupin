

## Executive Summary

NationalHealthCare.gov is a network-centric web-based system.  Its system architecture is complex and could not be described from a single viewpoint. The Department of Defense Architecture Framework (DoDAF) models are used to create the multiple viewpoints architecture for this system. By using DoDAF models, the system architecture is represented by:

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

On March 23, 2010, President Obama signed into law The Patient Protection and Affordable Care Act (ACA), which require every American to obtain health insurance or pay a penalty [[1]](#ref1).  The purpose of the ACA is to make insurance more affordable by reducing insurance premiums and out-of-pocket cost for Americans who previously could not afford insurance[[1]](#ref1).  Furthermore, the law prevents insurance companies from denying Americans health insurance based on pre-existing conditions.  Additional benefits of the ACA includes but not limited to no-cost preventative care, coverage for young adults under the age of 26, and no cancellation or lifetime limits on care. 

The purpose of this Architecture Specification Document (ASD) is to describe the operational, system, and service views of the healthcare marketplace.  The healthcare marketplace in tended to provide American individuals and families another way to purchase healthcare insurance online through state or federal healthcare marketplace.  Low and middle class Americans will have the option to purchase federally regulated and subsidized insurance through the online marketplace.  For individuals who fall below the Federal Poverty Level, the marketplace will help them determine the amount of subsidies or Premium Tax Credit.  

The healthcare marketplace (referred to as the healthcare.gov) shall provide Americans with online capabilities to compare health plans, enroll in a chosen health plan, and calculate any subsidies or credits.  The marketplace shall display available plans to User based on the types of plans including Bronze, Silver, Gold and Platinum.  The marketplace shall provide an intuitive user interface that allows User to compare the different types of plans based on their medical needs.  In addition, the marketplace shall provide User the option to enroll in the chosen health plan.  The marketplace shall validate User’s eligibility including but not limited to the validity of the SSN, legal resident, employment status, income, and citizenship.  Furthermore, the marketplace shall calculate any subsidies and/or credits that the User qualifies based on employment and income levels.

Currently, there are no web-based healthcare marketplaces that are available for the general public to purchase healthcare plan to meet the ACA requirements.  Hence, the government is seeking a contractor to build a cloud-based healthcare marketplace that allows users to browse, apply, and purchase healthcare plans.  Specifically, the healthcare marketplace needs to address the following challenges:

1.	Provide users with a user-friendly web application interface to browse, compare, apply, and purchase healthcare plans online using the Internet
2.	Establish call centers including faith based organizations, government affiliates, etc. to help users requiring assistance or those who do not have sufficient Internet connection/bandwidth access to the healthcare marketplace
3.	Collect and update healthcare plans from healthcare providers and make the plans available on the healthcare marketplace
4.	Create login accounts for users to manage their healthcare plans and user profile
5.	Ability for the user to apply for the ACA
6.	Calculate healthcare subsidies in real-time as defined by the ACA requirements
7.	Leverage third-party services and products to streamline the application and plan purchase process including verification and online payment services
8.	Report individuals and their employers to the Internal Revenue Service

Moreover, healthcare providers will offer users’ healthcare plans through the marketplace.  These plans will be received and updated by the healthcare.gov system.  BPC intends to leverage commercial-off-the-shelf provides and services to expedite the development effort and minimize capital cost.  These third-party services include employment and income verification, address verification, and e-commerce payment.     

The development of this healthcare marketplace will be funded through the Department of Health and Human Services (HHS) [[2]](#ref2).  Specifically, the Centers for Medicare and Medicaid Services (CMS) have obligated in excess of $840 million dollars to develop the healthcare marketplace.  It is the intent of the Blue Point Consulting to develop the healthcare marketplace in concert with Accenture; and to maintain the website on an ongoing basis.

Blue Point Consulting (BPC) was founded in 2005 and headquarters in Reston, Virginia as a software development company.  BPC was awarded their first contract through the Small Business Innovation Research (SBIR) program.  BPC received Phase I and Phase II funding by the US Navy to research and develop innovative methods to seamlessly integrate a common operating picture across various government agencies using cloud computing technologies.  Through the initial SBIR program, BPC have grown to a 400 employees with annual revenue exceeding $50 million dollars.  We believe with our software development and cloud computing expertise will help the Accenture team build a user-friendly, robust, and highly available online healthcare marketplace.
In support of this project, BPC has hired 35 new information technology professionals, in addition to our current team, to design and develop this web-based healthcare marketplace.  The team consist but not limited to a program manager, project manager, requirements analysts, system architecture, software developers, network engineers, quality assurance and control specialist, release and deployment engineers.  The team will support all phases of the software development life-cycle until the initial baseline release.  After the initial production release, BCP will reduce the team size to address bug fixes and future enhancements and commensurate with the price schedule.

BPC intends to maintain and enhance the healthcare marketing place after the initial development effort.  This effort is part of the three base year contract.  The maintenance and enhancement of the healthcare marketplace includes new functionality, bug fixes to the website, data updates from third-party providers, generate and deliver reports to the internal revenue service, resolve account management issues, and address payment processing problems.  The intent of these services are: 1) to provide users of the healthcare marketplace with a good buying experience, 2) provider users numerous options to purchase the healthcare plans, 3) provide the latest healthcare plans and cost, 4) provide a highly-available, reliable, and intuitive application, and 5) meet the ACA requirements.

BPC proposed a firm-fixed priced contract to support this project, using the labor categories and software development licenses outlined in the General Administration Services (GSA) pricing.  All travel expenses will be considered out-of-pocket and billed in the government as required.  All hardware and server software licenses will be considered outside the scope of this project. The price proposal is a three year base contract with 5 option years as specified in the cost proposal.  BPC believes that we are offering the government with the best solution and best value to develop a highly robust system within a very aggressive timeframe.  In addition, since BPC is a Virginia based company, this project will help generate revenue for the Commonwealth and for US small businesses.


## Architecture Specification

This section describes the system architecture of the healthcare.gov system including the operational views, system views, and service views.  The purpose of this document, among other factors, are to describe the scope of the architecture, determine the data required to support the system, conduct and analyze the architectural impact of the system, and identify key stakeholders.

## Operational Viewpoint

### OV-1: High-Level Operational Concept Graphic

The high-level operational concept view depicted in figure 1 below shows how the cloud-based healthcare marketplace will operate in the context of users, healthcare providers, government agencies, and third-party vendors.

[Figure 1 - Operational Concept of the Healthcare.gov]

The healthcare marketplace is hosted by an authorized cloud service provider who complies with the FedRamp requirements.  By leveraging the FedRamp cloud service provider, the government’s certification and accreditation requirements will be met.  In addition, this will reduce capital cost for hardware and software acquisition, reduce any delays as a result of the procurement process, and maximize the return on investment.

General users will have the ability to browse, apply and purchase health plans using a web-browser.  The healthcare marketplace is accessible from any geographic location using a broadband network connection.  Users who do not have access to the Internet or those who need additional assistance use their local call center.  The call center will browse, apply, and purchase on the users behalf.  Lastly, the system administrator will have the ability to create, reset, or update the user’s login account.  

Healthcare Insurance Providers will send BCP monthly insurance plans.  The plans will be updated into the healthcare marketplace system and made available within the acceptable timeframe defined in the Service Level Agreement.

The healthcare marketplace will leverage third-party partners who will provide e-commerce payment services, employment and income verification, and address verification capabilities.  The address verification is used to ensure that the user’s address is most current, accurate, and within the United States and its territories.  The employment and income verification is to mitigate fraudulent activities for the purposes of calculating subsidies and employer reporting.  The e-commerce payment service is used to process the health plan payment.  

### OV-2: Operational Resource Flow Description

The purpose of the operational resource flow as depicted in figure 2 is to illustrate how resources flow within the healthcare marketplace system.  General user enters their personal, health, and employment information as part of the application process. This information is used to determine if the user qualifies for subsidies.  Similarly, the Call Center user can perform the same operation on behalf of the user.  In the event that the user is unable to login or create an account, the System Administrator can create, update, or reset the user’s account including their password.  

During the application process, the healthcare.gov system will invoke the address verification web service.  The healthcare.gov will send the user’s residential address and expects a result code to be returned.  Similarly, the healthcare.gov will send the user’s employer and income information to the Employment & Income verification service.  This is to ensure that the user is employed at the company and at the income stated.  Lastly, the healthcare.gov will verify that the user’s social security is valid by querying the database that houses the latest social security numbers.  The database contains the SSN and active status that the Social Security Administration provides BPC on a monthly basis.  After the user selects the healthcare plan for purchase, the credit card or bank information is sent to the e-Commerce payment provider to perform the actual transaction.  If successful, the payment is debited from the user’s account and paid to the healthcare provider.  

[Figure 2 - Operational Resource Flow of the Healthcare.gov]

### OV-5b: Operational Activity Model

The Operational Activity Model in figure 3 and 4 describes operational activities and tasks of the healthcare marketplace system. The figures are grouped into four categories: Users, the healthcare.gov system, the Cloud Service Providers, and the Data Providers.  The intent is to delineate the roles and responsibility for each activity.

[Figure 3 - Operational Activity Model for the Healthcare.gov]

The User category encompasses both General Users and Call Center Users.  Call Center Users will operate the system on behalf of the user in the call centers.  The diagram depicts the high-level activities of users including account creation, application login, browse and compare healthcare plans, apply for and review the status of the application results, and purchase and update the healthcare plan.

When the user wants to browse and compare healthcare plans, the request is sent to the healthcare.gov system.  The healthcare.gov evaluates the browse criteria, retrieve the plans from the service providers based on the criteria, identify the plans, and format the results and display to the user.  The cloud service provider returns the result from a data repository that has been pre-processed containing the healthcare plans and its offerings.

The application request and update invoked by the user is sent to the healthcare.gov system.  The healthcare.gov system perform a series of real-time verification as depicted in the figure 3 including verify the social security number to ensure that it is valid, verify the residential address for completeness and deliverability, and verify the employment and income level.  The SSN verification is performed using the healthcare.gov services, which uses the SSA data that is sent to the healthcare.gov on a monthly basis.  The address and employment/income verification services are performed in real-time using third-party providers including USPS and Experian.  If the verification process is successful, the system will determine and calculate any applicable subsidies that the user is entitled.  The result is delivered to the user and the application data is stored in the healthcare.gov database.

After the user has selected the healthcare plan for purchase, the request is made by the user and sent to the healthcare.gov system as illustrated in figure 3.  The healthcare.gov system processes the request including calculating the final cost, apply subsidies, and invoke a third-party cloud-service payment system to conduct the e-commerce transaction.  The confirmation result along is returned to the user.

Users have the ability to create an account on the healthcare.gov website.  When the user initiates the request, the healthcare.gov perform a verification process, stores the account information in the data store, emails the user using the cloud service, and returns the result to the user.  A similar process occurs when the user logs into the healthcare.gov system.  The system authenticates and authorizes the user and logs the user into the system.  For a system administrator, the healthcare.gov allows the administrator to update the user’s password and account information as shown in figure 4. The healthcare.gov service emails the updated password to the user while the system stores the information in a data store.

[Figure 4 - Operational Activity Model (continued) for the Healthcare.gov]

## Systems Viewpoint

### SV-1: Systems Interface Description

### SV-2: Systems Resources  Flow Description

### SV-3: Systems Functionality  Description

## Services Viewpoint

We have defined the Operational resources in OV-2. Those resources need to be supported by one or more services. In this section, we continue to architect NationalHealthCare.gov network-centric web-based system from the services viewpoints. 

With the service viewpoint models, we could identify and associate the service resources to the operational and capability requirements.

### SvcV-1: Service Context Description

#### Service Concepts

The requirement is to design a network-centric web-based system. Therefore, we will go from the conceptual layer of the service architecture in order to identify and to define the major service components.
NationalHealthCare.gov network-centric web-based system includes:
- Physical nodes & Transportation: The network of server and client computers that are connected over the Internet.
- Protocols: Common protocols for network and web services.
- Web Core Services: The core services that provide supports for the main web application services.
- Enterprise Service Bus (ESB): The system services that control the internal system activities.
- Automation: The services that are automated and provide supports for other services of the system.
- Service Management: The security layer to manage the accessibility to the services.

#### Service Options

By using Service Oriented Architecture (SOA) design pattern, we could show how the components provide services to other components via communications protocols, the Internet network in this case.

Below is the SOA-based architecture of NationalHealthCare.gov:


#### Service Resource Flow Requirements

Services are not limited to internal system functions and can include Human Computer Interface (HCI) and Graphical User Interface (GUI) functions or functions that consume or produce service data to or from service functions. The external service data providers and consumers can be used to represent the human that interacts with the service.

#### Capability integration Planning


#### Service integration Management

#### Service Operational Planning

### SvcV-2: Service Resource Flow Description

According to the Requirements and the Service Context Description,

### SvcV-4: Service Functionality Description

Service Functionality Description describes the functions performed by services and the service data flows among service functions.
In this section, we identify and describe the allocation of service functions to resources and the flow of resources between service functions.
NationalHealthCare.gov network-centric web-based system contains of the following core sets of service functionality:
- Frontend Web Services
- Web-based Core Services.
- Web-based Application Services.
	- Core function Services
		- User Management Services
		- Application Services
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

## Concluding Remarks

## Referernces

<a name="ref1">[1]</a> “Obamacare Bill: Full PPACA & Related Laws." Obamacare Facts. N.p., n.d. Web. 03 March 2015

<a name="ref2">[2]</a> Pickert,Kate.  “Report: Cost of Healthcare.gov Approaching $1 Billion.” Time.  Time n.d. Web. 30 Jul. 2014
