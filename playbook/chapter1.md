# Chapter 1 - Manufacturer risk assessment

## 📘 Introduction and Description (ASE_INT.1)

### IAD-1 - The Technical Documentation introduction shall have a unique name and version
1. MUST have a unique reference with a unique name and version.
1. The [unique identification](../definitions.md#unique-identification) MUST clearly distinguish from other Technical Documentations.

### IAD-2 - The Technical Documentation introduction shall include the manufacturer information
1. MUST be indicated the name, registered trade name or registered trademark of the manufacturer.
1. MUST be indicated the postal address, email address or other digital contact details.
1. Where applicable, MUST be indicated the website where the manufacturer can be contacted.
1. The contact details MUST be in a language which can be easily understood by users and market surveillance authorities.
1. MUST be included the [single point of contact](../definitions.md#single-point-of-contact) that enables users to communicate with them.
1. MUST be included the type of technical security support offered to handle vulnerabilities and manage security updates.

### IAD-3 - The Technical Documentation introduction shall include CRA compliance statements.
1. SHOULD be declared any [harmonised standard](https://single-market-economy.ec.europa.eu/single-market/goods/european-standards/harmonised-standards_en) fully or partially applied.
1. SHOULD be declared any [common specifications](https://health.ec.europa.eu/medical-devices-vitro-diagnostics/common-specifications_en) fully or partially applied.
1. SHOULD be declared any [European cybersecurity certification](https://certification.enisa.europa.eu/index_en) fully or partially applied.
1. SHOULD be declared any other relevant technical specifications applied.
1. If partly applied, the technical documentation MUST specify the parts which have been applied.
1. MUST contain a copy of the EU declaration of conformity.

### IAD-4 - The Technical Documentation introduction shall uniquely identify the PwDE
1. The PwDE MUST have a unique reference with a unique name and version.
1. The [unique identification](../definitions.md#unique-identification) MUST clearly distinguish from other PwDEs.
1. The PwDE MUST bear a type, batch or serial number or other element.
1. The PwDE unique reference MIGHT be provided on their packaging or in a document accompanying the PwDE.

### IAD-5 - The PwDE description shall identify the product type
1. The PwDE description MUST describe the [product type](../definitions.md#-product-type).
2. The PwDE description MUST be clear and not misleading.

### IAD-6 - The PwDE description shall summarize the usage
1. MUST clearly describe the [intended purpose](../definitions.md#intended-purpose).
1. MUST clearly describe the [reasonably foreseeable use](../definitions.md#reasonably-foreseeable-use).
1. MUST clearly describe the [reasonably foreseeable misuse](../definitions.md#reasonably-foreseeable-misuse).
1. MUST describe the expected time to be in use and its [support period](../definitions.md#support-period).
1. MUST describe the relevant information that was taken into account to determine the support period.

### IAD-7 - The PwDE description shall describe the physical description of the PwDE.
1. MUST clearly describe all hardware, firmware, software and guidance components that constitute the PwDE.
1. For each separately delivered part MUST be identified by a [unique identification](../definitions.md#unique-identification).
1. For each separately delivered part format (e.g., binary, PDF) MUST be described.
1. For each separately delivered part, the delivery method used to provide it to the end user MUST be described.
1. Optionally, MIGHT also include the SBOM as described in [[ALC_SBM.1]](../methodology.md#-sbom-alc_cms2--alc_sbm1).
1. For HW PwDEs, MUST include photographs or illustrations showing external features, marking and internal layout.
1. For products with multiple physical components, all of them MUST be identified and described.

### IAD-8 - The PwDE description shall describe the logical description of the PwDE.
1. MUST clearly describe the logical security features offered by the PwDE.
1. For products with multiple configurations, all of them MUST be identified and described.

## 🛡️ Risk Assessment Analysis (ASE_SPD.1)
### SPD-1 - Describe all threats in terms of a threat agent, an asset and an adverse action.
1. MUST consider the length of time the product is expected to be in use.
1. MUST include a risk-based analysis of cybersecurity risks based on the [intended purpose](../definitions.md#intended-purpose).
1. MUST include a risk-based analysis of cybersecurity risks based on the [reasonably foreseeable use](../definitions.md#reasonably-foreseeable-use).
1. MUST describe the conditions of use, of the PwDE.
1. MUST describe the [security impact and probability](../definitions.md#-security-impact-and-probability) for each of the threats.
1. MUST indicate whether and how the security requirements set out in [Annex I](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_I) Part I(2) are applicable to the PwDE.
1. MUST also indicate how the manufacturer is to apply [Annex I](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_I) Part I(1).
1. MUST also indicate how the manufacturer is to apply vulnerability handling requirements set out in [Annex I](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_I) Part II.
1. It MUST be coherent with [ASE_INT.1](../methodology.md#-introduction-and-description-ase_int1).
1. If certain [ESRs are not applicable](../definitions.md#non-applicability-of-an-esr), it MUST be included a clear justification.
### SPD-2 - Describe the Security Policies.
1. Each [Security Policy](../definitions.md#security-policies) is explained in sufficient detail to make it clearly understandable.
### SPD-3 - Describe the assumptions about the operational environment of the PwDE.
1. Each [assumption](../definitions.md#assumptions) is explained in enough detail for end users to understand.
## 🎯 Security Objectives (ASE_OBJ.1)
### OBJ-1 - Describe the security objectives for the operational environment.
1. The [security objectives for the operational environment](../definitions.md#security-objectives-for-the-operational-environment) may support the PwDE security functionality.
### OBJ-2 - Trace each security objective for the operational environment to the threat it addresses.
1. Each security objective for the operational environment MAY trace back to threats.
1. Each security objective for the operational environment MUST trace back to at least one threat, Security Policy or assumption.
1. MUST be coherent with [ASE_SPD.1](../methodology.md#%EF%B8%8F-risk-assessment-analysis-ase_spd1).
### OBJ-3 - Trace each security objective for the operational environment to the Security Policies which it enforces.
1. Each security objective for the operational environment MAY trace back to Security Policies.
1. Each security objective for the operational environment MUST trace back to at least one threat, Security Policy or assumption.
1. MUST be coherent with [ASE_SPD.1](../methodology.md#%EF%B8%8F-risk-assessment-analysis-ase_spd1).
### OBJ-4 - Trace each security objective for the operational environment to the assumptions it supports.
1. Each security objective for the operational environment MAY trace back to assumptions.
1. Each security objective for the operational environment MUST trace back to at least one threat, Security Policy or assumption.
1. MUST be coherent with [ASE_SPD.1](../methodology.md#%EF%B8%8F-risk-assessment-analysis-ase_spd1).
### OBJ-5 - Demonstrate that the security objectives for the operational environment uphold all assumptions.
1. All security objectives for the operational environment related to an assumption MUST support maintaining the operational environment.

## 🔐 Security Functionalities (ASE_REQ.1 & ASE_TSS.1)
### REQ-1 - Describe the Security Functions of the PwDE.
1. The [Security Functions](../definitions.md#security-function) MUST be described considering the related end users.
1. MUST be well-defined and no misunderstanding may occur due to the introduction of vague terms.
1. MUST be described for an audience assumed to have a reasonable knowledge of IT, security and the CRA.
1. SHOULD add a [Security Function](../definitions.md#security-function) to cover the [Reset to its original state](../definitions.md#reset-to-its-original-state-requirement).
1. MUST add a [Security Function](../definitions.md#security-function) to cover the [Identification, Authentication and Access Management Mechanism](../definitions.md#identification-authentication-and-access-management-mechanism-requirement).
1. MUST add a [Security Function](../definitions.md#security-function) to cover the [Reporting unauthorized access Mechanism](../definitions.md#reporting-unauthorized-access-requirement).
1. MUST add a [Security Function](../definitions.md#security-function) to cover the [Confidential data Mechanism](../definitions.md#confidential-data-requirement).
1. MUST add a [Security Function](../definitions.md#security-function) to cover the [Integrity of data Mechanism](../definitions.md#integrity-of-data-requirement).
1. MUST add a [Security Function](../definitions.md#security-function) to cover the [Availability of functions](../definitions.md#availability-of-functions-requirement).
1. MUST add a [Security Function](../definitions.md#security-function) to cover the [Minimise impact](../definitions.md#minimise-impact-requirement).
1. MUST add a [Security Function](../definitions.md#security-function) to cover the [Mitigation mechanism](../definitions.md#mitigation-mechanism-requirement).
1. MUST add a [Security Function](../definitions.md#security-function) to cover the [Recording and Monitoring](../definitions.md#recording-and-monitoring-requirement).
1. MUST add a [Security Function](../definitions.md#security-function) to cover the [Removal of Data](../definitions.md#removal-of-data-requirement).

### REQ-2 - For each threat, the Security Functions must demonstrate that they are suitable to meet that threat.
1. Each [Security Function](../definitions.md#security-function) MUST trace back to at least one threat for the PwDE.
1. The justification for a threat MUST show whether the threat is removed, diminished or mitigated.

### REQ-3 - The Security Functions must demonstrate that they are suitable to enforce each Security Policy.
1. Each Security Policy MUST trace back to Security Functions or Security Objectives of the [[ASE_REQ.1]](../methodology.md#-security-functionalities-ase_req1--ase_tss1) or [[ASE_OBJ.1]](../methodology.md#-security-objectives-ase_obj1).
1. The Security Policy MUST be satisfied if all related Security Functions are implemented and all related assumptions hold.
1. The TOE MUST provide mechanisms to enforce those Security Functions so that the Security Policy is covered.
1. Each Security Function that traces back to a Security Policy MUST actually contribute to the enforcement of it.
1. The tracing MUST NOT just be a simple relation of Security Functions with Security Policies, but a detailed explanation.
1. MUST be coherent with [ASE_SPD.1](../methodology.md#%EF%B8%8F-risk-assessment-analysis-ase_spd1).

### REQ-4 - Shall be internally consistent.
1. All [Security Functions](../definitions.md#security-function) MUST logically fit together without contradictions or ambiguities.

****

Go to next [Chapter 2 - Guidance ➡️ ](chapter2.md) 
