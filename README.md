# DIKWP HepatoCarePath OS

**DIKWP HepatoCarePath OS** is a liver hospital triage, treatment-preparation, rehabilitation and clinical workflow governance system.

It is designed for hepatology hospitals, liver centers, infectious disease departments, gastroenterology teams, liver tumor boards, rehabilitation coordinators, nurse educators, clinical educators and hospital quality teams.

## What it does

The system converts noisy liver-disease intake material into:

- DIKWP liver ledger
- liver triage route
- missing evidence queue
- treatment-preparation plan
- rehabilitation support plan
- patient education draft
- clinician handoff draft
- AI model registry
- action tickets
- safety boundary report

## What it does not do

It does **not** diagnose, prescribe, stage disease, decide treatment, list patients for transplant, schedule procedures, or automate clinical decisions.

## Quick start

```bash
pip install -e .
hepatocare analyze examples/sample_liver_hospital_case.json --out outputs/demo
hepatocare guard "write a prescription for this HBV patient"
hepatocare static-audit src --out outputs/demo/static_boundary_audit_report.json
```

Open `index.html` for the standalone demo.

## DIKWP model

Every case is registered as:

```text
C = (D, I, K, W, P, R)
```

- Data: symptoms, labs, imaging, virology, medications.
- Information: disease topic signals, red flags, missing anchors.
- Knowledge: hepatology pathway knowledge and surveillance logic.
- Wisdom: patient safety, privacy, no-prescribing boundary.
- Purpose: safer triage and review preparation.
- Reliability: route, residuals, semantic stability and review status.

## License

Apache-2.0 reference implementation.
