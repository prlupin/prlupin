
<img src="figures/logo.png" style="float: right;" width="200px" alt="logo" title="logo">

## A New Design of Healthcare.gov
**Architecture Specification Document**

**CS5704 | Project 2 | Group 7:**

Alireza Jazayeri - Danh Huynh - Dat Hoang

April 07, 2015

### Executive Summary

This Architecture Specification Document (ASD) describes the architecture of the federal healthcare exchange marketplace, the HealthCare.gov, which allows Americans the ability to purchase health insurance online.

The HealthCare.gov provides American individual and families another way to purchase healthcare insurance online through state or federal healthcare marketplace.  Low and middle class Americans will have the option to purchase federally regulated and subsidized insurance through the online marketplace.  For individuals who fall below the Federal Poverty Level, the marketplace will help them determine the amount of subsidies or Premium Tax Credit.  

Per the basic requirements, the HealthCare.gov is a network-centric software system. Its system architecture is complex and could not be described from a single viewpoint. The Department of Defense Architecture Framework (DoDAF) models are used to create the multiple viewpoints architecture for this system. By using DoDAF models, the system architecture could be represented by multiple viewpoints. In this ASD, the architecture of the HealthCare.gov is described using following viewpoints:

|  Operational Viewpoint (OV)
	- OV-1: High-Level Operational Concept Graphic
	- OV-2: Operational Resource Flow Description
	- OV-5b: Operational Activity
|  System Viewpoint (SV)
	- SV-1: Systems Interface Description
	- SV-2: Systems Resource Flow Description
	- SV-4: Systems Functionality Description
|  Service Viewpoint (SvcV)
	- SvcV-1: Services Context Description
	- SvcV-2: Services Resource Flow Description
	- SvcV-4: Services Functionality Description


### Table of Contents

| # | Title
| ------- | -----
| 1. | [Introduction](introduction)
| 2. | [Architecture Specification](architecture)
| 2.1	| [OV-1: High-Level Operational Concept Graphic](architecture/#21-ov-1-high-level-operational-concept-graphic)
| 2.2	| [OV-2: Operational Resource Flow Description](architecture/#22-ov-2-operational-resource-flow-description)
| 2.3	| [OV-5b: Operational Activity Model](architecture/#23-ov-5b-operational-activity-model)
| 2.4	| [SV-1: Systems Interface Description](architecture/#24-sv-1-systems-interface-description)
| 2.5	| [SV-2: Systems Resource Flow Description](architecture/#25-sv-2-systems-resources-flow-description)
| 2.6	| [SV-4: Systems Functionality Description](architecture/#26-sv-3-systems-functionality-description)
| 2.7	| [SvcV-1: Services Context Description](architecture/#27-svcv-1-service-context-description)
| 2.7.1	| [Services Concepts and Services Options](architecture/#271-service-concepts-and-service-options)
| 2.7.2	| [Services Integration Planning and Management](architecture/#272-service-integration-planning-and-management)
| 2.7.3	| [Services Context Description](architecture/#273-services-context-description)
| 2.8	| [SvcV-2: Services Resource Flow Description](architecture/#28-svcv-2-service-resource-flow-description)
| 2.9	| [SvcV-4: Services Functionality Description](architecture/#29-svcv-4-service-functionality-description)
| 3. | [Concluding Remarks](conclusion/#3-concluding-remarks)
| | [References](conclusion/#references)


### List of Figures

| # | Title
| ------- | -----
| Figure 1 | [High-Level Operational Concept of the HealthCare.gov](architecture/#figure1)
| Figure 2 | [Operational Resource Flow of the HealthCare.gov](architecture/#figure2)
| Figure 3 | [Operational Activity Model for the HealthCare.gov](architecture/#figure3)
| Figure 4 | [Operational Activity Model (continued) for the HealthCare.gov](architecture/#figure4)
| Figure 5 | [Systems Interface Description of the HealthCare.gov](architecture/#figure5)
| Figure 6 | [Systems Resource Flow Description of the HealthCare.gov](architecture/#figure6)
| Figure 7 | [System Functionality Description of the HealthCare.gov](architecture/#figure7)
| Figure 8 | [Conceptual Layered Architecture of the HealthCare.gov](architecture/#figure8)
| Figure 9 | [SOA Overview of the HealthCare.gov](architecture/#figure9)
| Figure 10 | [Services Context Description of the HealthCare.gov](architecture/#figure10)
| Figure 11 | [Services Resource Flow Description of the HealthCare.gov](architecture/#figure11)
| Figure 12 | [Services Functionality Overview of the Healthcare.gov](architecture/#figure12)
| Figure 13 | [Services Functionality Description of the HealthCare.gov](architecture/#figure13)


### List of Abbreviations and Terms

| Abbreviation | Meaning
| ---- | ----
| ACA | Affordable Care Act
| ASD | Architecture Specification Document
| BPC | Blue Point Consulting
| CMS | Centers for Medicare and Medicaid Services
| CSS | Cascading Style Sheets
| DoDAF | Department of Defense Architecture Framework
| ESB | Enterprise Service Bus
| GSA | General Administration Services
| HHS | Health and Human Services
| HTML | Hypertext Markup Language
| HTTP | Hypertext Transfer Protocol
| HTTPS | HTTP over Transport Layer Security
| IPv6 | Internet Protocol Version 6
| OV | Operational Viewpoint
| SBIR | Small Business Innovation Research
| SNMP | Simple Network Management Protocol
| SOA | Services Oriented Architecture
| SOAP | Simple Object Access Protocol
| SV | Service Viewpoint
| SvcV | Services Viewpoint
| TCP/IP | Transmission Control Protocol / Internet Protocol
| TLS | Transport Layer Security
| UDDI | Universal Description, Discovery and Integration
| WSDL | Web Services Description Language
| WWW | World Wide Web
| XML | Extensible Markup Language

### Download PDF

[Download PDF](Group7.pdf) version of this report
