# Chapter 2 - Guidance

## 🔧 Operational Guidance (AGD_OPE.1)
### OPE-1 - Describe, for each end user, the Security Functions that should be controlled.
1. MUST identify, for each end user, the [Security Functions](../definitions.md#security-function) allowed.
1. MUST identify, for each end user, the interface.
1. MUST be coherent with [[ASE_REQ.1]](../methodology.md#-security-functionalities-ase_req1--ase_tss1) and [[ASE_OBJ.1]](../methodology.md#-security-objectives-ase_obj1).
1. MUST describe, for each end user, the interface tipology and the reason for such interface.
1. The user guidance SHOULD contain warnings regarding the use of these Security Functions.
1. Warnings SHOULD address expected effects.
1. Warnings SHOULD address possible side effects.
1. Warnings SHOULD address possible interactions with other interfaces.
### OPE-2 - Describe, for each interface, the privileges that should be controlled.
1. MUST identify, for each end user, the [Privileges](../definitions.md#privilege) allowed.
1. The configuration of the PwDE MAY allow different users different privileges for its functions.
1. Some users MIGHT be authorized to perform certain functions, while other users MAY NOT.
1. These privileges SHOULD be described, for each end user, by the user guidance.
1. The user guidance SHOULD contain warnings regarding the use of these privileges.
1. Warnings SHOULD address expected effects.
1. Warnings SHOULD address possible side effects.
1. Warnings SHOULD address possible interactions with other interfaces.
### OPE-3 - Describe, for each end user, how to use the available interfaces in a secure manner.
1. SHOULD provide advice regarding effective use of the PwDE.
### OPE-4 - Describe, for each end user, the available interfaces.
1. MUST describe all security [parameters](../definitions.md#parameter) under the control of the user.
1. SHOULD indicate secure values as appropriate.
1. SHOULD contain an overview of the Security Functions visible at the user interfaces.
1. SHOULD identify and describe the purpose, behaviour and interrelationships of the interfaces and Security functions.
1. For each interface SHOULD describe the method(s) by which the interface is invoked.
1. For each interface SHOULD describe the end user-configurable settings, their purpose, valid/secure values and insecure uses.
1. For each interface SHOULD describe the immediate response, message or code returned.
1. SHOULD be consistent with the [[ASE_INT.1]](../methodology.md#-introduction-and-description-ase_int1), [[ASE_REQ.1]](../methodology.md#-security-functionalities-ase_req1--ase_tss1), [[ADV_FSP.2]](../methodology.md#-interfaces-adv_fsp2) and [[ADV_TDS.2]](../methodology.md#%EF%B8%8F-pwde-design-adv_tds2).
### OPE-5 - For each end user, clearly present each security actions they can perform.
1. MUST include changing the security characteristics of entities under the control of the PwDE.
1. MUST describe, for each end user, the security events that may occur and the actions they may need to take.
1. SHOULD define security events may occur so the end users can keep the PwDE in the [security by default configuration](../definitions.md#-security-by-default-configuration). 
### OPE-6 - Identify all possible modes of operation of the PwDE.
1. MUST identify all modes of operation.
1. MAY include operation failures.
1. MUST include their consequences and implications for [maintaining the security](../definitions.md#maintain-security).
### OPE-7 - For each user, describe the security measures needed to meet the operational security objectives.
1. It MUST be coherent with the security objectives described in the [[ASE_OBJ.1]](../methodology.md#-security-objectives-ase_obj1).
1. For each end user, the relevant security measures MUST be described appropriately.
1. The security measures SHOULD include all relevant external procedural, physical, personnel and connectivity measures.
1. Those measures relevant for secure installation MUST be coherent with [[AGD_PRE.1]](../methodology.md#-installation-guidance-agd_pre1).

## 🧹 Decommissioning (AGD_DEC.1)
### DEC-1 - Describe all the steps necessary for secure decommissioning upon end-of-life.
1. This procedure MAY provide instructions to stop PwDE operation prior to [secure decommissioning](../definitions.md#-secure-decommissioning) procedures.
1. SHOULD provide detailed ordered steps to be executed as part of the decommissioning process.
1. SHOULD provide constraints to be met in the procedure steps. 
1. SHOULD provide considerations for human safety when physical procedures are used.
1. SHOULD provide criteria to determine if the decommissioning steps have been adequately executed.
1. It MIGHT consist in sending the PwDE to the manufacturer (or other) to ensure an appropriate destruction method.
### DEC-2 - Describe all the necessary equipment that is required to perform PwDE decommissioning.
1. The necessary equipment SHOULD include tools and auxiliary guidance.
1. Depending on the type of PwDE, it MIGHT be required to use special equipment as part of these procedures.
1. Specific guidance MAY be needed in order to use the required tools.
1. MUST be identified one by one all the required tools for executing such procedures.
1. It SHOULD be avoided to just reference generic types of equipment, for example, “a tool for secure disk deletion”.
1. The Decommission procedure must be coherent with the [[ADV_FSP.2]](../methodology.md#-interfaces-adv_fsp2) and the [[AGD_OPE.1]](../methodology.md#-operational-guidance-agd_ope1).

⚠️ If no extra equipment is needed, this does not apply.

⚠️ If decommissioning only involves sending the TOE to the manufacturer (or other), this does not apply.

### DEC-3 - Decommissioning must prevent access to PwDE-protected assets after it’s retired.
1. The decommission procedure MUST be coherent with the mechanisms described in the [[ADV_TDS.2]](../methodology.md#%EF%B8%8F-pwde-design-adv_tds2).
1. The decommission procedure deletion of assets MUST be coherent with the defined in [[ASE_SPD.1]](../methodology.md#%EF%B8%8F-risk-assessment-analysis-ase_spd1).
1. The decommission procedure MUST leave the assets effectively destroyed or rendered unusable or unrecoverable.
1. If decommissioning is just sending the TOE back, the delivery process MUST [maintain security](../definitions.md#maintain-security).
### DEC-4 - The decommissioning procedures shall be compatible with the operational environment.
1. The decommissiong procedure MUST be coherent with [[ASE_INT.1]](../methodology.md#-introduction-and-description-ase_int1) and [[ASE_OBJ.1]](../methodology.md#-security-objectives-ase_obj1).
1. The security objectives described in the [[ASE_OBJ.1]](../methodology.md#-security-objectives-ase_obj1) MAY support the decommissioning procedures.
1. The security objectives SHOULD be met while the PwDE is operational, and not during or after decommissioning.
## 📦 Installation Guidance (AGD_PRE.1)
### INS-1 - Shall describe all the steps necessary for secure acceptance of the delivered PwDE.
1. MUST include the verification of all parts of the TOE indicated in the [[ASE_INT.1]](../methodology.md#-introduction-and-description-ase_int1).
1. SHOULD reflect the steps the end user has to perform in order to accept the PwDE.
1. SHOULD provide detailed information about making sure that the delivered PwDE is the complete instance.
1. SHOULD provide detailed information about detecting modification/masquerading of the delivered PwDE.
### INS-2 - Shall describe all the steps necessary for secure installation of the PwDE. 
1. SHOULD detail the minimum system requirements for secure installation.
1. SHOULD detail the requirements for the operational environment in accordance with the security objectives provided by [[ASE_OBJ.1]](../methodology.md#-security-objectives-ase_obj1).
1. SHOULD detail the steps the user has to perform in order to get to an operational PwDE in the secure configuration.
1. MUST include; for each step, a the decision tree on the next step depended on success, failure or problems at the current step.
1. MUST include changing the installation specific security characteristics of entities under the control of the PwDE.
1. MUST describe how to handle exceptions and problems.
1. The secure installation SHOULD bring PwDE into the [security default configuration](../definitions.md#-security-by-default-configuration).
1. For tailor-made PwDEs it MIGHT NOT bring into the [security default configuration](../definitions.md#-security-by-default-configuration), it MUST also be coherent with the [[ADV_ARC.2]](../methodology.md#-security-architecture-adv_arc2).
### INS-3 - Shall describe the secure preparation of the operational environment.
1. MUST be coherent with the security objectives as described in the [[ASE_OBJ.1]](../methodology.md#-security-objectives-ase_obj1).

****

Go to next [Chapter 3 - Development ➡️ ](chapter3.md) 
