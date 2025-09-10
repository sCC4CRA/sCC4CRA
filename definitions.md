# Definitions

The following are the concepts transported from [CC2022R1](https://www.commoncriteriaportal.org/cc/index.cfm) or [CRA regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng). 

⚠️ The definitions highligthed with "👉❗" are intended to be updated with further clarifications or guidance by the European Commision. 

## From Common Criteria 2022 R1 methodology
### Assumptions
The assumptions are made about the operational environment to ensure the PwDE can provide its security functionality. If the PwDE is placed in an operational environment that does not meet these assumptions, it may be unable to provide all of its security functionality. Assumptions may concern the physical environment, personnel, and connectivity of the operational environment.

### Interactions
A description of interactions among or between subsystems identifies the reasons subsystems or modules communicate and characterizes the information that is passed. It need not define the information to the same level of detail as an interface specification. For example, it would be sufficient to say: “Subsystem X requests a block of memory from the memory manager, which responds with the location of the allocated memory.”

### OSPs
Organizational security policies (OSPs) are security rules, procedures, or guidelines imposed in the operational environment. OSPs can be established by an organization controlling the operational environment of the PwDE, or by legislative or regulatory bodies. OSPs can apply to the PwDE and/or its operational environment.

OSPs are defined in terms of rules or guidelines that must be followed by the PwDE and/or its environment. The OSPs MAY NOT be needed if all security objectives are derived from assumptions and threats only.

### Maintain security
Refers to the measures required to ensure the PwDE remains protected during delivery. Interpretation depends on:
* Nature of the PwDE (hardware, software, or both).
* Declared security level and attacker potential; delivery must not weaken overall security.
* Security objectives for the environment are maintained.

### Method of use
The interface's method of use describes how the interface is intended to be used. This description should be built around the various interactions available at that interface. For instance, if the interface were a Unix command shell, `ls`, `mv`, and `cp` would be interactions for that interface. For each interaction, the method of use describes what the interaction does, both for behaviour seen at the interface (e.g., the programmer calling the API, the Windows user changing a setting in the registry) as well as behaviour at other interfaces (e.g., generating an audit record). The method of use summarizes how the interface is manipulated in order to invoke the Security Functions.

### Non-bypassability
Non-bypassability is a property ensuring that the security functionality of the PwDE (as specified by the Security Function) is always invoked and cannot be circumvented when appropriate for that specific mechanism. For example, if access control to files is specified as a capability of the PwDE via a Security Function, there must be no interfaces through which files can be accessed without invoking the PwDE's access control mechanism. An interface that allows raw disk access could be an example of such a bypass.

### Parameter
Parameters are explicit inputs to and outputs from an interface that control the behaviour of that interface. A parameter description explains the parameter in a meaningful way. For instance, an acceptable parameter description for interface `foo(i)` would be: “parameter `i` is an integer that indicates the number of users currently logged in to the system.” A description such as “parameter `i` is an integer” is not sufficient.

### Purpose
The purpose of an interface is a high-level description of the general goal of the interface (e.g., process GUI commands, receive network packets, provide printer output, etc.). It is a general statement summarising the functionality provided by the interface.

### Privilege
A PwDE can implement the notion of privilege and protect itself by using privileged-mode routines to handle user data. The PwDE can make use of processor-based separation mechanisms (e.g., privilege levels or rings) to separate TSF code and data from user code and data. This concept can be applied in different types of products in various forms.

### Security Enforcing Interfaces
An interface is Security Enforcing if it triggers any [Security Function](definitions.md#security-function) from [[ASE_REQ.1]](methodology.md#-security-functionalities-ase_req1--ase_tss1). Some interfaces may enforce [Security Function](definitions.md#security-function), while others may not.

### Self-protection
Self-protection refers to the ability of the TSF to protect itself from manipulation by external entities that may result in changes to the TSF. Without these properties, the TSF could be disabled from performing its security services. The notion of self-protection applies only to the services provided by the PwDE through its interfaces.

### Security objectives for the operational environment
The operational environment of the PwDE implements technical and procedural measures to assist the PwDE in correctly providing its security functionality, which is defined by the security objectives for the PwDE. This pair-wise solution is called the security objectives for the operational environment and consists of a set of statements describing the goals that the operational environment shall achieve.

Examples of security objectives for the operational environment are:
* The operational environment shall provide a workstation with OS Linux version 3.01b to execute the PwDE.
* The operational environment shall ensure that all human PwDE users receive appropriate training before allowing them to work with the PwDE.
* The operational environment of the PwDE shall restrict physical access to the PwDE to administrative personnel and maintenance personnel accompanied by administrative personnel.
* The operational environment shall ensure the confidentiality of the audit logs received from the PwDE on the Audit Server.

### Subsystem
A subsystem is a description of the design of the TOE; it provides a high-level description of what a portion of the TOE is doing and how. A subsystem may be further divided into lower-level subsystems or modules. Very complex TOEs can require several levels of subsystems to adequately convey a useful description of how the PwDE works. Very simple PwDEs, in contrast, might not require a subsystem level of description; the module can clearly describe how the PwDE works.

### Threat agent
An entity that has the potential to exercise adverse actions on assets protected by the PwDE. Threat agents may be further described by aspects such as expertise, resources, opportunity, and motivation.

### Unique Identification
Unique identification can be achieved using elements like a version number or publication date.

## From CRA regulation
### Access management mechanism Requirement

The Requirement of the Annex I Part I (2)(d) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *ensure protection from unauthorised access by appropriate control mechanisms, including but not limited to authentication, identity or access management systems, and report on possible unauthorised access;*

The Access Management requirement needs to be covered by Security Functions. As an example from CC2022R1:

**Access control**
* The PwDE enforces the {list of Control Mechanisms} on {list of subjects, objects and operations among subjects and objects covered}.
* The TSF shall enforce the {access controls} to objects based on the following: {list of subjects and objects controlled}.

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(d)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### Availability of functions Requirement
The Requirement of the Annex I Part I (2)(h) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *protect the availability of essential and basic functions, also after an incident, including through resilience and mitigation measures against denial-of-service attacks;*

This requirement needs to be covered by Security Functions. As an example using CC2022R1:

* **Degraded fault tolerance**
  * The TSF shall ensure the operation of {List the Security mechanisms} when the following failures occur: {List the types of failures}.

* **Failure with preservation of secure state**
  * The PwDE preserves a secure state when the following types of failures occur: {List the types of failures}.

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(h)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### Actively exploited vulnerabilities
Means a vulnerability for which there is reliable evidence that a malicious actor has exploited it in a system without permission of the system owner. Actively exploited vulnerabilities concern instances where a manufacturer establishes that a security breach affecting its users or any other natural or legal persons has resulted from a malicious actor exploiting a flaw in one of the products with digital elements made available on the market by the manufacturer.

Examples of such vulnerabilities could be weaknesses in a product’s identification and authentication functions. Vulnerabilities discovered with no malicious intent, for purposes of good-faith testing, investigation, correction, or disclosure to promote the security or safety of the system owner and its users, should not be subject to mandatory notification.

Severe incidents impacting the security of the product with digital elements refer to situations where a cybersecurity incident affects the development, production, or maintenance processes of the manufacturer in such a way that it could increase cybersecurity risk for users or other persons. Such an incident could include a situation where an attacker has successfully introduced malicious code into the release channel via which the manufacturer releases security updates to users.

### Authentication mechanism Requirement

The Requirement of the Annex I Part I (2)(d) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *ensure protection from unauthorised access by appropriate control mechanisms, including but not limited to authentication, identity or access management systems, and report on possible unauthorised access;*

The Authentication requirement needs to be covered by Security Functions. As an example from CC2022R1:

* **End User authentication**
  * The PwDE allows {list of actions} on behalf of the user to be performed before the user is authenticated.
  * The PwDE requires each user to be successfully authenticated before allowing any other TSF-mediated actions on behalf of that user.

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(d)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### Confidential Data Requirement

The Requirement of the Annex I Part I (2)(e) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *protect the confidentiality of stored, transmitted or otherwise processed data, personal or other, such as by encrypting relevant data at rest or in transit by state of the art mechanisms, and by using other technical means;*

This requirement needs to be covered by Security Functions. As an example using CC2022R1:

* **Stored data confidentiality**
  * The PwDE ensures the confidentiality of {Choose data} while it is stored in the {Choose memories}, providing memory encryption with robust [cryptographic algorithms](../definitions.md#cryptographic-algorithm) {Choose algorithms}.

**Inter-PwDE trusted channels**
* The PwDE provides a communication channel between itself and another trusted IT product that is logically distinct from other communication channels and provides assured identification of its endpoints and protection of the channel data from modification or disclosure.
* The PwDE permits {Indicate end points} to initiate communication via the trusted channel.
* The PwDE initiates communication via the trusted channel for {list of functions for which a trusted channel is required}.

**Trusted path**
* The PwDE provides a communication path between itself and {selection: remote or local} users that is logically distinct from other communication paths and provides assured identification of its endpoints and protection of the communicated data from {selection: modification, disclosure, or {Other types}}.
* The PwDE permits {selection: the PwDE, local users, remote users} to initiate communication via the trusted path.
* The PwDE requires the use of the trusted path for {selection: initial user authentication or {other services}}.
* The PwDE shall perform the Trusted Path in accordance with a specified [cryptographic algorithm](../definitions.md#cryptographic-algorithm) {Choose Cryptographic algorithm} and cryptographic key sizes {Choose key sizes} that meet the CRA Regulation (REGULATION (EU) 2024/2847).

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(e)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### 👉❗ Cryptographic algorithms
The European Commission has not defined any accepted cryptographic algorithms to be used. As a general reference for EUCC, the [Agreed Cryptographic Mechanisms](https://certification.enisa.europa.eu/certification-library/eucc-certification-scheme_en#guidelines-for-eucc) are used. Further guidelines on this are expected to be provided by the European Commission.

### 👉❗ Due Diligence
When integrating third-party components, including free and open-source software not yet on the market, manufacturers must exercise due diligence to ensure compliance with the Regulation’s essential cybersecurity requirements. The level of due diligence should match the component’s cybersecurity risk and may include:

* **Conformity check:** Verify that the component’s manufacturer demonstrates compliance with the Regulation, e.g., CE marking.  
* **Security updates:** Ensure the component receives regular security updates.  
* **Vulnerability check:** Verify the component is free from known vulnerabilities in the European vulnerability database or other public sources.  
* **Additional testing:** Perform extra security testing if necessary.  

Further guidance regarding this concept is expected by the European Commission.

### EUVD 
European Vulnerability Database (EUVD) established pursuant to Article 12(2) of Directive (EU) 2022/2555. The European Vulnerability Database will assist manufacturers in detecting known exploitable vulnerabilities in their products, in order to ensure that secure products are made available on the market.

### Identification mechanism Requirement
The Requirement of the Annex I Part I (2)(d) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *ensure protection from unauthorised access by appropriate control mechanisms, including but not limited to authentication, identity or access management systems, and report on possible unauthorised access;*

The Identity requirement needs to be covered by Security Functions. As an example from CC2022R1:

* **End User identification:**
  * (optional) The PwDE allows {list of actions} on behalf of the user to be performed before the end user is identified.
  * The PwDE requires each end user to be successfully identified before allowing any security actions on behalf of that end user.

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(d)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### Intended purpose
Means the use for which a product with digital elements is intended by the manufacturer, including the specific context and conditions of use, as specified in the information supplied by the manufacturer in the instructions for use, promotional or sales materials, statements, and technical documentation.

### Integrity of Data Requirement
The Requirement of the Annex I Part I (2)(f) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *protect the integrity of stored, transmitted or otherwise processed data, personal or other, commands, programs and configuration against any manipulation or modification not authorised by the user, and report on corruptions;*

This requirement needs to be covered by Security Functions. As an example using CC2022R1:

* **Stored data integrity monitoring and action**
  * The PwDE monitors user data stored in containers controlled by the PwDE for integrity errors on all objects, based on the following attributes: {Choose attributes}.
  * Upon detection of a data integrity error, the PwDE {describe the action}.

* **Inter-PwDE trusted channels**
  * The PwDE provides a communication channel between itself and another trusted IT product that is logically distinct from other communication channels and provides assured identification of its endpoints and protection of the channel data from modification or disclosure.
  * The PwDE permits {Indicate end points} to initiate communication via the trusted channel.
  * The PwDE initiates communication via the trusted channel for {list of functions for which a trusted channel is required}.

* **Trusted path**
  * The PwDE provides a communication path between itself and {selection: remote or local} users that is logically distinct from other communication paths and provides assured identification of its endpoints and protection of the communicated data from {selection: modification, disclosure, or {Other types}}.
  * The PwDE permits {selection: the PwDE, local users, remote users} to initiate communication via the trusted path.
  * The PwDE requires the use of the trusted path for {selection: initial user authentication or {other services}}.
  * The PwDE shall perform the Trusted Path in accordance with a specified [cryptographic algorithm](../definitions.md#cryptographic-algorithm) {Choose Cryptographic algorithm} and cryptographic key sizes {Choose key sizes} that meet the CRA Regulation (REGULATION (EU) 2024/2847).

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(f)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. from the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### 👉❗ Known exploitable vulnerability
This concept requires further definition/guidance by the European Commission. For example, in which cases can a vulnerability be considered too complex? In Common Criteria, there is the concept of attack potential, by which product vulnerabilities can be classified as Residual Vulnerabilities. This concept could fit into the "CRA concept" of "Risk-based analysis," but further clarifications are required.

### Minimise Impact Requirement
The Requirement of the Annex I Part I (2)(i) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *minimise the negative impact by the products themselves or connected devices on the availability of services provided by other devices or networks;*

This requirement needs to be covered by Security Functions. As an example using CC2022R1:

* **PwDE initialization**
  * The PwDE provides an initialization function that is self-protected for integrity and authenticity.
  * The PwDE initialization function ensures that certain properties hold on certain elements immediately before establishing the TSF in a secure initial state, as specified in {describe}.
  * The PwDE initialization function detects and responds to errors and failures during initialization such that the PwDE {selection: is halted, successfully completes initialization} with {selection: reduced functionality, signaling error state, {List of actions}}.
  * The PwDE initialization function only interacts with the PwDE in {list defined methods} during initialization.

* **PwDE self-testing**
  * The PwDE runs a suite of the following self-tests {selection: during initial start-up, periodically during normal operation, at the request of the authorized user, under the conditions {List conditions under which self-test should occur}} to demonstrate the correct operation of {selection: {List parts of PwDE}, the PwDE}: {List of self-tests run by the PwDE}.
  * The PwDE provides authorized users with the capability to verify the integrity of {selection: {List parts of PwDE data}, PwDE data} and {selection: {assignment: parts of PwDE}, PwDE}.

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(i)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. from the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### Mitigation mechanism requirement
The Requirement of the Annex I Part I (2)(k) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *be designed, developed and produced to reduce the impact of an incident using appropriate exploitation mitigation mechanisms and techniques;*

This requirement needs to be covered by Security Functions. As an example using CC2022R1:

* **Failure with preservation of secure state**
  * The PwDE preserves a secure state when the following types of failures occur: {List the types of failures}.
* **Manual recovery**
  * After {list of failures/service discontinuities}, the PwDE enters a maintenance mode where the ability to return to a secure state is provided.

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(k)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. from the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### non-Applicability of an ESR
The reason for the non-applicability of an ESR COULD be that an ESR is incompatible with the nature of a PwDE. If certain ESRs are not applicable, but the manufacturer has identified cybersecurity risks, it SHOULD take measures to address those risks by other means.

### non-Security Function subsystem
Modified concept from Common Criteria "SFR-non-interfering." It is a subsystem that does not play any role in enforcing or supporting a Security Function.

### 👉❗ Product Type
Common Criteria 2022R1 does not clearly describe product typologies. Currently, the CRA Regulation neither defines a classification of product types in the Default products category. Further decisions are expected to clarify whether risk assessments will be based on product types (or vertical standards), similarly as per Important and Critical Products.

### Reasonably foreseeable use
Means use that is not necessarily the intended purpose supplied by the manufacturer in the instructions for use, promotional or sales materials and statements, or in the technical documentation, but which is likely to result from reasonably foreseeable human behavior or technical operations or interactions.

### Reasonably foreseeable misuse
Means the use of a product with digital elements in a way that is not in accordance with its intended purpose, but which may result from reasonably foreseeable human behavior or interaction with other systems.

### Recording and Monitoring requirement
The Requirement of the Annex I Part I (2)(l) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *provide security related information by recording and monitoring relevant internal activity, including the access to or modification of data, services or functions, with an opt-out mechanism for the user;*

This requirement needs to be covered by Security Functions. As an example using CC2022R1:

* **Audit data generation**
  * The PwDE generates audit data of the following auditable events:
    * Start-up and shutdown of the audit functions;
    * All auditable events for the {if applicable, choose level} level of audit;
    * {Other auditable events}
  * The PwDE records within the audit data at least the following information:
    * Date and time of the auditable event, type of event, subject identity (if applicable), and the outcome (success or failure) of the event;
    * For each auditable event type, based on the auditable event definitions of the functional components included in {...}.

* **Specification of Management Functions**
  * The TSF shall be capable of performing the following management functions:
    * Enable and disable the audit data generation function.
    * Configure which events shall be audited (subject to FAU_GEN.1).
    * Manage user roles and privileges.
    * Manage TSF configuration parameters related to security.
    * Initialize and reset security-relevant parameters.

* **Security roles**
  * The PwDE maintains the roles {List the authorized identified roles}.
  * The PwDE is able to associate end users with roles.

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(l)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. from the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### Removal of Data requirement
The Requirement of the Annex I Part I (2)(m) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *provide the possibility for users to securely and easily remove on a permanent basis all data and settings and, where such data can be transferred to other products or systems, ensure that this is done in a secure manner.*

This requirement needs to be covered by Security Functions. As an example for the Removal of Data (the transfer of data to another system is not described) requirement using CC2022R1:

* **Specification of Management Functions**
  * The PwDE is capable of performing the following management functions:
    * Securely and permanently remove all user data and settings.
    * Restore the system to its factory state.

* **Subset residual information protection**
  * The PwDE ensures that any previous information content of a resource is made unavailable upon the {selection: allocation of the resource to, deallocation of the resource from} the following objects: {list of objects}.

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(m)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. from the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### Reporting unauthorized access Requirement
The Requirement of the Annex I Part I (2)(d) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *ensure protection from unauthorised access by appropriate control mechanisms, including but not limited to authentication, identity or access management systems, and report on possible unauthorised access;*

The Reporting unauthorized access Requirement needs to be covered by Security Functions. As an example from CC2022R1:

* **Audit data generation**
  * The PwDE generates audit data of the following auditable events:
    * Start-up and shutdown of the audit functions;
    * All auditable events for the {if applicable, choose level} level of audit;
    * {Other auditable events}
  * The PwDE records at least the following information within the audit data:
    * Date and time of the auditable event, type of event, subject identity (if applicable), and the outcome (success or failure) of the event;
    * For each auditable event type, based on the auditable event definitions of the functional components included in {...}.

* **Potential violation analysis**
  * The PwDE applies a set of rules when monitoring the audited events and, based on these rules, indicates a potential violation of the enforcement of the SFRs.
  * The TSF enforces the following rules for monitoring audited events:
    * Accumulation or combination of {Choose auditable events} known to indicate a potential security violation;
    * {Other rules}

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(d)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. from the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### Reset to its original state Requirement
The Requirement of the Annex I Part I (2)(b) of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requires:
* *be made available on the market with a secure by default configuration, unless otherwise agreed between manufacturer and business user in relation to a tailor-made product with digital elements, including the possibility to reset the product to its original state;*

This requirement is partially covered by [ADV_ARC.2](../methodology.md#-security-architecture-adv_arc2). However, the requirement:
* *including the possibility to reset the product to its original state*

needs to be covered by a Security Function of the PwDE. An example from CC2022R1:

* **Specification of Management Functions**
  * The PwDE is capable of performing the following management functions:
    * Reset the PwDE to its original factory configuration.
    * Remove all user data.
    * Restore all default security settings.

This Security Function can be skipped if:
1. An agreement as mentioned in the ESR is provided with the technical documentation.
2. The SPD in the ST identifies other measures in the operational environment that compensate for the need for a secure default configuration, such as declaring an assumption for trusted administrators to ensure they perform a secure initial configuration following the AGD_PRE.1 guidance.

Further information on the coverage of this requirement using CC2022R1 can be found in section "ESR (2)(b)" of the [CRA by EUCC Annex](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en). Furthermore, other Security Functions described in other standards e.g. from the future standards delevoped as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) could be used.

### SBOM
Stands for Software Bill Of Materials. It is not defined in the CRA Regulation nor in the Blue Guidance. From [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng):
* *An SBOM can provide manufacturers, purchasers, and operators of software with information that enhances their understanding of the supply chain, with multiple benefits. In particular, it helps track known newly emerged vulnerabilities and cybersecurity risks.*

From [TR-03183](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html):
* *A “Software Bill of Materials” (SBOM) is a machine-processable file containing supply chain relationships and details of the components used in a software product. It supports automated processing of information on these components, covering both “primary components” and used (e.g., external/third-party) components.*

As an example, a manufacturer could check the format proposed in [BSI TR-03183-2](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html).

### 👉❗ Secure decommissioning
I did not find any formal definition of Secure Decommissioning in the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng). Further definitions might be provided.

### Security Function
Modified concept from Common Criteria "Security Functional Requirement (SFR)". This is a security mechanism (no clear equivalent in [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng)) that counters a threat.  

In Common Criteria, there is high formality related to SFRs; in this methodology, it has been reduced to the bare minimum. Manufacturers can define their own Security Functions, although it is recommended to use existing defined concepts to facilitate analysis. Recommended sources instead of proprietary security functions include:
* Common Criteria 2022 R1
* SESIP (EN17927)
* EN18031
* CEN/CENELEC standards referenced in the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) Requests 2 to 14
* Other standards relevant to the threats and security measures of that PwDE.

### Security Function enforcing subsystem
Modified concept from Common Criteria "SFR-Enforcing subsystem". It is a subsystem responsible for enforcing a Security Function, also called "SF-enforcing." SF-enforcing behavior refers to how a subsystem provides the functionality that implements a Security Function of [ASE_REQ.1].

### Security Function supporting subsystem
Modified concept from Common Criteria "SFR-Supporting subsystem." It is a subsystem relied upon by a Security Function enforcing subsystem to implement a Security Function. Also called "SF-supporting."

### 👉❗ Security by Default configuration
This term is used in CRA, e.g., in Annex I Part I (2)(b), but is never formally defined. In general, it should mean a configuration in which the security of the PwDE or its assets is guaranteed. A default configuration is also the state in which the PwDE is delivered to the user prior to execution of instructions in [[AGD_PRE.1]](../methodology.md#-installation-guidance-agd_pre1).

### 👉❗ Security Impact and probability
This term is retrieved from TR-03183, specifically from requirement "REQ_RA 1.1". There is no definition in CRA or TR-03183. Further guidance is expected.

### Single Point of Contact
Manufacturers shall designate a single point of contact to enable users to communicate directly and rapidly, including facilitating vulnerability reporting.  

The single point of contact should be easily accessible, clearly indicate its availability, and be kept up to date. Automated tools (e.g., chat boxes) may be offered, but a phone number or other digital contact method (email, contact form) must also be provided. It should not rely exclusively on automated tools.  

The single point of contact MUST allow users to choose their preferred communication method.

### 👉❗ State of the art
This concept is used in both CC2022R1 and CRA Regulation. But this concept needs further clarifications from the European Commission since it might differentiate between what is a vulnerability and what is not.

### Support Period
The support period refers to the timeframe during which a manufacturer must ensure that vulnerabilities of a product with digital elements (PwDE) are addressed effectively and in accordance with the essential cybersecurity requirements in Part II of Annex I. The support period must be no less than five years, unless the expected lifetime of the PwDE is shorter, in which case vulnerability handling must cover the full lifetime. Where the expected use exceeds five years (e.g., hardware components, network devices, or software like OS or video-editing tools), manufacturers should provide a correspondingly longer support period.  

Manufacturers are responsible for determining a support period reflecting expected product use, considering reasonable user expectations, product nature, intended purpose, and relevant Union legislation. Factors such as support periods of similar products, operating environment, third-party component support, and guidance from the ADCO group may be applied proportionally.

The support period MUST include at least the month and year, be clearly specified at purchase, and, where applicable, be present on the product’s packaging or digitally. If feasible, the product MUST display a notification indicating the end of its support period.  

If the expected lifetime is less than five years, the support period **could** cover the full lifetime. This choice **should** be justified based on the PwDE’s nature.  

### Vulnerability Databases
CRA Regulation references the European vulnerability database (EUVD):
* *European vulnerability database established pursuant to Article 12(2) of Directive (EU) 2022/2555. The European vulnerability database will assist manufacturers in detecting known exploitable vulnerabilities in their products, in order to ensure that secure products are made available on the market.*

In general, searches across different "Common/European/National Vulnerability Databases (CVD/EUVD/NVD)" may be required:
* *(...) verifying that a component is free from vulnerabilities registered in the European vulnerability database established pursuant to Article 12(2) of Directive (EU) 2022/2555 or other publicly accessible vulnerability databases*. 

## From TR-03183 Technical Specification
### Machine-processable
SBOMs are defined as machine-processable files in this Technical Guideline. This implies machines can create, read, modify, process, analyze, and evaluate content, and act based on the data. The content itself is well-defined and structured. The term “machine-readable” is avoided due to multiple interpretations.




