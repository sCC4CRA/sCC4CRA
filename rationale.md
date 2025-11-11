# Rationale for the analysis, changes and exclusions

This document describes the rationale used to develop this methodology.

## General
### EN17640 integration (Discarded)
It has been considered to align this methodology with EN 17640, the "Fixed-time cybersecurity evaluation methodology for ICT products" (also known as FITCEM). This standard is recognized as the first cybersecurity methodology specifically created to meet the requirements of the European Cybersecurity Act (CSA).

However, it has been determined that this standard is not fully aligned with the requirements of the CRA Regulation. While it would be possible to add a mapping to demonstrate compliance with the EN 17640 “Basic” assurance level, which allows self-assessment, this has been deemed unnecessary, as such mappings generally do not provide any practical benefit.

Therefore, the integration of this methodology with EN 17640 has been discarded for the time being, because:
* It does not provide any tangible benefit.
* It does not facilitate compliance for manufacturers.

If, in the future, aligning this methodology with EN 17640 is considered beneficial as it is a harmonized European standard, this decision will be reconsidered.

## CC-2022 R1 simplification
### General
#### Composition activities
The composition activities defined in [Common Criteria CC:2022 Release 1 Part 3](https://www.commoncriteriaportal.org/files/ccfiles/CC2022PART3R1.pdf) have been integrated into this methodology, as the CRA Regulation requires consideration of the PwDE and its components, including third-party components.  

The composition requirements from the standard Common Criteria methodology have been inherently included as requirements in this methodology, as shown below (some have also been discarded):

The following WU have been added:
* **ASE_COMP.1C and ASE_COMP.1.2C -> REQ.COMP-1:** The requirements from ASE_COMP.1 have been integrated into REQ.COMP-1; however, they have been greatly simplified, as the requirements from the standard Common Criteria are too formal.
* **ADV_COMP.1.1C -> ARC.COMP-1:** The requirements from ADV_COMP.1 have been integrated into ARC.COMP-1. In this case, they are considered to be well aligned; although the wording has been simplified, the requirements remain largely consistent.
* **ALC_COMP.1.1C -> SBM.COMP-1:** The requirements from ALC_COMP.1.1C have been integrated into SBM.COMP-1. In this case, they are considered to be well aligned, as the requirements of the CRA Regulation are consistent with the composition rules of the Common Criteria.

The following have been discarded:
* ALC_COMP.1.2C: Has not been added, since the Delivery procedure is not a requirement for CRA regulation.
* ATE_COMP.1.1C: Has not been added, since the PwDE is considered that is always tested as a whole.
* AVA_COMP.1.1C: Has not been added, since the PwDE is considered that is always tested as a whole.

The [ETR for Composition](rationale.md#etr-for-composition) has not been considered because, in general, is only shared between accredited CAB's, and the composition methodology for CRA Regulation is less restrictive just requiring the component guidance. Therefore, aiming not to be more restrictive than the regulation itself, the ETR for Composition report is not considerd for this methodology.

#### ETR for Composition
This is a report that, in general, is shared between the CC accredited CAB's. It is a restricted evaluation report that enables the secure reuse of a evaluated component within the whole product evaluation. Provides details; such as, the results of the penetration testing of the components and all vulnerabilities that have been considered for the component during its evaluation.

#### No Protection Profiles  
This methodology has been developed considering the scenario in which the Technical Documentation does not claim any Protection Profile (PP). The methodology is designed to be a built-in approach, keeping it simple. For now, Protection Profiles are not considered.  

The [CRA implementation by EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en) describes different scenarios in section 7.6. In future versions, this methodology may be adapted to align with the most appropriate scenario.  

#### No Reduced Scope (e.g., non-TOE)  
Concepts like non-TOE (e.g., identifying any non-TOE hardware/software/firmware required by the TOE) have been removed, since under CRA the entire product is within the evaluation scope. As a result, the concept of reduced evaluation scope is not considered; the entire PwDE is always in scope.  

#### SARs Removed  
The CC2022R1 defines different SARs based on the required assurance level. To simplify complexity, SAR levels have been removed and replaced with a fixed set of built-in SARs. Additionally, the concept of multi-assurance TOEs introduced in CC2022R1 has been discarded, as it has no direct equivalence with CRA and would add unnecessary complexity to the methodology.  

#### Self-Assessment  
Third-party certification and evaluation have been removed. All requirements and tasks originally assigned to the evaluator have been transferred to the manufacturer.  

#### Simplification  
The amount of text and formalities has been reduced to the bare minimum (e.g., *The statement of the Security Objectives shall describe the security objectives for the operational environment* → *Describe the security objectives for the operational environment*).  

#### Terminology Changes  
Some CC2022R1 concepts have been replaced with CRA terms. Since the intention of this methodology is to facilitate adoption by non-CC users, CRA terminology has been prioritized:  
  * **TOE → PwDE**  
  * **TSF → PwDE**  
  * **TSFI → Interface**  
  * **Developer → Manufacturer**  
  * **SFR → Security Functions**  
  * **SFR-enforcing → Security Function Enforcing**  
  * **each part → each component**  
  * **each user role → each end user**  
  * **Preparative → Installation** 

### ASE
#### TOE Overview and TOE Summary Simplified  
The redundancy of security features in the introduction has been removed from [ASE_INT.1], as it is considered redundant with [ASE_REQ.1].  

#### Manufacturer Information  
Manufacturer information, such as the **registered trade name or registered trademark of the manufacturer**, has been added in [ASE_INT.1]. In CC2022, this is generally not specifically required, but it has been included to ensure coverage of CRA regulatory requirements.  

#### Only Security Objectives for the Environment  
ASE_OBJ.2 has been considered unnecessary since *security objectives for the TOE* may be redundant and not required.  

#### SFRs Simplified  
[ASE_REQ] and [ASE_TSS] have been merged to facilitate description, improve understanding of security measures, and reduce complexity and redundancy:  
* SFR descriptions have been simplified, and operations have been removed.  
  * SFR naming, although not explicitly defined in this methodology, is open to definition and use. Suggested approaches include:  
    * Using a SESIP-like approach.  
    * Using the full name instead of CC2022 class identifiers (e.g., **FDP_SDI.1 → User Data. Stored Data Integrity Monitoring**). In any case, no strict rules are defined, except for providing a clear and understandable rationale.  

For this reason, the SFR concept has been simplified to **[Security Functions](definitions.md#security-function)**.  

#### ASE_CCL  
This CC2022R1 family focuses on declaring Conformance Claim justifications. This methodology uses a simplified structure with fixed built-in families and requirements. Furthermore, since Protection Profiles are not considered, this family has been removed.  

#### ASE_ECD  
This CC2022R1 family focuses on declaring formalities regarding Assurance and Security Requirements. Since this methodology has been simplified to remove such formalities, this family has been removed.   

### ADV
#### Security Domains  
The concept of **Security Domains** from [ADV_ARC] has been replaced with the concept of **limiting the attack surface** as defined by the CRA.  

#### ADV_FSP.2  
Although the document [CRA via EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en) correlates CRA requirements with [ADV_FSP.1], considering that [ADV_TDS.2] and an extended [ADV_ARC.1] are also required, it is more consistent to require at least [ADV_FSP.2].  

#### ADV_PDM.1  
The [CRA via EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en) states:  
* *The rationale for data minimisation shall identify all **user data** that is processed by the TOE.*  

However, the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires consideration of all data:  
* *process only **data, personal or other,** that are adequate, relevant and limited to what is necessary in relation to the intended purpose of the product with digital elements (data minimisation);*  

Therefore, the ADV_PDM.1 requirements in this methodology have been generalized to **all data processed, stored, or transferred by the PwDE**.  

#### ADV_INT  
This CC2022R1 family is intended for high-assurance evaluations to declare product development conformities. It has **not been considered in this methodology**.  

#### ADV_IMP  
This CC2022R1 family focuses on the evaluator’s analysis of the PwDE implementation. Since this methodology is **self-assessed**, this family has **not been considered**.  

### ALC
#### ALC_DEL  
This family has been removed. In the [CRA via EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en), there is no specific mapping between **ALC_DEL** and the CRA requirements.  

#### ALC_FLR  
This family has not been considered to cover the requirements of the [CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) Annex I, Part II. It is considered more appropriate and straightforward to follow the standards developed by **CEN/CENELEC** under the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) (Reference 15).  

#### ALC_PSR.1  
This family has not been considered to cover the requirements of the [CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) Annex I, Part II, for the same reason as **ALC_FLR**: it is more appropriate and straightforward to rely on standards developed by **CEN/CENELEC** under the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) (Reference 15).  

#### ALC_CMC  
This CC2022R1 family is not mentioned as necessary in the [Cyber Resilience Act implementation by EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Therefore, it has not been considered in this methodology.  

#### ALC_TAT  
Similar to ALC_CMC, this CC2022R1 family is not identified as necessary in the [Cyber Resilience Act implementation by EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Therefore, it has not been considered in this methodology. 

### ATE
#### ATE_COV.1  
The **ATE_COV** family has not been included, following the conclusions of the [CRA via EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en) document. While it could make sense to include it to ensure testing of all interfaces, this methodology excludes it to avoid being more restrictive than the [CRA via EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en) guidance validated by ENISA.  

#### ATE_IND.1  
This CC2022R1 family focuses exclusively on testing performed by an evaluator. Since this methodology is **self-assessed**, this family has not been considered.  

### AVA
#### Evaluator Work  
The **AVA_VAN.x** evaluator tasks have been reassigned as obligations for the manufacturer.  

#### Assurance Level  
The methodology aligns with **AVA_VAN.5**, not because of the required attack potential, but due to the level of assurance mandated by the [CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng). The regulation requires covering the entire product and all third-party components in the vulnerability analysis, as the PwDE *“shall be made available on the market without known exploitable vulnerabilities”*. This requirement is only fully addressed by applying an approach equivalent to **AVA_VAN.5**.

## CRA Compliance 
### Annex I Part I

| Requirement | Coverage | Comments |
|-------------|----------|----------|
| (1) | ❌ | This requirement is addressed by the **output** of the risk assessment, which is reflected in [ASE_SPD.1], [ASE_OBJ.1], and [ASE_REQ.1]. However, the detailed steps for performing the risk assessment are expected to be standardized by **CEN/CENELEC** under the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) (Reference 1). [Common Criteria CC:2022 Release 1](https://www.commoncriteriaportal.org/cc/index.cfm) does not cover the risk assessment. Therefore, it is more practical to directly rely on the standards proposed to comply with the [Cyber Resilience Act Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng). |
| (2)(a) | ✅ |  |
| (2)(b) | ✅ |  |
| (2)(c) | ❌ | The patch management mechanism and security updates are **out of scope** for this release. Although the [CRA via EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en) recommends using section "IV.4 Patch Management" of the EUCC and the CC family **ALC_FLR**, it is preferred to wait for guidance from the European Commission and the publication of horizontal standards developed by **CEN/CENELEC** as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) (Requests 1–15) before incorporating these requirements. [Common Criteria CC:2022 Release 1](https://www.commoncriteriaportal.org/cc/index.cfm) focuses mainly on product evaluation activities, and the new patch-related requirements may not yet be beneficial under the current methodology. Using horizontal standards may be more practical in such cases. |
| (2)(d) | ✅ |  |
| (2)(e) | ✅ |  |
| (2)(f) | ✅ |  |
| (2)(g) | ✅ |  |
| (2)(h) | ✅ |  |
| (2)(i) | ✅ |  |
| (2)(j) | ✅ |  |
| (2)(k) | ✅ |  |
| (2)(l) | ✅ |  |
| (2)(m) | ✅ |  |

For the rationale of the covered requirements see [Cyber Resilience Act implementation by EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en).

### Annex I Part II
Not Covered ❌. Same rationale as per the requirement "(2)(c)" of [Annex I Part I](rationale.md#annex-i-part-i).

### Annex VII
| Requirement |  Coverage      |  Comments    |
|---------|------------|-----------------|
|(1)|✅||
|(2)|🟡✅|Same rationale as per the requirement "(2)(c)" of [Annex I Part I](rationale.md#annex-i-part-i).|
|(3)|✅||
|(4)|✅||
|(5)|✅||
|(6)|✅||
|(7)|✅||
|(8)|✅||

All requirements (except for (2)) covered by [[ASE_INT.1]](methodology.md#-introduction-and-description-ase_int1).
