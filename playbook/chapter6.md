# Chapter 6 - Vulnerability Analysis
## 🕵️‍♀️ Vulnerability Analysis (AVA_VAN.5)
### VAN-1 - Search public sources for potential vulnerabilities in the PwDE.
1. MUST be considered all publicly available information sources.
1. MUST be considered all internal information of similar products.
1. SHOULD be focused on those sources that refer to the technologies of the PwDE.
1. The extensiveness of this search SHOULD consider the [product type](../definitions.md#-product-type).
1. The identification of one potential vulnerability can reveal other areas that MUST be investigated.
1. SHOULD be described the approach taken to identify potential vulnerabilities.

### VAN-2 - Search public sources for potential vulnerabilities in the third-party components.
1. For components with the CE marking affixed, the actively exploited vulnerabilities SHOULD be checked into the [EUVD](../definitions.md#euvd).
1. MAY use the [ALC_SBM.1](../methodology.md#-sbom-alc_cms2--alc_sbm1) to match its components against public [vulnerability databases](../definitions.md#vulnerability-databases).

### VAN-3 - Perform an independent vulnerability analysis using the Technical Documentation and the code.
1. The analysis MUST comprise the whole PwDE.
1. The analysis MUST comprise all the configurations defined in [[ASE_INT.1]](../methodology.md#-introduction-and-description-ase_int1).
1. The analysis MUST be based on the [state of the art](../definitions.md#-state-of-the-art) at the time of placing the PwDE in the market.
1. The analysis MUST include a [Due Diligence](../definitions.md#-due-diligence) of third-party products without a CE Mark.
1. Components of the [ALC_SBM.1](../methodology.md#-sbom-alc_cms2--alc_sbm1) with CE Mark MAY NOT need to be assessed.
1. SHOULD be made by a a third-party expert or an employee not related with the PwDE development.
1. SHOULD use the knowledge of the Technical Documentation and code to identify potential flaws.
1. SHOULD use the knowledge of the Technical Documentation and code to identify potential errors.

### VAN-4 - Devise penetration testing based on the identified potential vulnerabilities.
1. SHOULD prepare for penetration testing as necessary to determine the susceptibility of the PwDE.
1. MAY be useful to devise penetration tests using cases that target specific vulnerabilities.
1. Multiple potential vulnerabilities MAY be covered with the same test.
1. Test documentation MUST have sufficient detail to enable the tests to be repeatable.
1. It MAY be possible to justify and avoid testing for a potential vulnerability which is NOT a [known exploitable vulnerability](../definitions.md#-known-exploitable-vulnerability).

⚠️ If no potential vulnerabilities were identified, this requirement DOES NOT apply.
### VAN-5 - Conduct penetration testing based on the identified potential vulnerabilities.
1. The PwDE used to perform the penetration testing MUST be identified as per [[AGD_PRE.1]](../methodology.md#-installation-guidance-agd_pre1).
1. The PwDE SHOULD be in [Security by Default configuration](../definitions.md#-security-by-default-configuration) as per [[AGD_PRE.1]](../methodology.md#-installation-guidance-agd_pre1).
1. MUST be coherent with the security objectives for the operational environment described in [[ASE_OBJ.1]](../methodology.md#-security-objectives-ase_obj1).
1. If any test resources are used, they MUST be calibrated and used correctly.
1. MUST record the actual results of the penetration tests.

⚠️ If no penetration testing was devised, this requirement DOES NOT apply.
### VAN-6 - Conclude that the product is placed in the market without known exploitable vulnerabilities.

1. The manufacturer MUST fix all known [actively exploited vulnerabilities](../definitions.md#actively-exploited-vulnerabilities) before placing the PwDE in the market.
1. The manufacturer MUST fix all [known exploitable vulnerabilities](../definitions.md#-known-exploitable-vulnerability) before placing the PwDE in the market.

⚠️ The section 5.3.2 of the [TR-03183](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Standards-und-Zertifizierung/Technische-Richtlinien/TR-nach-Thema-sortiert/tr03183/TR-03183_node.html) interprets as optional the fixing [known exploitable vulnerabilities](../definitions.md#-known-exploitable-vulnerability).
