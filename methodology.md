# Methodology

## Chapter 1 - Manufacturer risk assessment

### 📘 Introduction and Description (ASE_INT.1)
* **IAD-1** - The Technical Documentation introduction shall have a unique name and version.
* **IAD-2** - The Technical Documentation introduction shall include the manufacturer's information.
* **IAD-3** - The Technical Documentation introduction shall include CRA compliance statements.
* **IAD-4** - The Technical Documentation introduction shall uniquely identify the PwDE.
* **IAD-5** - The PwDE description shall identify the product type.
* **IAD-6** - The PwDE description shall summarize its usage.
* **IAD-7** - The PwDE description shall describe the physical description of the PwDE.
* **IAD-8** - The PwDE description shall describe the logical description of the PwDE.

### 🛡️ Risk Assessment Analysis (ASE_SPD.1)
* **SPD-1** - Describe all threats in terms of a threat agent, an asset and an adverse action.
* **SPD-2** - Describe the Security Policies.
* **SPD-3** - Describe the assumptions about the operational environment of the PwDE.

### 🎯 Security Objectives (ASE_OBJ.1)
* **OBJ-1** - Describe the security objectives for the operational environment.
* **OBJ-2** - Trace each security objective for the operational environment to the threat it addresses.
* **OBJ-3** - Trace each security objective for the operational environment to the Security Policies which it enforces.
* **OBJ-4** - Trace each security objective for the operational environment to the assumptions it supports.
* **OBJ-5** - Demonstrate that the security objectives for the operational environment uphold all assumptions.

### 🔐 Security Functionalities (ASE_REQ.1 & ASE_TSS.1)
* **REQ-1** - Describe the security controls of the PwDE.
* **REQ.COMP-1** - Identify, for each third-party component, the security controls that are relevant for your PwDE.
* **REQ-2** - For each threat, the security controls must demonstrate that they are suitable to meet that threat.
* **REQ-3** - The security controls must demonstrate that they are suitable to enforce each Security Policy.
* **REQ-4** - Shall be internally consistent.


For more details see the Playbook of [Chapter 1 - Manufacturer risk assessment](playbook/chapter1.md).

## Chapter 2 - Guidance

### 🔧 Operational Guidance (AGD_OPE.1)
* **OPE-1** - Describe, for each end user, the security controls that should be controlled.
* **OPE-2** - Describe, for each interface, the privileges that should be controlled.
* **OPE-3** - Describe, for each end user, how to use the available interfaces provided in a secure manner.
* **OPE-4** - Describe, for each end user, the available interfaces.
* **OPE-5** - For each end user, clearly present each security actions they can perform.
* **OPE-6** - Identify all possible modes of operation of the PwDE.
* **OPE-7** - For each user, describe the security measures needed to meet the operational security objectives.

### 🧹 Decommissioning (AGD_DEC.1)
* **DEC-1** - Describe all the steps necessary for secure decommissioning upon end-of-life.
* **DEC-2** - Describe all the necessary equipment that is required to perform PwDE decommissioning.
* **DEC-3** - Decommissioning must prevent access to PwDE-protected assets after it is retired.
* **DEC-4** - The decommissioning procedures shall be compatible with the operational environment.

### 📦 Installation Guidance (AGD_PRE.1)
* **INS-1** - Shall describe all the steps necessary for secure acceptance of the delivered PwDE.
* **INS-2** - Shall describe all the steps necessary for secure installation of the PwDE.
* **INS-3** - Shall describe the secure preparation of the operational environment.

For more details see the Playbook of [Chapter 2 - Guidance](playbook/chapter2.md).

## Chapter 3 - Development
### 🔀 Interfaces (ADV_FSP.2)
* **INT-1** - The described interfaces must be coherent with the PwDE design.
* **INT-2** - Describe the purpose, method of use and all parameters associated with each interface.
* **INT-3** - Describe the security actions and error messages of the Interfaces.
* **INT-4** - Add a tracing between the security controls with the corresponding Interfaces.

