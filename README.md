# Impact Measurement Standard (IMS)

**Maintained by:** ImpactMint  
**Status:** Public Draft  
**Version:** IMS Core (with IMS 2.0 Extensions)

---

## What is IMS?

The **Impact Measurement Standard (IMS)** is a neutral, machine-readable data standard for representing real-world impact activities with **evidence, verification, and audit-ready structure**.

IMS is designed to act as the **data and trust layer** beneath sustainability reporting and disclosure frameworks such as:

- ISSB (IFRS S1 & S2)
- UN Sustainable Development Goals (SDGs)
- UNDP Results Framework
- GRI Standards

IMS does **not** replace these frameworks.  
It enables **credible, high-quality impact data** to flow into them.

---

## 🔒 Full Platform Code — Judge Access

The complete platform source code and architecture documentation are in a 
private repository. Access has been granted to Colosseum judges.

👉 https://github.com/mustafazaidi-impact/impactmint-platform

Questions: mustafa.zaidi@getmedloop.com

---

## Why IMS exists

Regulators and markets are moving away from *tick-box ESG* toward **decision-useful, verifiable sustainability data**.

Most existing tools focus on:
- questionnaires
- reporting templates
- disclosures

IMS focuses on what is missing:

> **How impact data is structured, verified, and trusted before it becomes a report.**

---

## Design principles

IMS is built on the following principles:

- **Verification-first** — evidence and assurance are core, not optional  
- **Period-aware** — impact is time-bound and closable  
- **Framework-agnostic** — usable across ISSB, SDGs, GRI, UNDP  
- **Chain-agnostic** — blockchain optional, not mandatory  
- **Backward-compatible** — IMS Core remains stable over time  

---

## IMS structure

IMS is composed of two layers:

### 1. IMS Core (stable)

IMS Core defines the minimum structure required to represent an impact activity:

- Organization and project identifiers
- Impact activity type and quantity
- Reporting period (start and end)
- Source metadata

IMS Core is backward-compatible with IMS 1.0.

---

### 2. IMS 2.0 Extensions (optional)

IMS 2.0 adds **audit-grade and assurance-focused extensions**, including:

- Verification layers (human and automated)
- Evidence references (e.g., IPFS CIDs)
- Impact confidence and uncertainty
- Reporting period closure
- Cryptographic fingerprints for integrity

These extensions are **additive and optional**.

---

## Example (IMS Core + IMS 2.0 Extensions)

```json
{
  "ims_version": "core+2.0",
  "activity": {
    "activity_type": "Tree Plantation",
    "quantity": 500,
    "unit": "trees"
  },
  "reporting_period": {
    "start": "2025-01-01",
    "end": "2025-03-31",
    "closed_at": "2025-04-05"
  },
  "impact_value": {
    "value": 212.5,
    "unit": "tCO2e",
    "confidence": 0.87,
    "uncertainty_range": "+/- 12%"
  },
  "verification": {
    "final_status": "verified"
  }
}

```
## IMS Core Compliance

Fields required for **IMS Core compliance** remain valid even if **IMS 2.0 extensions** are not present.  
This ensures backward compatibility and supports phased adoption across organizations and systems.

---

## Verification model

IMS supports **multi-layer verification**, including:

- **Human verification** (auditors, verifiers)
- **Automated checks** (rules-based validation, anomaly detection)
- **Future machine-assisted verification**

Verification layers are recorded explicitly to support **auditability, transparency, and trust**.

---

## Reporting period closure

IMS supports **reporting period finality**.

Once a reporting period is closed:

- Impact values **must not change**
- Amendments **create new records**
- A **closure hash** ensures non-repudiation

This aligns impact data handling with **financial audit practices**.

---

## Impact fingerprint

IMS supports **cryptographic fingerprints** derived from:

- Core impact data
- Evidence references
- Verification layers
- Reporting period closure

Fingerprints enable:

- Tamper detection
- Cross-system verification
- Optional on-chain anchoring

IMS **does not require blockchain usage**.

---

## Regulatory alignment

IMS is designed to support regulatory and institutional requirements, including:

- **ISSB S1 & S2** (IFRS Sustainability Standards)
- **UN SDGs** and **UNDP Results Framework**
- **GRI disclosures**
- **National sustainability reporting regimes** (e.g., SECP)

IMS focuses on **data quality and assurance**, not disclosure formatting.

---

## What IMS is not

IMS is **not**:

- an ESG reporting template
- a sustainability score
- a carbon registry
- a marketplace
- a disclosure framework

**IMS is infrastructure.**

---

## Governance and evolution

IMS is maintained by ImpactMint as a **public, evolving standard**.

- IMS Core remains stable
- Extensions evolve incrementally
- Backward compatibility is preserved
- Feedback and proposals are welcome

IMS is intended to be **adopted, extended, and implemented across systems**.

---

## Status

- **IMS Core** is stable  
- **IMS 2.0 extensions** are in active development and pilot use  

Reference implementations and APIs are under development.

---

## License

Recommended license: **CC-BY 4.0** (or equivalent permissive license)
