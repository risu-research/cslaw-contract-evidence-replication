# Contract Versions and Claim-Specific Evidence in Public Procurement

Replication materials accompanying the ACM CS&LAW 2027 archival paper submission.

The archive contains the recorded procurement observations, source-document locators, SQL cross-checks, and executable tests of contract-version coherence. Its version-preserving query evaluator also produces checkable counterexamples for answers lost when related fields are treated independently.

## Run the replication checks

Download and extract [the artifact archive](CSLAW2027_Replication_Artifact.zip), enter the `CSLAW2027_V90_Review_Artifact` directory, and run:

```bash
python3 RUN_REVIEW.py
```

Python 3.10 or later is sufficient. The scripts use the standard library and run without a network connection. To include the extended experiments:

```bash
python3 RUN_REVIEW.py --full
```

Detailed run logs appear in `verification_output/`. You can check the generated query certificates separately:

```bash
python3 proof_engine/verify_certificates.py
```

## Results and source records

The archive provides reproducible checks for the 56-supplier, 560-cell comparison; ten settled category differences; seven category-level reconstructed lookup differences; and the recorded contract-version relations. In the RADcube case, the two inspected schedules give two coherent five-field vectors, while independent recombination permits 32 vectors, including 30 absent from either schedule.

The package also contains a reusable finite-version query evaluator, counterexample certificates, and tests of the representation on general finite relations.

Start with `RESULTS_AT_A_GLANCE.md` for the computations, `REVIEWER_EVIDENCE_MAP.md` for contract URLs and page references, and `REVIEWER_RESULT_MAP.md` for the corresponding scripts and inputs.

## Archive integrity

- File: `CSLAW2027_Replication_Artifact.zip`
- SHA-256: `d3c2db6c9eb02b201e01eef00fb56c474777e2656ab1b38a476906fcaff9b74d`
- Size: 260,482 bytes
- Python: 3.10+; no third-party dependencies

The scripts reproduce calculations from recorded observations. The cited source documents provide the evidence for those observations, and the paper supplies their legal interpretation.
