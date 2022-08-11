# BCDA PHASE II Tech Challenge: B2D2

[![hackmd-github-sync-badge](https://hackmd.io/sbj3SSUBQcS0MopOHU_mJg/badge)](https://hackmd.io/sbj3SSUBQcS0MopOHU_mJg)

###### tags: `Fearless` `BCDA`

This project is the next phase of the recompete. 
- [AB2D BCDA DPC Phase 2 Slides](https://docs.google.com/presentation/d/1ia_GMIe07c5pyClOg26LC1gAFpeeVRRxq8HLinyLd3E/edit#slide=id.g13f9ba05f80_0_6)
- [BCDA Core Notes to self :notebook:](/1BnjmuTIRAqMbKfbPsTZNA)
- [DPC Team Notes to self :notebook_with_decorative_cover:](/QkQD5B4KRQm4ha0uLVE10Q) 
- My [notes from the last pitch phase](https://docs.google.com/document/d/1xIRg033qUS9ah_BRTk-im4Gudj6KmoBq7T9tXMCNQR0/edit?usp=sharing)
- [Team Working Agreement Aug 9, 2022](https://docs.google.com/document/d/1BHS-bpRGAfv3KsFnEDDMxCXi4vqAhVCY/edit#heading=h.1fob9te)
- Github repo [BCDA-DPC-B2D2-Veteran-Attribution-API](https://github.com/FearlessSolutions/BCDA-DPC-B2D2-Veteran-Attribution-API)
- Team [Kanban board on Github](https://github.com/orgs/FearlessSolutions/projects/1/views/1)
- [Veteran Attribution API PRD](https://hackmd.io/@mrmetaverse/b2d2-tech-challenge-PRD) Addresses the Product requirements section 
- [Veteran Attribution API OKRs draft](/cwYy9UMJTw-2mntAE2A-Bg)




### Who is on the team? 

<details>
A max of 10 people will be speaking at orals. Those who speak at orals are expected to work on the technical challenge. If anyone from a subcontractor participates in orals, they are automatically labeled as key personnel. 
    
* Yetty - BD Account/Proposal Manager 
* Nichole - Portfolio Director H+S
* Beth - Program Manager
* Laila - Tech Lead 
* Jesse - Product lead 
* Ben - ISSO SME, expressed that he can help but is stretched on other projects, not comfortable being the only security SME on challenge


    
<summary>click to expand</summary>

![](https://hackmd.io/_uploads/BJqiM25p5.png)
    
ben.ohe@semanticbits.com,
Beth Wingerd <bwingerd@fearless.tech>,
Christopher Brune <cbrune@fearless.tech>,
courtney.wright@semanticbits.com,
David Tisza <dtisza@fearless.tech>,
Nick Saccente <nsaccente@fearless.tech>,
Nichole Weems <nweems@fearless.tech>,
Robert Cummings <rcummings@fearless.tech>,
Rick Giese <rgiese@flexion.us>,
Tianna Woodson <twoodson@fearless.tech>,
Yetty Ibitoye <yibitoye@fearless.tech>
tdinoff@flexion.us
sappachi@flexion.us
sharshar@gmail.com
krobertson@flexion.us
jtipton@flexion.us

</details>
    
<br />



### Which channels do we use to communicate? 
- slack channel :unlock: `#prop-cms-ab2d-bcda-dpc`
- slack channel :lock: `#prop-bcda-dpc-ab2d-techchallenge`
- Github repo: :lock: `https://github.com/FearlessSolutions/BCDA-DPC-B2D2-Veteran-Attribution-API`

---

# Technical Exercise - Veteran Attribution API (RFQ-230240)

> _**Note:** This is a hypothetical technical challenge scenario designed for respondents to showcase relevant skillsets for the purpose of this acquisition. Please refer to RFQ-230240 and the Statement of Objectives document for the full scope of this award._

## Background

The Centers for Medicare & Medicaid Services (CMS) have played a key role in the standardization and implementation of data sharing services using the Fast Healthcare Interoperability Resources (FHIR) data standard[^1]. As such, it has built an ecosystem of API products that provides Medicare Providers, Alternative Payment Model participants and Medicare Part D Plans with claims data in order to improve care coordination and the delivery of care to its Medicare population.

As part of the CMS 2022 Strategic Plan[^2], the agency has established two new strategic pillars intended to advance its data sharing efforts by better serving its most vulnerable populations. The strategic pillars include:

* Advancing health equity by addressing the health disparities that underlie our health system; and
* Driving innovation to tackle our health system challenges and promote value-based, person-centered care.

Similarly, the U.S. Department of Veterans Affairs (VA) – who is a partner Federal agency that coordinates, provides, and pays for healthcare benefits – has defined similar strategic goals and objectives including a commitment to "emphasize the delivery of benefits, care and services to underserved, marginalized and at-risk Veterans"[^3].

Driven by their aligned strategic plans and informed by feedback from industry partners, CMS and the VA have identified a joint opportunity in which CMS will provide Medicare claims data to the VA in order to improve the care coordination and delivery of care for Veterans that are covered under Medicare and the VA health care benefits program.

## Technical Exercise

Today, CMS has the ability to identify the population of "dual-beneficiaries" under the Medicare and Medicaid programs given its role in the management and operation of both programs. However, when looking at the population of individuals covered by both Medicare and the VA health benefits programs, each of the agencies possess separate pieces of the data puzzle. Before CMS can send Medicare claims data to the VA, both agencies need to exchange demographic and coverage information of its patients and agree on a method to identify and build this population on an ongoing basis.

You are part of a newly onboarded CMS agile team that has been tasked with building an Application Programming Interface (API) that will be used by the VA to submit their patient’s data to CMS using FHIR. This new API has been named the _Veteran Attribution API_. CMS envisions a minimum viable product that allows the VA to send Patient and Coverage data to CMS in bulk. The API must also allow CMS users to query the Patient and Coverage data individually.


> :notebook:[Veteran Attribution API PRD](/HVEGF4jcTk-Vul1v_1b-gw)


The Veteran Attribution API implementation must:

1. Have an authentication/authorization mechanism.
2. Implement a mechanism to match patients using the CMS and VA data provided and identify the population covered under both programs.
3. Provide endpoints that allow querying the Patient and Coverage data synchronously.
4. Use the FHIR Bulk Data Access Implementation Guide[^4] (IG) version 2.0.0 and the Draft Bulk Data Import IG[^5] to receive Patient and Coverage data in bulk. Document all the assumptions and decisions you make in regards to the use and implementation of these IGs.
5. Be FHIR Release 4 (R4) compliant (for all the bulk and non-bulk operations and functionality).
6. Be built using Java, Go, Ruby or Python as the main programming language of the core API solution.

As part of your submission, you must:

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

### **Additional Resources**

1. **Discovery Sprint Report**
    * Description: Report of the discovery sprint performed by the Data and Analytics Strategy Group around this API ecosystem.
    * File: [CMS-DASG-Discovery-Sprint-Summary.pdf](docs/CMS-DASG-Discovery-Sprint-Summary.pdf)

2. **CMS Strategic Plan**
    * Description: CMS Strategic Plan Pillars and Cross-Cutting Initiatives.
    * Website: https://www.cms.gov/cms-strategic-plan
    * File: [CMS-Strategic-Plan-Cross-Cutting-Initiatives.pdf](docs/CMS-Strategic-Plan-Cross-Cutting-Initiatives.pdf)

3. **VA Strategic Plan**
    * Description: Department of Veterans Affairs Fiscal Years 2022-28 Strategic Plan.
    * Website: https://www.research.va.gov/about/strategic_plan.cfm
    * File: [VA-Strategic-Plan-2022-2028.pdf](docs/VA-Strategic-Plan-2022-2028.pdf)

4. **Policies and Technology for Interoperability and Burden Reduction**
    * Description: Policies and Technology for Interoperability and Burden Reduction.
    * Website: https://www.cms.gov/Regulations-and-Guidance/Guidance/Interoperability/index 

5. **Publication: Improving Care Coordination for Veterans Within VA and Across Healthcare Systems**
    * Description: Article describing some of the care coordination challenges faced Veterans in the United States.
    * Citation: Cordasco, K.M., Hynes, D.M., Mattocks, K.M. _et al._ Improving Care Coordination for Veterans Within VA and Across Healthcare Systems. _J GEN INTERN MED_ 34, 1–3 (2019). https://doi.org/10.1007/s11606-019-04999-4
    * File: [Article-Improving-Care-Coordination-For-Veterans.pdf](docs/Article-Improving-Care-Coordination-For-Veterans.pdf)

## Success Criteria

The following categories and criteria will be used by the Government to evaluate each Respondent’s Technical Exercise:

### Technical Solution

CMS will evaluate the Respondent’s ability to technically design, implement and deliver a working software solution. For a submission to be considered “working software solution” it must be deployable, usable, and testable by CMS with minimum effort and using sample test data. CMS should be able to follow the instructions and documentation provided by the Respondent without requiring debugging or reverse engineering undocumented steps.

Solutions will be evaluated on their simplicity, code quality, performance, accuracy, security, maintainability and scalability. Adherence and implementation of best technical practices will be considered. The Government will also evaluate the technical choices, assumptions and decisions made as part of the proposed solution, including features that were not implemented but documented and proposed as future enhancements. Bugs, defects and errors encountered when using and testing the working software solution will be considered for evaluation purposes.

### Product Delivery

CMS will evaluate the Respondent’s ability to establish a product vision and strategy, define a minimally viable product, establish and measure objectives and key results (OKRs) and prioritize work. The Government will evaluate the agile process and activities established to perform the work. Elements like milestone definitions, user stories, definition of done, and any other product-related artifact will be evaluated. Adherence and implementation of best product management practices and strategies will be considered. The Government will also evaluate the product roadmap, decisions made and the ability to communicate the overall strategy to deliver the proposed solution.

### Human-Centered Design

CMS will evaluate the Respondent’s ability to plan and perform user research, usability testing, and any other activity or strategy considered part of a human-centered approach. The Government will evaluate any plans, designs, protocols, activities and any other artifact used as part of a human-centered design practice. Adherence and implementation of best practices and strategies for human-centered design will be considered.

### Data Management

CMS will evaluate the Respondent’s ability to understand, process and use the provided data as part of the working software solution. The Government will evaluate the understanding, selection and implementation of the various FHIR resources, profiles, extensions and operations that become part of the submitted solution.

### Additional Elements

CMS has sole discretion to categorize an artifact or element of the submitted solution when it overlaps or relates to one or more of the previously defined categories.

## Technical Exercise Assumptions

The following assumptions should also be considered in designing and implementing the technical exercise submission:

* The evaluation environment will reside in the AWS East Commercial cloud.
* All AWS services currently approved for FedRAMP Moderate (East/West) or undergoing JAB Review or 3PAO Assessment can be used. If in doubt, please submit any questions to the Contracting Officer for clarification.
* It is not required that the solution is exclusively based on AWS services.
* Open-source tools, libraries, and technologies can be used and are encouraged. The scripts, tooling, and instructions to instantiate any service to be hosted within the AWS environment must be part of the challenge submission.
* For the scope of this challenge, the AWS environment has outbound access to the internet.
* For the scope of this challenge, internet-available repositories can be accessed and used (e.g. operating systems, libraries, packages, containers, etc.).
* Consider the security standards appropriate for receiving, sending, or hosting Personal Identifiable Information and Protected Health Information in your implementation.
* For the scope of this challenge, subscription-based Software as a Service (SaaS) solutions can be used only if a free trial is available to the government. Respondents must explain in detail the rationale, decision making process, and any evaluations made to select such service. CMS will not pay for anything included as part of the solution. If in doubt, please submit any questions to the Contracting Officer for clarification.
* CMS will not purchase or accept a purchased license for any product or service.
* The respondent's solution will be deployed in an AWS environment that may already contain provisioned services or resources in it. The respondent is responsible to account for that possibility.


1. Policies and Technology for Interoperability and Burden Reduction: https://www.cms.gov/Regulations-and-Guidance/Guidance/Interoperability/index

2. CMS 2022 Strategic Plan: https://www.cms.gov/cms-strategic-plan

3. VA Strategic Plan 2022-2028: https://www.va.gov/oei/docs/va-strategic-plan-2022-2028.pdf

4. https://hl7.org/fhir/uv/bulkdata/

5. https://github.com/smart-on-fhir/bulk-import



-----

# Archive & Resources 

<details>
<summary>Planning phase</summary>

## About B2D2


This project is the next phase of the recompete. 
- [AB2D BCDA DPC Phase 2 Slides](https://docs.google.com/presentation/d/1ia_GMIe07c5pyClOg26LC1gAFpeeVRRxq8HLinyLd3E/edit#slide=id.g13f9ba05f80_0_6)
- [BCDA Core Notes to self :notebook:](/1BnjmuTIRAqMbKfbPsTZNA)
- [DPC Team Notes to self :notebook_with_decorative_cover:](/QkQD5B4KRQm4ha0uLVE10Q) 
- My [notes from the last pitch phase](https://docs.google.com/document/d/1xIRg033qUS9ah_BRTk-im4Gudj6KmoBq7T9tXMCNQR0/edit?usp=sharing)



### Who is on the team? 

<details>
<summary>click to expand</summary>

![](https://hackmd.io/_uploads/BJqiM25p5.png)
    
ben.ohe@semanticbits.com,
Beth Wingerd <bwingerd@fearless.tech>,
Christopher Brune <cbrune@fearless.tech>,
courtney.wright@semanticbits.com,
David Tisza <dtisza@fearless.tech>,
Nick Saccente <nsaccente@fearless.tech>,
Nichole Weems <nweems@fearless.tech>,
Robert Cummings <rcummings@fearless.tech>,
Rick Giese <rgiese@flexion.us>,
Tianna Woodson <twoodson@fearless.tech>,
Yetty Ibitoye <yibitoye@fearless.tech>
tdinoff@flexion.us
sappachi@flexion.us
sharshar@gmail.com
krobertson@flexion.us
jtipton@flexion.us

</details>
<br />

Yetty - BD Account/Proposal Manager 
Nichole - Portfolio Director H+S
Beth - Program Manager
Laila - Tech Lead 
Jesse - Product lead 
Ben - ISSO SME, expressed that he can help but is stretched on other projects, not comfortable being the only security SME on challenge

Max of 10 people will be speaking at orals. Those who speak at orals are expected to work on the technical challenge. If anyone from a subcontractor participates in orals, they are automatically labeled as key personnel. 




### Which channels do we use to communicate? 
- slack channel :unlock: `#prop-cms-ab2d-bcda-dpc`
- slack channel :lock: `#prop-bcda-dpc-ab2d-techchallenge`
- Github repo: :lock: ``


## :bulb: Why are we here? 

We were selected for the down-select to advance to the technical challenge, and pitch. 

## :woman: Who is impacted by our work? 

- CMS 
- Staff and Partners: SemanticBits, Flexion, Fearless
- The Public who benefit from CMS 

## :dart: Goals: What do we hope to accomplish? 

- We generally get a handful of instructions from the government.
- We generally are expected to produce a working solution in `14*` days. 
- We want to approach this as a technical project team. 
- We will ideate possibilities to be ready for the challenge. At the time that we get the challenge, we want to be able to hit the ground running. 
- ![](https://hackmd.io/_uploads/ByK8Lh9Tq.png)
- ![](https://hackmd.io/_uploads/BycPIhc65.png)
    
### Aug 9, 2022 
- we are meeting today at 08/09/22 to get the team together for some logistics/house-keeping items that could slow us down from moving at full speed. 
    - [x] schedule or async team working agreement 
        - async updates
        - in person 2 times a week
        - we will use github to manage our work  
        - we will use this readme as a crosswalk source of truth (until another tool is identified) 
        - [Team Working Agreement Aug 9, 2022](https://docs.google.com/document/d/1BHS-bpRGAfv3KsFnEDDMxCXi4vqAhVCY/edit#heading=h.1fob9te)
    - [x] how will we manage our kanban? 
        - [ ] set up kanban (*github*)
    - [x] team name
        **Team name suggestions:**
            * **BAD** - acronym for BCDA AB2D DPC
            * Actively Promoting Interoperability - **API**
            * **B2D2** Big Bad Data Delivery
        - [ ] do we have any assumptions about the tech stack, etc.? Anything we should have ready? i.e. serverless-in-a-box, or headless-drupal ready to deploy, etc. 
            - [ ] Can we create little snippets of documentation? 

</details>

<details>
<summary>Extras (OKRs)</summary>

## When you are ready for OKRS: 

[![](https://hackmd.io/_uploads/Sk5ll6dw9.png)](https://jeffgothelf.com/blog/okr-anti-pattern-creating-okrs-to-fit-your-backlog/)

### The problem with SMART Goals
>Never Start with “S.M.A.R.T” (specific, measurable, attainable, realistic, and time-bound ) Goals - Why? Because SMART goals are almost always small goals, created by small-minded people who have small dreams and attempt to complete small tasks that keep them busy but not extraordinary. Achieving significant things—real dreams and aspirations that demand real power and guts—requires bigger thinking.
>We need to broaden up our perspective if we want to feel energized enough to achieve something meaningful. Instead, try **“D.U.M.B” goals.** This stands for dream-focused, uplifting, method-based, behavior-triggered goals.

## Assumptions: 
*Typical questions might include:*

Who are our users?
What is the product used for?
When is it used?
What situations is it used in?
What will be the most important functionality?
What’s the biggest risk to product delivery?

The hypotheses created in Lean UX are designed to test our assumptions. There’s a simple format that you can use to create your own hypotheses, quickly and easily.

An example:

We believe that enabling people to save their progress at any time is essential for smartphone users. This will achieve a higher level of sign up completions. We will have demonstrated this when we can measure an improvement of the current completion rate of 20%.

We state the belief and why it is important and who it is important to. Then we follow that with what we expect to achieve. Finally, we determine what evidence we would need to collect to prove that our belief was true.

![](https://hackmd.io/_uploads/HyQSjXd89.png)


</details>
