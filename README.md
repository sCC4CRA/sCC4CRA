# Simplified Common Criteria for CRA

## 📘 Introduction
Cyber Resilience Act (CRA) REGULATION (EU) 2024/2847 was [published](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) by the European Commission on the 23rd of October of 2024. This regulation requires the Products with Digital Elements (PwDE) to comply with certain requirements when they are *"made available on the market"*. 

The PwDEs are differentiated by the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) into three different categories:
* Default
* Important (Class I and Class II)
* Critical

For the Default products, a Module A (self-assessment) procedure will be allowed. This methodology aims to provide a step-by-step, intuitive and straightforward compliance guidance for these products.

It has been developed by [Roger Riera](https://es.linkedin.com/in/rogerriera28) compiling and simplifying the best features of the following sources:
* [Cyber Resilience Act Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng)
* [Cyber Resilience Act implementation by EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en)
* [Common Criteria CC:2022 Release 1](https://www.commoncriteriaportal.org/cc/index.cfm)
* [Technical Guideline TR-03183](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html)
## 🛠️ Methodology

This sCC4CRA methodology describes step by step how to fulfill the Technical Documentation to cover most of the technical requirements of the [Cyber Resilience Act Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng). It is divided into six chapters providing both a high-level overview and step-by-step playbook:
* [High-level methodology](methodology.md)
* [Step by Step Playbook](playbook/chapter1.md)

The methodology, based in [CC2022R1](https://www.commoncriteriaportal.org/cc/index.cfm), has been modified according to this [rationale](rationale.md) and adapted to [Cyber Resilience Act Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) language and requirements. 

Furthermore, most of the formality of the [CC2022R1](https://www.commoncriteriaportal.org/cc/index.cfm) has been reduced to the bare minimum.

## 📜 CRA Compliance

The [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) describes many obligations to be fulfilled by the Products with Digital Elements (PwDEs) and the stakeholders managing them (e.g. the Manufacturers). 

This methodology is intended to facilitate the Manufacturer obligations [(Article 13)](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#art_13) for Default Products, in order to allow that their products fulfill the requirements for PwDEs as indicated in [(Article 6)](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#art_6) and to develop the Technical Documentation as set out in [(Article 31)](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#art_31).

To verify the applicability of this methodology, should be checked that your product does NOT fall under the product descriptions set out in [Annex III](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_III) or in [Annex IV](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_IV).

The following table shows the actual coverage of the [CRA Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) requirement of this methodology:

| Annex |  Coverage      |  Comments    |
|---------|------------|-----------------|
|Annex I Part I| 🟡✅ |All requirements are covered except for: <br> * Risk assesment <br> * Vulnerability Handling <br> See [rationale](rationale.md#annex-i-part-i)|
|Annex I Part II|❌|The Vulnerability Handling are not covered, see [rationale](rationale.md#annex-i-part-ii)|
|Annex II|✅|All requirements covered ✅ by [[ASE_INT.1]](methodology.md#-introduction-and-description-ase_int1)|
|Annex VII|🟡✅ |All requirements are covered except for the Security Updates. See [rationale](rationale.md#annex-vii)|

## 🚀 Next steps: 
This methodology will be updated based on the continuous work carried out by the European Comission previously to the application of the regulation on September 2027. The following tasks are identified:

* **Alignment with standardization:** Align the methodology with the upcoming horizontal standard developed by CEN/CENELEC as per the [Commission's Implementing Decision](https://ec.europa.eu/transparency/documents-register/detail?ref=C(2025)618&lang=en) Requests 1 to 15. They are being developed by the CEN-CLC/JTC 13 WG 9. Specifically the two important GAPs that need to be updated by the standardization groups are the standards related to the:
  * Risk assessment ([Annex I Part I (1)](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_I))
  * Vulnerability Handling and Secure Updates ([Annex I Part II](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202402847#anx_I))
* **Continuously simplify the methodology:** The main idea of this methodology is to keep it simple. Although simplified, it can still be made more intuitive. 
* **Composition:** Add composition classes named as *_COMP in [Common Criteria CC:2022 Release 1](https://www.commoncriteriaportal.org/cc/index.cfm) to allow benefiting from Common Criteria Composition rules. The idea is to make composition available either with CC, SESIP (EN17297) (or others) Certified CRA components.
* **Guides for Composition/Integration:** In general this methodology does not include guides for composition or integration (aka. ETRfC). These might be added in the future by reusing guidance of SOG-IS/ENISA for EUCC products. The [Cyber Resilience Act implementation by EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en) provides also some guidance for it.
* **Remote Data Processing:** Currently Remote Data processing is left Out of the scope of the methodology. It has been considered to follow a strategy as recomended in section "7.4. Remote data processing solutions" of the [Cyber Resilience Act implementation by EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en); however, I preferred to wait for some further guidance by the European Commision.

## ⚠️ Disclaimer

This methodology has been written solely for the purpose of facilitating the [CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) compliance for Default products. It does not give any presumption of conformity and MUST NOT be considered a legal text to ensure [CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) compliance.

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “NOT RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in [RFC 2119](https://www.rfc-editor.org/rfc/rfc2119).

## 📜 Version Control

| Version |  Date      |  Description    |
|---------|------------|-----------------|
| 1.0     | 11/09/2025 | First version considering the following sources:<br>* [Cyber Resilience Act Regulation](https://eur-lex.europa.eu/eli/reg/2024/2847/oj/eng) <br> * [Cyber Resilience Act implementation by EUCC](https://certification.enisa.europa.eu/publications/cyber-resilience-act-implementation-eucc-and-its-applicable-technical-elements_en) <br> * [Common Criteria CC:2022 Release 1](https://www.commoncriteriaportal.org/cc/index.cfm) <br> * [Technical Guideline TR-03183](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html)
