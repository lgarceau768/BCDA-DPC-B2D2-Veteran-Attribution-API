# Veteran Attribution API PRD

See [BCDA PHASE II Tech Challenge: B2D2](/sbj3SSUBQcS0MopOHU_mJg) for the main README and links. This document is solely for the Product Requirements as it pertains to the Product Delivery section of the ["Success Criteria"](https://hackmd.io/sbj3SSUBQcS0MopOHU_mJg?both#Success-Criteria) outlined in the tech challenge. 

## About

You are part of a newly onboarded CMS agile team that has been tasked with building an Application Programming Interface (API) that will be used by the VA to submit their patient’s data to CMS using FHIR. This new API has been named the Veteran Attribution API. *CMS envisions a minimum viable product that allows the VA to send Patient and Coverage data to CMS in bulk. The API must also allow CMS users to query the Patient and Coverage data individually.*

### Pain

Summary of the high level pain, followed by the specific pain points below.

data must be in compatible format 
data exists in multiple systems 
patient and coverage data must be validated in VA system and CMS system 
CMS users need to be able to query the patient and coverage data individually. 

### Context

Add in any additional context that might be useful. 

# :crystal_ball: Vision

>CMS envisions a minimum viable product that allows the VA to send Patient and Coverage data to CMS in bulk, and CMS users to query the Patient and Coverage data individually.

This is still TBD, but the essence of what CMS hopes to see is there. 

# 👩‍🎤 Users
User story format: As a `user persona`, I want `goal` so that `some reason`.

- 👩‍"**dual beneficiaries**": *when looking at the population of individuals covered by both Medicare and the VA health benefits programs, each of the agencies possess separate pieces of the data puzzle. Before CMS can send Medicare claims data to the VA, both agencies need to exchange demographic and coverage information of its patients and agree on a method to identify and build*
    - As a dual beneficiary I want information about my coverage to be safely communicated between the VA and Medicare, so that I can get the coverage I need without having my sensitive data leaked to nefarious people. 
- 👩‍**the VA**: The VA Submits their patient data to CMS using FHIR 
    - As the VA I need to exchange demographic and claims information of our patients with CMS so that we can ensure beneficiaries get the coverage they are eligible for and need. 
    - As the VA I need to agree with CMS on a method to identify and build this population on an ongoing basis, to ensure dual-beneficiaries get the coverage they need. 
- 👩‍**CMS**: Receives the data, and query the Patient and Coverage data individually.
    - As CMS I need to query the patient and coverage data individually, so that I may securely confirm eligibility? 
    - As CMS I need to exchange demographic and claims information of our patients with the VA so that we can ensure beneficiaries get the coverage they are eligible for and need. 
    - As CMS I need to agree with the VA on a method to identify and build this population on an ongoing basis, to ensure dual-beneficiaries get the coverage they need. 

# 👩‍💻 Implementation

**The Veteran Attribution API implementation must:**

1. Have an authentication/authorization mechanism.
2. Implement a mechanism to match patients using the CMS and VA data provided and identify the population covered under both programs.
3. Provide endpoints that allow querying the Patient and Coverage data synchronously.
4. Use the FHIR Bulk Data Access Implementation Guide[^4] (IG) version 2.0.0 and the Draft Bulk Data Import IG[^5] to receive Patient and Coverage data in bulk. Document all the assumptions and decisions you make in regards to the use and implementation of these IGs.
5. Be FHIR Release 4 (R4) compliant (for all the bulk and non-bulk operations and functionality).
6. Be built using Java, Go, Ruby or Python as the main programming language of the core API solution.

**As part of your submission, you must:**

* Submit a working solution of the Veteran Attribution API including any relevant and supporting documentation.
* Track any relevant product work in a Kanban board format.
* Submit a product plan that identifies the scope of the minimally viable product in relation to the broader program goals. It should also include any proposed objectives and key results to be tracked for this effort.
* Provide a high-level implementation plan strategy for the VA and CMS to adopt the Veteran Attribution API.
* Provide documentation for the end-user developers that will be integrating with the Veteran Attribution API.
* Submit any artifacts related to user research, usability testing, and human centered design, either performed or planned.
* Document the FHIR resources, profiles, extensions, and operations chosen for your implementation (as applicable) and explain why you selected each one.
* Include all the necessary instructions or automated scripts to build, provision resources, and install all software components.
* Perform a live virtual sprint demo session to present your solution and answer questions from your CMS product manager.

### **Data Elements**

You have been provided the following datasets to develop the minimum viable product of the Veteran Attribution API:

* [**CMS_MC_Patients.json**](data/CMS_MC_Patients.json) - Contains the patient information associated with the individuals covered under Medicare (FHIR bundle).
* [**CMS_MC_Coverage.json**](data/CMS_MC_Coverage.json) - Contains the Part A, Part B, and Part C coverage data associated with the individuals covered under Medicare (FHIR bundle).
* [**VA_Patients.json**](data/VA_Patients.json) - Contains the Veterans covered under the VA Health Benefits Program that must be matched against the Medicare recipients (FHIR bundle).
* [**VA_Coverage.json**](data/VA_Coverage.json) - Contains the coverage data associated with the individuals covered under the VA Health Benefits Program (FHIR bundle).

You must use the provided data sets for this technical challenge. Your solution must include the tools and/or scripts used to ingest the provided data, which may be used to ingest similarly formatted data. You may transform the data as needed. If a data discrepancy, gap, or mismatch is found, you must document the issue and explain how you would resolve it. If needed, you can generate additional synthetic data to complete this challenge. You must explain all of your technical decisions.


### Tech spec

- LINK TO SPEC

### Mocks / Design

- Insert Link to figma 
- Any relevant screens

### Other requirements

List all other non-functional requirements

# 🙆‍♀️ Release Criteria

## OKRs

### Objective: 
#### Key Result: 
#### Key Result: 

### Objective: 
#### Key Result:


### Minimum Criteria
List all metrics you're tracking and the desired value/trend for each metric


- [ ]  **Functionality**
    - [ ]  List minimum feature set for release?
- [ ]  **Usability**
    - [ ]  List minimum usability threshold
- [ ]  **Performance**
    - [ ]  List minimum performance requirement

### Test plan

Outline how you're planning testing coverage

# 🙅‍♀️ Out of Scope

List anything that is out of scope, this could be user persona's, user stories. 

- A full roadmap is not possible without the actual team and actual time. We can produce a high level thematic roadmap, but nothing deeper. 

# 🤦‍♀️ Risks

List any risks and potential mitigation

# 🤷‍♀️ Open Questions

List any outstanding questions