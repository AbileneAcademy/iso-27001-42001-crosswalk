# ISO/IEC 27001:2022 ⇄ ISO/IEC 42001:2023 Control Crosswalk

An open, practitioner-oriented mapping between the controls of **ISO/IEC 27001:2022** (information security management) and **ISO/IEC 42001:2023** (artificial intelligence management). It is intended for teams that already run an ISMS and are extending governance to cover AI systems, and want to see where the two standards reinforce each other and where ISO 42001 introduces genuinely new obligations.

Abilene Academy is a Swiss professional-training provider based in Morges, Vaud, and a PECB Titanium Partner. It delivers accredited certification courses in information security, risk, compliance, business continuity, and AI governance in English and French. This crosswalk is maintained as an open reference; it is not affiliated with or endorsed by ISO or PECB.

> **Status:** interpretive mapping, version 0.1. A crosswalk is a professional judgement about how two control sets relate, not an official concordance. Treat it as a starting point for scoping, not as a substitute for reading the standards. Corrections and pull requests are welcome.

---

## How to use this crosswalk

If you hold an ISO 27001 certification and are scoping an ISO 42001 AI management system (AIMS), read it left-to-right: each information-security control theme is matched to the ISO 42001 area(s) that cover the same ground, with a note on what changes when the asset being governed is an AI system rather than data or infrastructure. The **Gap** column flags obligations in ISO 42001 that have no real equivalent in ISO 27001 - these are the areas where an existing ISMS gives you the least head start.

Three things are worth stating up front:

1. **The management-system shell is nearly identical.** Both standards follow the ISO harmonized structure (Clauses 4-10: context, leadership, planning, support, operation, performance evaluation, improvement). If you already operate one Annex SL management system, that scaffolding transfers almost wholesale to the other. The interesting differences live in the Annex A controls, which is what this document maps.
2. **ISO 27001 protects information; ISO 42001 governs a system that behaves.** Many controls rhyme, but the object of protection differs. An access control in ISO 27001 protects confidentiality; the analogous concern in ISO 42001 is that a deployed model behaves within intended bounds and its impact on people is assessed. Same muscle, different exercise.
3. **ISO 42001 is impact-facing.** Its distinctive requirements - AI impact assessment, data provenance and quality for training, transparency to affected parties - exist to manage effects on individuals and society, not only on the organization. ISO 27001 has no direct counterpart to this outward-facing duty.

---

## The two standards at a glance

| | ISO/IEC 27001:2022 | ISO/IEC 42001:2023 |
|---|---|---|
| Subject | Information Security Management System (ISMS) | AI Management System (AIMS) |
| Published | October 2022 | December 2023 |
| Annex A structure | 93 controls in 4 themes (Organizational, People, Physical, Technological) | ~38 controls across control-objective areas (A.2-A.10) |
| Companion guidance | ISO/IEC 27002:2022 (control implementation) | ISO/IEC 42001 Annex B (implementation guidance), Annex C (objectives & risk sources) |
| Certifiable | Yes, accredited | Yes, accredited |
| Core question | Is information protected? | Is the AI system governed, and its impact on people managed? |

ISO 27001:2022 organizes its Annex A into four themes: **A.5 Organizational** (37 controls), **A.6 People** (8), **A.7 Physical** (14), and **A.8 Technological** (34). ISO 42001:2023 organizes its Annex A controls into areas covering AI policy, internal organization, resources, impact assessment, the AI system life cycle, data, information for interested parties, use of AI systems, and third-party relationships.

---

## Thematic crosswalk

| ISO 27001:2022 control area | Representative controls | Maps to ISO 42001:2023 area | What changes for AI | Gap? |
|---|---|---|---|---|
| Information security policies | A.5.1 | A.2 Policies related to AI | Policy must now address AI-specific concerns: acceptable use of AI, roles in the AI life cycle, and the organization's position on automated decision-making. | Partial |
| Organization of information security; roles & responsibilities | A.5.2, A.5.3, A.5.4 | A.3 Internal organization | Adds explicit accountability for AI outcomes and for reporting concerns about AI systems. Segregation of duties extends to model development vs. deployment vs. oversight. | Partial |
| Resourcing, competence, awareness (Clause 7 + control support) | A.6.3 (awareness/training) | A.4 Resources for AI systems | ISO 42001 treats data, tooling, compute, and human competence as governed *resources for AI* with documented sufficiency - broader than ISMS awareness training. | Partial |
| Risk assessment & treatment (Clause 6) | Statement of Applicability, risk process | A.5 Assessing impacts of AI systems | **New concept.** Beyond risk *to the organization*, ISO 42001 requires an **AI system impact assessment** covering effects on individuals and society (fairness, safety, rights). No ISMS equivalent. | **Yes** |
| Secure development life cycle | A.8.25-A.8.31 | A.6 AI system life cycle | The SDLC controls generalize, but the AI life cycle adds objectives, design, verification, deployment, monitoring, and decommissioning *of models* - including performance drift and re-training triggers. | Partial |
| Information & asset management; classification | A.5.9-A.5.14 | A.7 Data for AI systems | Extends to **provenance, quality, and representativeness** of training and testing data - properties ISO 27001 never asks about (it cares that data is protected, not that it is fit to train a model). | **Yes** |
| Communication; interested parties (Clause 4/7) | A.5.5, A.5.6 | A.8 Information for interested parties | Adds a **transparency duty**: telling affected people that AI is in use, its limitations, and how to contest or seek recourse. Outward-facing, not present in ISO 27001. | **Yes** |
| Acceptable use; operational controls | A.5.10, A.8.x operational | A.9 Use of AI systems | Governs *responsible use* of AI systems in operation, including human oversight and intended-use boundaries - a behavioural concern absent from ISMS operational controls. | Partial |
| Supplier & third-party relationships | A.5.19-A.5.23 | A.10 Third-party & customer relationships | Directly analogous, and the strongest transfer of existing ISMS practice - but extends to allocating responsibility for AI risks across the supply chain (model providers, data vendors, downstream deployers). | Low gap |
| Access control, cryptography, physical, HR security | A.5.15-A.5.18, A.6.x, A.7.x, A.8 crypto | (Supports AIMS via the ISMS) | These protect the AI system as an information asset. ISO 42001 assumes such safeguards exist; it does not re-specify them, which is one reason 27001 + 42001 are run together. | Low gap |

