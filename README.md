# Simplified Common Criteria for CRA

## 📘 Introduction
Cyber Resilience Act (CRA) REGULATION (EU) 2024/2847 was [published](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) by the European Commission on the 23rd of October of 2024. This regulation requires the Products with Digital Elements (PwDE) to comply with certain requirements when they are *"made available on the market"*. 

The PwDEs are differentiated by the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) into three different categories:
* Default
* Important (Class I and Class II)
* Critical

For the Default products, a Module A (self-assessment) procedure will be allowed. This methodology aims to provide a step-by-step, intuitive and straightforward compliance guidance for these products.

## 🛠️ Methodology

This sCC4CRA methodology is divided into six chapters providing both a high-level overview and step-by-step playbook:
* [High-level methodology](methodology.md)
* [Step-by-Step Playbook](playbook/chapter1.md)

The methodology, based in [CC2022R1](https://www.commoncriteriaportal.org/cc/index.cfm), has been modified according to this [rationale](rationale.md) and adapted to [Cyber Resilience Act Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) language and requirements. 

Furthermore, most of the formality of the [CC2022R1](https://www.commoncriteriaportal.org/cc/index.cfm) has been reduced to the bare minimum.

## 📜 CRA Compliance
Before applying this methodology, check that your product is **not** included in [Annex III](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_III) or [Annex IV](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_IV). The table below shows how this methodology maps to CRA requirements:

| Annex |  Coverage      |  Comments    |
|---------|------------|-----------------|
|Annex I Part I| 🟡✅ |All requirements are covered except for: <br> * Risk assesment <br> * Vulnerability Handling <br> See [rationale](rationale.md#annex-i-part-i)|
|Annex I Part II|❌|The Vulnerability Handling are not covered, see [rationale](rationale.md#annex-i-part-ii)|
|Annex II|✅|All requirements covered ✅ by [[ASE_INT.1]](methodology.md#-introduction-and-description-ase_int1)|
|Annex VII|🟡✅ |All requirements are covered except for the Security Updates. See [rationale](rationale.md#annex-vii)|

## 🚀 Next steps: 
This methodology will be updated based on the ongoing work carried out by the European Commission prior to the application of the regulation in September 2027. The following tasks are identified:

* **Continuous alignment with standardization work**  
* **Ongoing simplification of the methodology**  
* **Addition of composition families**  
* **Development of guides for composition and integration**  
* **Inclusion of remote data processing**  
* **Education, training, and dissemination of the methodology**

## ⚠️ Disclaimer

This methodology has been written solely for the purpose of facilitating the [CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) compliance for Default products. It does not give any presumption of conformity and MUST NOT be considered a legal text to ensure [CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) compliance.

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “NOT RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in [RFC 2119](https://www.rfc-editor.org/rfc/rfc2119).

## 📜 Version Control

| Version | Date | Description |
|----------|------|--------------|
| 1.1 | 11/10/2025 | Updated with the following changes:<ul><li>Minor changes to simplify and ease the readiness</li><li>Integrated to the harmonized standard being developed by CEN/CLC JTC 13 PT.2; using as a reference the webinar <a href="https://www.cencenelec.eu/news-events/events/2025/2025-09-08-preparation-for-the-une-event/">"Unlocking CRA Security Controls"</a>.</li></ul> |
| 1.0 | 11/09/2025 | First version considering the following sources:<ul><li><a href="https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng">Cyber Resilience Act Regulation</a></li><li><a href="https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en">Cyber Resilience Act implementation by EUCC</a></li><li><a href="https://www.commoncriteriaportal.org/cc/index.cfm">Common Criteria CC:2022 Release 1</a></li><li><a href="https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html">Technical Guideline TR-03183</a></li></ul> |


