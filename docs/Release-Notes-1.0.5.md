## Table Of Contents

- [Scope](#scope-)
- [Documentation](#documentation-)
- [Key Points](#key-points-)
- [Code](#code-)
- [Test Reports](#test-reports-)
  * [1. In scope](#1-in-scope-)
  * [2. Not in scope](#2-Not-in-scope-)
  * [3. Executive Summary – Consolidated Quality Status](#3-executive-summary--consolidated-quality-status-)
  * [4. Types of Testing](#4-types-of-testing-)
  * [5. Test Execution Summary](#5-test-execution-summary-)
- [Known Issues](#known-issues-)
- [List Of Acronyms](#list-of-acronyms-)

## Scope [**[↑]**](#table-of-contents)
This release is with **real biometrics**. This means that MOSIP Platform is now integrated with SDK, MDS (MOSIP  Device Service), ABIS (Automated Biometrics Identification System) and Biometric devices. Also, this version is tested for Biometric functionalities. Non-functional requirements (Performance, Scale and Security) will be taken up in subsequent releases.

* Modules included – Pre-Registration, Registration Client, Registration Processor, ID Authentication, Administration, Reference GUI implementation of Pre-Registration, Registration Client and Administration. 
* Modules not included – Partner Management and Resident Services
* IAM - The Identity and Access Management(IAM) had been changed from custom implementation to Keycloak. 

Module-wise features released as part of this release can be found [here](_files/release/1.0.5/MOSIP_Feature_Release_v1.0.5.xlsx)

## Documentation [**[↑]**](#table-of-contents)

### 1. Platform Documentation 
Includes Functional requirements, Process flows, Architecture and High level design, Getting started and Deployment guide, Developer documentation etc.  

### 2. Detailed Documentation
Low Level design is available in respective repository and [**Test cases**](https://github.com/mosip/mosip-functional-tests/tree/1.0.5)

### 3. Platform Configurability for RBR    
MOSIP Platform can be configured to be used for Real Biometrics.  [Guide to configure MOSIP for Real Biometrics](Guide-to-configure-MOSIP-for-Real-Biometrics.md)

## Key Points [**[↑]**](#table-of-contents)

|Key Points|	Details|
|----|----|
|Pre Registration - Browser support |	Chrome 74.0.3729|
|Deployment Script Environment|	Microsoft Azure|
|Registration Client – OS version|	Windows 10 (English version)  with TPM 2.0|
|Camera|	Logitech / Default windows camera|
|Scanner|	Canon lide 120|
|GPS|	GlobalSat BU-353-S4|
|Biometrics standard|	CBEFF format (Version - 0.9.0)|
|MOSIP Device Service (MDS)|	Version - 0.9.1|
|SMS gateway|	MSG91, Infobip|
|Registration Client – face capture |	OpenImaj - This is licensed for demo purpose only|
|Keystore|	SoftHSM|
|Antivirus|	ClamAV|
|Maps	|OpenstreetMap|
|Supporting key based digital signatures, not using digital certificates||	
|Transliteration|	ICU4J (Library with French, Arabic languages)|

## Code [**[↑]**](#table-of-contents)
The [code](https://github.com/mosip/mosip-platform/releases/tag/1.0.0) and [automation tests](https://github.com/mosip/mosip-functional-tests/tree/1.0.5) are available on GitHub. The code needs to be built and deployed as per the procedure documented in [**Building And Deploying MOSIP**](Platform-Documentation#9-building-and-deploying-mosip). We will actively support System Integrators during their first deployment.

## Test Reports [**[↑]**](#table-of-contents)
**Testing Scope**
#### 1. In scope [**[↑]**](#table-of-contents)

|Title	|Description|
|------|------|
|Modules Tested|<ul><li>Pre-registration (UI & Server)</li><li>Registration Client (UI & APIs)</li><li>Kernel (APIs)</li><li>Registration Processor (Server)</li><li>ID Authentication (APIs)</li><li>ID Repo (APIs)</li><li>Administration (UI & APIs)</li></ul>|
| Version Tag Tested|	1.0.5|
|Test Methodology|<ul><li>Manual</li><li>Test Automation</li></ul>|
|Types of testing|<ul><li>Smoke</li><li>Functional</li><li>Integration</li><li>Regression</li></ul>|
|Testing Levels|![Image](_images/test_rig_automation/image1.jpg) |
|Configuration Parameters tested for| Refer to properties file at [**Link**](https://github.com/mosip/mosip-config/tree/master/config-templates)|
|Browser Support|**Pre-Registration** <ul><li>Chrome – 78.0.3904.108</li></ul>|
|OS Support|**Registration Client** <ul><li>Windows 10</li></ul>|
|Language Support|French, Arabic, English|

#### 2. Not in scope [**[↑]**](#table-of-contents)

|Title|	Description|
|------|------|
|NFR Testing| <ul><li>Scalability Testing</li><li>Performance Testing</li><li>Security Testing</li></ul>|
|Configuration Testing| <ul><li>Testing is done for one set of approved production configuration<ul><li>Changing the configuration parameters for various values (boundary values) and testing the impact of each such value on the platform code will be taken up in subsequent releases.</li></ul>|

#### 3. Executive Summary – Consolidated Quality Status [**[↑]**](#table-of-contents)

|Sl. No.|	Module / Activity|Test Methodology|	Test Status|
|------|------|------|------|
|1|	Kernel	|<li> Test Automation	|PASS|	
|2|	Pre-Registration|<li> Test Automation|PASS |
|3|	Registration Client|* Tested Manually	* Test Automation|PASS|
|4|Registration Processor|<li> Tested Manually <li> Test Automation	|PASS |
|5|	ID Authentication	|	<li>  Test Automation	|PASS|
|6|	ID Repo	|	<li> Test Automation	|PASS|	
|7|Pre-Registration to Registration Client integration testing|	<li> Tested Manually|PASS	|	
|8|	Registration Client to Registration Processor integration testing|	<li> Tested Manually|PASS|	
|9|	Registration Processor to IDA integration testing|<li> 	Tested Manually|PASS|
|10|	IDA to ID Repo|<li> 	Tested Manually|PASS	|

#### 4. Types of Testing [**[↑]**](#table-of-contents)

|Testing Type| Description|
|------|------|
|Smoke Testing|Tests to ensure basic work flows work fine|
|Functional Testing|Tests to ensure functionality of each module and overall system work fine in accordance with the given requirements|
|Integration Testing|Tests to ensure the inter module functionality works fine and in accordance with the integration requirements|
|Regression Testing|Tests to ensure that any change doesn't break existing functionality|
	
#### 5. Test Execution Summary [**[↑]**](#table-of-contents)
![Image](_images/test_rig_automation/ExecutionSummary_1.0.5.jpg)  

## Known Issues [**[↑]**](#table-of-contents)
![Image](_images/test_rig_automation/KnownIssues_1.0.5.jpg) 

## List Of Acronyms [**[↑]**](#table-of-contents)
Acronym | Expanded Form
-----|-----------------
ABIS | Automated Biometric Identification System
API | Application Programming Interface
ID | Identity
IDA | Identity Authentication
MOSIP | Modular Open Source Identity Platform
NFR | Non-Functional Requirements
OTP | One Time Password
SDK | Software Development Kit
TBD | To Be Determined
TOTP| Temporary One Time Password
UIN | Unique Identification Number
WIP | Work In Progress
CBEFF | Common Biometric Exchange Formats Framework
HSM | Hardware Security Module
TPM | Trusted Platform Module




