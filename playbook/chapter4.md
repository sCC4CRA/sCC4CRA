# Chapter 4 - Life Cycle

## 🧩 SBOM (ALC_CMS.2 & ALC_SBM.1)
### SBM-1 - Include the PwDE itself and the components that comprises the PwDE, each part uniquely identified.
1. MUST identify and document components (hardware and software) contained in the PwDE.
1. Each component that comprises the PwDE MUST be [uniquely identified](../definitions.md#unique-identification).
1. For software components MUST include an [SBOM](../definitions.md#sbom).
1. The [SBOM](../definitions.md#sbom) MUST contain at least the top-level third-party software components used by the PwDE.
1. MUST contain sufficient information to [uniquely identify](../definitions.md#unique-identification) which version of each component has been used.
1. MUST identify and document the documentation required for the secure use of the PwDE.
1. Each document required for the secure use of the PwDE MUST be [uniquely identified](../definitions.md#unique-identification).
1. MUST be coherent with [[ASE_INT.1]](../methodology.md#-introduction-and-description-ase_int1).
### SBM-2 - For each hardware component that comprises the PwDE, shall indicate the developer of the item.
1. MUST indicate the developer for each hardware component.

⚠️ If only one developer is involved in the development of the hardware components, this requirement DOES NOT apply.

### SBM-3 - For each item of the SBOM, shall indicate the developer of the item in specific format
1. The [SBOM](../definitions.md#sbom) MUST contain at least the top-level third-party software components.
1. For each software component, it MUST include the developer’s URI, SPDX-ID structure license and hash value.
1. MUST be provided in [machine readable](../definitions.md#machine-processable) format.
1. MAY be provided in CycloneDX6 in version 1.4 or higher.
1. MAY be provided in Software Package Data eXchange (SPDX) in version 2.3 or higher.

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
