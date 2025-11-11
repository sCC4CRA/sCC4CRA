# Chapter 3 - Development
## 🔀 Interfaces (ADV_FSP.2)
### INT-1 - The described interfaces must be coherent with the PwDE design.
1. The interfaces identification CAN be described at a higher or lower level, but MUST be complete.
1. All portions of the PwDE as described in [[ADV_TDS.2]](../methodology.md#%EF%B8%8F-pwde-design-adv_tds2) SHOULD have a corresponding interface description.
1. If a portion of the PwDE as described in [[ADV_TDS.2]](../methodology.md#%EF%B8%8F-pwde-design-adv_tds2) does not have a corresponding interface, it MUST be duly justified.
### INT-2 - Describe the purpose, method of use and all parameters associated with each interface.
1. MUST describe the [purpose](../definitions.md#purpose) of each interface.
1. MUST describe the [method of use](../definitions.md#method-of-use) of each interface.
1. MUST describe the [parameters](../definitions.md#parameter) of each interface.
### INT-3 - Describe the security actions and error messages of the Interfaces.
1. MUST describe the security actions triggered by the [Security Enforcing interfaces](../definitions.md#security-enforcing-interfaces).
1. MUST describe the errors that occur through the invocation of the [Security Enforcing interfaces](../definitions.md#security-enforcing-interfaces).
1. The security action and the error messages MUST be coherent with the [[ASE_REQ.1]](../methodology.md#-security-functionalities-ase_req1--ase_tss1), [[ADV_TDS.2]](../methodology.md#%EF%B8%8F-pwde-design-adv_tds2) and [[AGD_OPE.1]](../methodology.md#-operational-guidance-agd_ope1).
### INT-4 - Add a tracing between the Security Functions with the corresponding Interfaces.
1. The tracing MUST serve as a guide to which [Security Functions](definitions.md#security-function) are related to [Security Enforcing interfaces](../definitions.md#security-enforcing-interfaces).
1. The Security Functions described MUST be coherent with [[ASE_REQ.1]](../methodology.md#-security-functionalities-ase_req1--ase_tss1).
## 🏰 Security Architecture (ADV_ARC.2)
### ARC-1 - Describe the limitation of the attack surface provided by the PwDE.
1. The PwDE MUST deactivate interfaces and services not required for usage by default.
1. The PwDE MUST deactivate debug interfaces and functions.
1. It MUST be consistent with the [[ADV_TDS.2]](../methodology.md#%EF%B8%8F-pwde-design-adv_tds2).
1. The description SHOULD take into account all of the [Security Function](definitions.md#security-function) of the [[ASE_REQ.1]](../methodology.md#-security-functionalities-ase_req1--ase_tss1).
1. The Debug interfaces of the PwDE MAY be retrospectively reactivated by an authorized user or administrator.
### ARC-2 - Describe how the PwDE initialisation process is secure.
1. MUST relate the PwDE components involved in bringing the PwDE into an initial secure state when power-on is applied.
1. MUST indicate the processing that occurs in transitioning from the "down" state to the initial secure state.
1. If initialization components are inaccessible after secure state, MUST explain why untrusted entities cannot access them
1. In this respect, these components MAY not be able to be accessed by untrusted entities after the secure state is achieved.
1. In this respect, these components MAY provide interfaces to untrusted entities, those cannot be used to tamper with the PwDE.
### ARC-3 - Demonstrate that the PwDE protects itself from tampering.
1. MUST demonstrate the [self-protection](../definitions.md#self-protection) of the PwDE against tampering.
1. The description MUST be coherent with the [[ADV_FSP.2]](../methodology.md#-interfaces-adv_fsp2) and [[ADV_TDS.2]](../methodology.md#%EF%B8%8F-pwde-design-adv_tds2).
### ARC-4 - Demonstrate that the PwDE prevents bypass of the Security Functions.
1. MUST demonstrate the [non-bypassability](../definitions.md#non-bypassability) that prevents the bypass of the security functions.
1. MUST describe how the mechanisms cannot be bypassed considering the [Security Functions](definitions.md#security-function) and the interfaces.
1. MUST be coherent with the [[ADV_TDS.2]](../methodology.md#%EF%B8%8F-pwde-design-adv_tds2) and the [[ADV_FSP.2]](../methodology.md#-interfaces-adv_fsp2).
### ARC-5 - Demonstrate that the PwDE enforces a secure default configuration when it is delivered.
1. MUST ensure that the delivered PwDE doesn’t provide any means to negatively affect the security of the PwDE.
1. MUST describe an argumentation on how the default configuration prevents undermining the PwDE security.
1. SHOULD describe in terms of protected assets and [Security Functions](definitions.md#security-function).
1. SHOULD describe the mechanism for their protection and the state of those mechanisms in the default configuration.
1. SHOULD describe the interfaces to access the asset and their state in the [Security by Default configuration](../definitions.md#-security-by-default-configuration).
1. For each of these items, SHOULD describe how their state at [Security by Default configuration](../definitions.md#-security-by-default-configuration) prevents PwDE to be vulnerated.
1. For tailor-made PwDEs, this requirement MIGHT be bypassed after an explicit agreement with the user.

### ARC.COMP-1 - Demonstrate, for each third-party component, how the PwDE fulfills its requirements. 
1. MUST demonstrate that the PwDE fulfills the requirements from the component.
1. The requirements MUST be coherent with the Security Functions covered by the component described in [[ASE_REQ.1]](../methodology.md#-security-functionalities-ase_req1--ase_tss1).
1. MUST consider the requirements 4, 5 and 8 of the [Annex II](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_II) from the component guidance.
1. SHOULD consider, where applicable, the Technical Documentation described in [Annex VII](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_VII) of the component.
1. MUST be coherent with [[ADV_FSP.2]](../methodology.md#-interfaces-adv_fsp2) and [[ADV_TDS.2]](../methodology.md#%EF%B8%8F-pwde-design-adv_tds2).
1. In case the requirement of the component is not followed, a corresponding reasoning MUST be provided.

⚠️ If the PwDE does not have [third-party components](../definitions.md#third-party-component), this requirement is NOT applicable.

## 🗂️ PwDE Design (ADV_TDS.2)
### TDS-1 - Describe the structure of the PwDE in terms of subsystems.
1. MUST describe the structure of the PwDE in terms of [subsystems](../definitions.md#subsystem).
1. The description MUST be coherent with the [[ADV_REQ.1]](../methodology.md#-security-functionalities-ase_req1--ase_tss1) and the [[AGD_OPE.1]](../methodology.md#-operational-guidance-agd_ope1).
1. Each piece of third party software described in the [[BOM]](../methodology.md#-bom-alc_cms2--alc_sbm1) MUST have its own unique subsystem.
### TDS-2 - Describe the Security Functions behaviour of the subsystems.
1. MUST classify all the subsystems in [Security Function enforcing](../definitions.md#security-function-enforcing-subsystem), [Security Function supporting](../definitions.md#security-function-supporting-subsystem) and [non-Security Function](../definitions.md#non-security-function-subsystem).
1. Non-Security Function subsystems MIGHT NOT need detailed description of their internal functioning.
1. The descriptions of SF-enforcing and SF-supporting are expected MUST be detailed.
1. The description MUST be coherent with [[ADV_ARC.2]](../methodology.md#-security-architecture-adv_arc2) and [[ADV_FSP.2]](../methodology.md#-interfaces-adv_fsp2).
### TDS-3 - Provide a description of the interactions among all subsystems of the PwDE.
1. MUST provide a description of the [interactions](../definitions.md#interactions) among all subystems.
1. MIGHT NOT need to describe the implementation details, but the shared key elements between subsystems.
1. Any control relationships between subsystems SHOULD also be described.
### TDS-4 - Demonstrate that all interfaces trace to the behaviour described in the PwDE design that they invoke.
1. The description SHOULD identify the subsystem involved when an operation is requested by an interface.
1. A complete "call tree" for each interface MIGHT NOT be needed, but some level of abstraction is acceptable.
1. All interfaces MUST be mapped to at least one subsystem.
1. This description MUST be coherent with the [[ADV_FSP.2]](../methodology.md#-interfaces-adv_fsp2).
### TDS-5 - Demonstrate that all Security Functions trace to the behaviour described in the PwDE design.
1. All Security Functions from [[ASE_REQ.1]](../methodology.md#-security-functionalities-ase_req1--ase_tss1) MUST be properly covered.
1. The description of the Security Function on [[ASE_REQ.1]](../methodology.md#-security-functionalities-ase_req1--ase_tss1) MUST be coherent with the subsystem description.

## 🧾 Data Minimisation (ADV_PDM.1)
### PDM-1 - Identify all data processed by the PwDE.
1. MUST identify all collected and processed data by the PwDE.
### PDM-2 - Relate each data processed by the PwDE with the input interfaces from which it is received. 
1. MUST provide a rationale for each data to relate with the inbound interfaces.
1. MUST be coherent with the [[AGD_OPE.1]](../methodology.md#-operational-guidance-agd_ope1) and [[ADV_FSP.2]](../methodology.md#-interfaces-adv_fsp2)
### PDM-3 - Relate each data processed by the PwDE with the outbound interfaces where it is outputted.
1. MUST provide a rationale for each data to relate with the outbound interfaces.
1. MUST be coherent with the [[AGD_OPE.1]](../methodology.md#-operational-guidance-agd_ope1) and [[ADV_FSP.2]](../methodology.md#-interfaces-adv_fsp2)
### PDM-4 - Demonstrate that all data handled by the PwDE is needed and appropriate for its purpose.
1. The PwDE MUST only collect and process data necessary for its intended purpose and reasonably foreseeable use.

****
Go to next [Chapter 4 - Life Cycle ➡️ ](chapter4.md) 