### 🏰 Security Architecture (ADV_ARC.2)
* **ARC-1** - Describe the limitation of the attack surface provided by the PwDE.
* **ARC-2** - Describe how the PwDE initialisation process is secure.
* **ARC-3** - Demonstrate that the PwDE protects itself from tampering.
* **ARC-4** - Demonstrate that the PwDE prevents bypass of the security controls.
* **ARC-5** - Demonstrate that the PwDE enforces a secure default configuration when it is delivered.
* **ARC.COMP-1** - Demonstrate, for each third-party component, how the PwDE fulfills its requirements. 

### 🗂️ PwDE Design (ADV_TDS.2)
* **TDS-1** - Describe the structure of the PwDE in terms of subsystems.
* **TDS-2** - Describe the security controls' behaviour of the subsystems.
* **TDS-3** - Provide a description of the interactions among all subsystems of the PwDE.
* **TDS-4** - Demonstrate that all interfaces trace to the behaviour described in the PwDE design that they invoke.
* **TDS-5** - Demonstrate that all security controls trace to the behaviour described in the PwDE design.

### 🧾 Data Minimisation (ADV_PDM.1)
* **PDM-1** - Identify all data processed by the PwDE.
* **PDM-2** - Relate each data processed by the PwDE with the input interfaces from which it is received.
* **PDM-3** - Relate each data processed by the PwDE with the outbound interfaces where it is outputted.
* **PDM-4** - Demonstrate that all data handled by the PwDE is needed and appropriate for its purpose.

For more details see the Playbook of [Chapter 3 - Development](playbook/chapter3.md).

## Chapter 4 - Life Cycle

### 🧩 BOM (ALC_CMS.2 & ALC_SBM.1)
* **BOM-1** - Include the PwDE itself and the components that comprises the PwDE, each part uniquely identified.
* **BOM-2** - For each hardware component that comprises the PwDE, shall indicate the developer of the item.
* **BOM-3** - For each item of the SBOM, shall indicate the developer of the item in a specific format.
* **BOM.COMP-1** - For each component, shall be installed the correct version and with the Security by Default configuration.

### 🔄 Life Cycle (ALC_LCD.1)
* **LCD-1** - Describe the processes used to develop and maintain the PwDE.
* **LCD-2** - Provide for the necessary control over the development and maintenance of the PwDE.

For more details see the Playbook of [Chapter 4 - Life Cycle](playbook/chapter4.md).

## Chapter 5 - Testing
### 📋 Functional (ATE_FUN.1)
* **FUN-1** - The test documentation shall consist of test plans, expected test results and actual test results.
* **FUN-2** - The test plans shall identify the tests to be performed and describe the scenarios under which each test is performed.
* **FUN-3** - The expected test results shall show the anticipated outputs from a successful execution of the tests.
* **FUN-4** - The actual test results shall be consistent with the expected test results.

### 🔍 Depth (ATE_DPT.1)
* **DPT-1** - Shall demonstrate the correspondence between the tests and the PwDE subsystems.
* **DPT-2** - The analysis of the depth of testing shall demonstrate that all PwDE subsystems have been tested.

For more details see the Playbook of [Chapter 5 - Testing](playbook/chapter5.md).

## Chapter 6 - Vulnerability Analysis

### 🕵️‍♀️ Vulnerability Analysis (AVA_VAN.5)
* **VAN-1** - Search public sources for potential vulnerabilities in the PwDE.
* **VAN-2** - Search public sources for potential vulnerabilities in the third-party components.
* **VAN-3** - Perform an independent vulnerability analysis using the Technical Documentation and the code.
* **VAN-4** - Devise penetration testing based on the identified potential vulnerabilities.
* **VAN-5** - Conduct penetration testing based on the identified potential vulnerabilities.
* **VAN-6** - Conclude that the product is placed on the market without known exploitable vulnerabilities.

For more details see the Playbook of [Chapter 6 - Vulnerability Analysis](playbook/chapter6.md).