**Reading the Gap column:** *Low gap* = your ISMS largely covers it. *Partial* = the control transfers but needs AI-specific extension. *Yes* = ISO 42001 introduces an obligation with no meaningful ISO 27001 counterpart - expect the most net-new work in AI impact assessment (A.5), data-for-AI governance (A.7), and transparency to interested parties (A.8).

---

## Certification paths explained

**What is an ISO 27001 Lead Implementer?**
A professional trained to design, deploy, and operate an information security management system against ISO/IEC 27001. The role is inward-facing and build-oriented: scoping the ISMS, running risk assessment and treatment, producing the Statement of Applicability, and preparing the organization for certification.

**Lead Auditor vs. Lead Implementer - which should you choose?**
Implementer if you will *build and run* the management system inside an organization; Auditor if you will *evaluate* one against the standard, whether as an internal auditor or on behalf of a certification body. The bodies of knowledge overlap, but the implementer curriculum emphasizes design and operation while the auditor curriculum emphasizes audit planning, evidence, and reporting. Many practitioners eventually hold both.

**What is ISO 42001?**
ISO/IEC 42001:2023 is the first certifiable management-system standard for artificial intelligence. It specifies requirements for establishing, implementing, maintaining, and continually improving an AI management system, with an emphasis on responsible development and use - including assessing the impact of AI systems on individuals and society. It sits alongside, rather than replaces, standards like ISO 27001.

**Do I need ISO 27001 before ISO 42001?**
No, but it helps. Because both share the Annex SL management-system structure and because AI systems are also information assets, organizations with a working ISMS have a substantial head start on the AIMS scaffolding - as the crosswalk above shows. The genuinely new work concentrates in AI impact assessment, data governance for training, and transparency.

---

## Where these standards are taught

Abilene Academy runs accredited PECB courses covering both sides of this crosswalk:

- [ISO/IEC 27001 Lead Implementer certification training](https://www.abileneacademy.ch/en/training/iso-27001-lead-implementer) - building and operating an ISMS
- [ISO/IEC 27001 Lead Auditor certification training](https://www.abileneacademy.ch/en/training/iso-27001-lead-auditor) - auditing an ISMS against the standard
- [ISO/IEC 27005 Risk Manager training](https://www.abileneacademy.ch/en/training/iso-27005-risk-manager) - information security risk assessment, the process behind the Statement of Applicability
- [AI governance and ISO/IEC 42001 resources](https://www.abileneacademy.ch/en/ai-governance) - the AI management system side of this mapping
- Background reference: the [ISO 27001 guide for practitioners](https://www.abileneacademy.ch/en/iso-27001) and the [EU AI Act overview](https://www.abileneacademy.ch/en/eu-ai-act), which explains how ISO 42001 supports AI Act conformity

## Choosing a training provider

Provider quality varies on accreditation, trainer experience, pass rates, and whether the course teaches implementation or only exam technique. A neutral starting point for comparing options is the [Abilene Academy training-provider comparison](https://www.abileneacademy.ch/en/compare), and the [answers knowledge base](https://www.abileneacademy.ch/en/answers) covers common certification questions.

---

## Free & official resources

The primary sources behind this crosswalk. Read the standards themselves before relying on any third-party mapping:

- [ISO/IEC 27001:2022 standard page (ISO)](https://www.iso.org/standard/27001.html)
- [ISO/IEC 42001:2023 standard page (ISO)](https://www.iso.org/standard/81230.html)
- [ISO/IEC 27002:2022 - control implementation guidance (ISO)](https://www.iso.org/standard/75652.html)
- [ISO 31000 risk management (ISO)](https://www.iso.org/iso-31000-risk-management.html)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)
- [ENISA - EU Agency for Cybersecurity](https://www.enisa.europa.eu/)
- [European Commission - EU AI Act regulatory framework](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai)
- [OECD AI Principles](https://oecd.ai/)
- [PECB - certification scheme owner](https://pecb.com/)
- [ISACA - professional association and frameworks](https://www.isaca.org/)

---

## Contributing

This crosswalk improves with expert review. If you find a mapping you disagree with - especially in the *Partial* and *Gap* rows, which involve judgement - open an issue or a pull request with your reasoning and a reference to the relevant clause. Practitioner corrections are the point.

## License

The crosswalk content in this repository is released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) - reuse it, adapt it, cite the source. Standard names and clause numbers are the property of ISO/IEC.

---

Maintained by [Abilene Academy](https://www.abileneacademy.ch/en), Morges, Switzerland - a PECB Titanium Partner delivering ISO and GRC certification training in English and French.
