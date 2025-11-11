# Chapter 4 - Life Cycle

## 🧩 BOM (ALC_CMS.2 & ALC_SBM.1)
### BOM-1 - Include the PwDE itself and the components that comprises the PwDE, each part uniquely identified.
1. MUST identify and document components (hardware and software) contained in the PwDE.
1. Each component that comprises the PwDE MUST be [uniquely identified](../definitions.md#unique-identification).
1. For software components MUST include an [SBOM](../definitions.md#sbom).
1. MUST contain sufficient information to [uniquely identify](../definitions.md#unique-identification) which version of each component has been used.
1. MUST identify and document the documentation required for the secure use of the PwDE.
1. Each document required for the secure use of the PwDE MUST be [uniquely identified](../definitions.md#unique-identification).
1. MUST be coherent with [[ASE_INT.1]](../methodology.md#-introduction-and-description-ase_int1).
### BOM-2 - For each hardware component that comprises the PwDE, shall indicate the developer of the item.
1. MUST indicate the developer for each hardware component.

⚠️ If only one developer is involved in the development of the hardware components, this requirement DOES NOT apply.

### BOM-3 - For each item of the SBOM, shall indicate the developer of the item in specific format
1. The [SBOM](../definitions.md#sbom) MUST contain at least the top-level third-party software components.
1. For each software component, it MUST include the developer’s URI, SPDX-ID structure license and hash value.
1. MUST be provided in [machine readable](../definitions.md#machine-processable) format.
1. MUST be provided in CycloneDX in version 1.4 or higher. -> See ⚠️ below.
1. MAY be provided in Software Package Data eXchange (SPDX) in version 2.3 or higher.

⚠️ The [TR-03183-2](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html) specifies CycloneDX v1.6 as the minimum version, whereas the [CRA via EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en) refers to CycloneDX v1.4.

⚠️ Chapter 5 of [TR-03183-2](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html) contains more requirements than the current CRA Regulation.

### BOM.COMP-1 - For each component, shall be installed the correct version and with the Security by Default configuration
1. MUST verify that the correct version of the component has been integrated in the PwDE as described in the [Guidance](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_II).
1. MUST follow the necessary measures during initial commissioning as described in the [Guidance](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_II).
1. The PwDE MUST provide a technical evidence to the End User to allow the identification of the components.
1. The technical evidence SHOULD be provided by means of its integration to the PwDE unique identification.
1. The technical evidence MAY be providing by reading out the unambiguous inscription on its surface.

## 🔄 Life Cycle (ALC_LCD.1)
### LCD-1 - Describe the processes used to develop and maintain the PwDE.
1. SHOULD include information on the life-cycle phases of the PwDE and the boundaries between the subsequent phases.
1. SHOULD include information on the procedures, tools and techniques used by the manufacturer.
1. SHOULD include the overall management structure governing the application of the procedures.
1. SHOULD include information on which parts of the TOE are delivered by subcontractors, if applicable.
### LCD-2 - Provide for the necessary control over the development and maintenance of the PwDE.
1. MUST provide the necessary control over the development and maintenance of the PwDE.
1. The life-cycle model MIGHT minimise the likelihood of security flaws.

****
Go to next [Chapter 5 - Testing ➡️ ](chapter5.md) 
