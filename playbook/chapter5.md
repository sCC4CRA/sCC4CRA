# Chapter 5 - Testing
## 📋 Functional (ATE_FUN.1)
### FUN-1 - The test documentation shall consist of test plans, expected test results and actual test results.
1. MUST contain test plans, expected test results and actual test results.
1. MUST have sufficient detail to enable the tests to be repeatable.
### FUN-2 - The test plans shall describe the scenarios for performing each test. 
1. These scenarios MUST include any dependencies on the results of other tests.
1. The test plan SHOULD also provide information about the test configuration being used.
1. The test configuration SHOULD include the configuration of the PwDE and any test equipment being used.
1. The test plan SHOULD include information about how to execute the test.
1. This information SHOULD be detailed enough to ensure that the test configuration is reproducible.
1. The PwDE referred to in the developer's test plan SHOULD have the same unique reference as per the [[ASE_INT.1]](../methodology.md#-introduction-and-description-ase_int1).
1. All PwDE configurations declared in the [[ASE_INT.1]](../methodology.md#-introduction-and-description-ase_int1) MUST be tested in completeness.
1. The [[ASE_OBJ.1]](../methodology.md#-security-objectives-ase_obj1) SHOULD be considered for the configuration of the test environment.
### FUN-3 - The expected test results shall show the anticipated outputs from a successful execution of the tests.
1. The expected test results MUST determine whether or not a test has been successfully performed.
1. Expected test results MUST be unambiguous and consistent with expected behaviour given the testing approach.
### FUN-4 - The actual test results shall be consistent with the expected test results.
1. The PwDE used to perform the testing MUST be identified as per [[AGD_PRE.1]](../methodology.md#-installation-guidance-agd_pre1).
1. The PwDE SHOULD be in [Security by Default configuration](../definitions.md#-security-by-default-configuration) as per [[AGD_PRE.1]](../methodology.md#-installation-guidance-agd_pre1).
1. If results need to be processed before comparing, the test documentation SHOULD explain how.
1. The manufacturer MUST format expected results for easy comparison with actual results.
## 🔍 Depth (ATE_DPT.1)
### DPT-1 - Shall demonstrate the correspondence between the tests and the PwDE subsystems.
1. A simple cross-table MAY be sufficient to show test correspondence between the tests and the [[ADV_TDS.2]](../methodology.md#%EF%B8%8F-pwde-design-adv_tds2).
1. The identification of the tests and the behaviour/interaction presented in the depth-of coverage analysis MUST be unambiguous.
1. Every test MIGHT NOT map to a subsystem behaviour or interaction description.
### DPT-2 Shall demonstrate that all PwDE subsystems have been tested.
1. All descriptions of TSF subsystem behaviour MUST be tested.
1. All interactions among TSF subsystems that are provided in the PwDE design MUST be tested.
1. Every tests MIGHT NOT map to the subsystem behaviour or interaction description in the PwDE design.

****
Go to next [Chapter 6 - Vulnerability Analysis ➡️ ](chapter6.md) 
