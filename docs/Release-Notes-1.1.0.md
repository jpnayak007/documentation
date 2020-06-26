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
- [Support Process (To Be Determined)](#support-process-to-be-determined-)
- [List Of Acronyms](#list-of-acronyms-)
- [Highlights](#highlights)
## Scope [**[↑]**](#table-of-contents)

Version **1.1.0** of MOSIP Platform is a feature and stability release.

MOSIP 1.0 was a functional release of mosip with the core modules tested with biometrics. The 1.1 release of mosip builds upon the 1.0 version and adds more features, some new modules, engineering enhancements, performance and security tuning.MOSIP 1.0 was a functional release of mosip with the core modules tested with biometrics. The 1.1 release of mosip builds upon the 1.0 version and adds more features, some new modules, engineering enhancements, performance and security tuning.

Release Date: June 30, 2020

Highlights of the 1.1.0 release include:
* New Module added – Partner Management and Master Data Administration, 
* Features added - New features added to MOSIP platform
* Bug Fixes across all modules
* Engineering Changes
  * Automated deployment scripts for development, testing environments on Kubernetes
  * Open build process using Travis
  * Github actions, git commit id in builds
  * Shift from private repository to public maven and  docker repositories
  * Decoupling version of components from release version
  * Gitbook based documentation
* Technology Changes
  * Keycloak for IAM
  * ApacheDS ldap as user store deprecated
  * Prometheus end points in all spring boot services
  * Network HSM support added

Module-wise features released as part of this release can be found [here](https://github.com/mosip/documents/_files/MOSIP_Feature_Release_v1.1.0.xlsx).

## Documentation [**[↑]**](#table-of-contents)
### 1. Platform Documentation 
Includes Functional requirements, Process flows, Architecture and High level design, Getting started and Deployment guide, Developer documentation etc.  
   [**Link to Platform Documentation**](Platform-Documentation)
### 2. Detailed Documentation
[**Low Level design**](https://github.com/mosip/mosip-platform/tree/master/design)
### 3. Platform Configurability for RBR    
MOSIP Platform can be configured to be used for Real Biometrics.  [Guide to configure MOSIP for Real Biometrics](https://github.com/mosip/mosip-docs/wiki/Guide-to-configure-MOSIP-for-Real-Biometrics)

## Key Points [**[↑]**](#table-of-contents)

|Key Points|	Details|
|----|----|
|Pre Registration - Browser support |	Chrome 74.0.3729|
|Deployment Script Environment|	Microsoft Azure|
|Registration Client – OS version|	Windows 10 (English version)  with TPM 2.0|
|Camera|	Logitech / Default windows camera|
|Scanner|	Canon lide 120|
|GPS|	GlobalSat BU-353-S4|
|Biometrics standard|	CBEFF format (Version - 2.0)|
|MOSIP Device Service (MDS)|	Version - 0.9.5|
|SMS gateway|	MSG91, Infobip|
|Registration Client – face capture |	OpenImaj - This is licensed for demo purpose only|
|Keystore|	SoftHSM|
|Antivirus|	ClamAV|
|Maps	|OpenstreetMap|
|Supporting key based digital signatures, not using digital certificates||	
|Transliteration|	ICU4J (Library with French, Arabic languages)|
|ABIS |ABIS Spec Version v0.9| 
|SDK |SDK Spec Version v0.9| 


## Code [**[↑]**](#table-of-contents)
The [code](https://github.com/mosip/commons/releases) and [automation tests](https://github.com/mosip/mosip-functional-tests) are available on GitHub. The code needs to be built and deployed as per the procedure documented in [**Building And Deploying MOSIP**](Platform-Documentation#9-building-and-deploying-mosip). We will actively support System Integrators during their first deployment.

## Test Reports [**[↑]**](#table-of-contents)
**Testing Scope**
#### 1. In scope [**[↑]**](#table-of-contents)

|Title	|Description|
|------|------|
|Modules Tested|<li> Pre-registration (UI & Server) <li> Registration Client (UI & APIs) <li> Kernel (APIs) <li> Registration Processor (Server) <li> ID Authentication (APIs) <li> ID Repo (APIs) <li> Administration (UI & APIs) <li> Resident Services (APIs)|
| Version Tag Tested|	1.0.6|
|Test Methodology| <li>  Manual <li>  Test Automation|
|Types of testing|<li>	 Smoke <li> Functional <li>  Integration <li> 	Regression|
|Testing Levels|![Image](_images/test_rig_automation/image1.jpg) |
|Configuration Parameters tested for| Refer to properties file at [**Link**](https://github.com/mosip/mosip-config/tree/master/config-templates)|
|Browser Support|**Pre-Registration**    <li> Chrome – 78.0.3904.108|
|OS Support|**Registration Client**    <li> Windows 10|
|Language Support|French, Arabic, English|

#### 2. Not in scope [**[↑]**](#table-of-contents)

|Title|	Description|
|------|------|
|NFR Testing| <li> Scalability Testing <li> Performance Testing <li> Security Testing|
|Configuration Testing|<li> Testing is done for one set of approved production configuration <li> Changing the configuration parameters for various values (boundary values) and testing the impact of each such value on the platform code will be taken up in subsequent releases.|

#### 3. Executive Summary – Consolidated Quality Status [**[↑]**](#table-of-contents)

|Sl. No.|	Module / Activity|Test Methodology|	Test Status|
|------|------|------|------|
|1|	Kernel	|<li> Test Automation	|PASS|	
|2|	Pre-Registration|<li> Test Automation|PASS |
|3|	Registration Client|<li> Tested Manually <li> Test Automation|PASS|
|4|Registration Processor|<li> Tested Manually <li> Test Automation	|PASS |
|5|	ID Authentication	|	<li>  Test Automation	|PASS|
|6|	ID Repo	|	<li> Test Automation	|PASS|
|7|	Resident Services	|	<li> Test Automation	|PASS|	
|8|Pre-Registration to Registration Client integration testing|	<li> Tested Manually|PASS	|	
|9|	Registration Client to Registration Processor integration testing|	<li> Tested Manually|PASS|	
|10|	Registration Processor to IDA integration testing|<li> 	Tested Manually|PASS|
|11|	IDA to ID Repo|<li> 	Tested Manually|PASS	|

#### 4. Types of Testing [**[↑]**](#table-of-contents)

|Testing Type| Description|
|------|------|
|Smoke Testing|Tests to ensure basic workflows work fine|
|Functional Testing|Tests to ensure functionality of each module and overall system work fine in accordance with the given requirements|
|Integration Testing|Tests to ensure the inter module functionality works fine and in accordance with the integration requirements|
|Regression Testing|Tests to ensure that any change doesn't break existing functionality|
	
#### 5. Test Execution Summary [**[↑]**](#table-of-contents)
![Image](_images/test_rig_automation/ExecutionSummary_1.0.6.jpg)  

## Known Issues [**[↑]**](#table-of-contents)
![Image](_images/test_rig_automation/KnownIssues_1.0.6.jpg) 

## Support Process (To Be Determined) [**[↑]**](#table-of-contents)
Process to be followed for support required, escalation matrix, etc.

## List Of Acronyms [**[↑]**](#table-of-contents)
[**Refer to List Of Acronyms**](Platform-Documentation#12-list-of-acronyms)