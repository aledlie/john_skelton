---
layout: single
title: "Technical & International Arbitration Track Capstone Internship Proposal"
excerpt: "AI Governance & Compliance Engineering Intern at IntegrityStudio.ai - A hands-on internship combining international arbitration expertise with observability platform development, API integration, compliance automation, and dispute-ready evidence systems."
author_profile: true
toc: true
toc_label: "Contents"
toc_sticky: true
---

## Position Overview

**Title:** AI Governance & Compliance Engineering Intern (Technical & International Arbitration Track)

**Department:** Policy & Compliance Engineering

**Supervisors:**
- John Skelton (Head of Policy) - Legal/regulatory guidance
- Minea Arkiomaa (Head of AI Compliance Development) - Technical compliance implementation

**Duration:** 12 weeks (Full-time) or 20 weeks (Part-time)

**Location:** Remote with optional hybrid in Austin, TX

---

## Executive Summary

This technical and international arbitration track capstone leverages John Skelton's unique combination of international commercial arbitration expertise, EU law foundation, and multilingual capabilities while adding substantial hands-on technical work with IntegrityStudio's AI observability platform. The internship produces both actionable compliance research and functional technical artifacts including compliance automation tools, API integration guides, and evaluation frameworks that directly enhance IntegrityStudio's enterprise offerings.

Beyond immediate deliverables, this track builds skills aligned with John's long-term career interests at organizations including **Jus Mundi** (legal intelligence for international arbitration), **Institute for AI Policy and Strategy** (AI governance research), and **OpenAI** (AI safety and policy).

---

## Project Title

**"Building Technical Infrastructure for Cross-Border AI Compliance & Dispute Resolution: From Observability to Arbitration-Ready Evidence Systems"**

---

## Why Technical & International Arbitration Track

### The Business Need

Enterprise AI compliance requires more than policy documents. Organizations need:
- **Automated compliance monitoring** integrated with AI observability platforms
- **API-driven audit trails** that satisfy multiple regulatory regimes
- **Evaluation frameworks** that translate legal requirements into measurable technical criteria
- **Integration tooling** connecting legal obligations to engineering workflows

### John's Foundation for Technical Growth

| Qualification | Technical Application |
|--------------|----------------------|
| LLM International Commercial Arbitration (Stockholm) | Design dispute-ready audit trail specifications |
| LLB International & European Law (Groningen) | Translate EU AI Act into technical compliance rules |
| EU AI Act coursework | Immediate familiarity with risk classification logic |
| Quadrilingual (DE/ES/EN/FR) | Parse multilingual regulatory APIs and documentation |
| Legal research methodology | Systematic approach to technical documentation |

### Technical Skills to Develop

- OpenTelemetry observability concepts and instrumentation
- API integration patterns for compliance automation
- AI evaluation methodology and metrics design
- Technical documentation for developer audiences
- Collaboration with engineering teams on compliance features

---

## Project Scope & Deliverables

### Phase 1: Technical Foundations & Regulatory Mapping (Weeks 1-4)

**Objective:** Establish regulatory landscape and learn IntegrityStudio's technical architecture.

**Technical Learning:**
1. Complete IntegrityStudio platform onboarding:
   - Understand OpenTelemetry-based observability architecture
   - Learn trace, metric, and log collection patterns
   - Study AI evaluation and monitoring capabilities
   - Review API documentation and SDK usage

2. Shadow engineering sessions:
   - Attend 2-3 engineering standups weekly
   - Pair with engineers on compliance-related features
   - Review platform codebase architecture (read-only)

**Research Tasks:**
1. Conduct comparative legal analysis with technical mapping:
   - EU AI Act (risk classification algorithms, documentation requirements)
   - NIST AI RMF (evaluation metrics, risk management controls)
   - National implementations (DE, FR, ES, UK technical guidance)

2. Map regulatory requirements to observability capabilities:
   - Which OpenTelemetry signals satisfy which obligations?
   - Identify technical gaps in audit trail coverage
   - Document API endpoints needed for compliance reporting

**Deliverables:**
- *Regulatory-to-Observability Mapping Document* (technical specification)
- *Platform Architecture Notes* (personal learning documentation)
- *Compliance API Requirements Specification*

---

### Phase 2: Compliance Automation Development (Weeks 5-8)

**Objective:** Build technical artifacts that automate compliance workflows.

**Technical Tasks:**

1. **Develop Compliance Rule Engine Specifications:**
   - Define JSON schema for EU AI Act risk classification rules
   - Create rule templates for high-risk AI system detection
   - Specify API contracts for compliance status queries

   ```yaml
   # Example: Risk Classification Rule Structure
   rule:
     id: eu-ai-act-high-risk-001
     jurisdiction: EU
     regulation: AI_ACT
     article: "6"
     risk_level: HIGH
     conditions:
       - ai_system_category: "biometric_identification"
       - deployment_context: "public_spaces"
     required_documentation:
       - technical_documentation
       - conformity_assessment
       - eu_declaration_of_conformity
     audit_trail_requirements:
       - input_data_logging: true
       - output_decision_logging: true
       - human_oversight_logging: true
   ```

2. **Create Compliance Checklist API Integration Guide:**
   - Document IntegrityStudio API endpoints for compliance checks
   - Write integration examples in Python/curl
   - Build sample scripts for automated compliance verification

3. **Design Audit Trail Specification for Arbitration Readiness:**
   - Define evidence chain-of-custody data model
   - Specify timestamp, hash, and provenance requirements
   - Create export format specifications (JSON-LD, legal-ready PDF)

**Deliverables:**
- *EU AI Act Compliance Rule Schema* (JSON Schema + documentation)
- *IntegrityStudio Compliance API Integration Guide* (developer documentation)
- *Arbitration-Ready Audit Trail Specification* (technical + legal)

---

### Phase 3: AI Evaluation Framework & Tooling (Weeks 9-11)

**Objective:** Create evaluation frameworks that bridge legal requirements and technical metrics.

**Technical Tasks:**

1. **Build AI Evaluation Criteria Library:**
   - Translate EU AI Act Annex IV requirements into measurable metrics
   - Define evaluation thresholds for fairness, transparency, robustness
   - Create metric collection specifications using OpenTelemetry conventions

   | Legal Requirement | Technical Metric | OpenTelemetry Signal |
   |-------------------|-----------------|---------------------|
   | Accuracy (Art. 15) | F1 Score, AUC-ROC | `ai.model.accuracy` gauge |
   | Bias Mitigation | Demographic parity | `ai.fairness.disparity` histogram |
   | Transparency | Explainability score | `ai.explainability.fidelity` gauge |
   | Human Oversight | Override rate | `ai.oversight.interventions` counter |

2. **Develop Compliance Dashboard Wireframes:**
   - Design multi-jurisdictional compliance status views
   - Create alert threshold configurations
   - Specify drill-down paths from summary to evidence

3. **Create Arbitration Evidence Export Tool Specification:**
   - Define API for generating dispute-ready evidence packages
   - Specify cryptographic verification requirements
   - Document chain-of-custody metadata standards

**Deliverables:**
- *AI Evaluation Metrics Library* (technical specification + examples)
- *Compliance Dashboard Design Document* (wireframes + data model)
- *Dispute Resolution Evidence Export Specification*

---

### Phase 4: Integration & Technical Documentation (Week 12)

**Objective:** Synthesize technical work into production-ready documentation.

**Technical Tasks:**
1. Finalize all technical specifications for engineering handoff
2. Create developer onboarding guide for compliance features
3. Document lessons learned and technical recommendations
4. Present technical architecture to engineering team

**Deliverables:**
- *Technical Specification Package* (all schemas, APIs, specifications)
- *Compliance Engineering Developer Guide*
- *Final Technical Presentation*

---

## Final Capstone Deliverable

### "IntegrityStudio Technical Compliance Toolkit"

**Format:** Technical documentation repository + specification package

**Contents:**

```
PART I: REGULATORY-TECHNICAL MAPPING
├── Chapter 1: EU AI Act Technical Requirements
│   ├── Risk classification decision trees
│   ├── Documentation requirements as data schemas
│   └── Audit trail specifications
├── Chapter 2: OpenTelemetry for AI Compliance
│   ├── Signal mapping to legal obligations
│   ├── Instrumentation patterns
│   └── Compliance-specific semantic conventions
└── Chapter 3: Multi-Jurisdictional Rule Engine

PART II: API & INTEGRATION SPECIFICATIONS
├── Chapter 4: Compliance Rule Schema
│   └── JSON Schema + validation rules
├── Chapter 5: IntegrityStudio API Integration Guide
│   ├── Authentication and authorization
│   ├── Compliance status endpoints
│   └── Code examples (Python, curl, JavaScript)
├── Chapter 6: Audit Trail Data Model
│   └── Evidence preservation specifications
└── Chapter 7: Export Format Specifications

PART III: EVALUATION FRAMEWORK
├── Chapter 8: AI Evaluation Metrics Library
│   ├── Metric definitions
│   ├── Collection specifications
│   └── Threshold recommendations
├── Chapter 9: Compliance Dashboard Design
│   ├── Wireframes
│   ├── Data requirements
│   └── Alert configurations
└── Chapter 10: Arbitration Evidence Package Specification

APPENDICES
├── A: Regulatory Text Excerpts (Original + Translation)
├── B: API Reference Documentation
├── C: Schema Files (JSON, YAML)
└── D: Sample Implementation Code
```

---

## Technical Skill Development Matrix

```
WEEK 1-4                    WEEK 5-8                    WEEK 9-12
─────────────────────────────────────────────────────────────────────
Platform Onboarding         API Integration             Production Documentation
  ↓                           ↓                           ↓
OpenTelemetry Basics   →    Schema Design         →    Technical Writing
  ↓                           ↓                           ↓
Architecture Review         Compliance Automation       Engineering Handoff
  ↓                           ↓                           ↓
Engineering Pairing         Developer Documentation     Technical Presentation
```

### Technical Growth Milestones

| Week | Technical Skill | Demonstration |
|------|-----------------|---------------|
| 2 | OpenTelemetry fundamentals | Explain trace/metric/log model |
| 4 | API documentation reading | Navigate IntegrityStudio API docs |
| 6 | JSON Schema authoring | Complete compliance rule schema |
| 8 | Developer documentation | Publish integration guide draft |
| 10 | Evaluation metrics design | Define metric collection specs |
| 12 | Technical presentation | Present to engineering team |

---

## Cross-Functional Collaboration

### Engineering Team Integration

| Activity | Frequency | Purpose |
|----------|-----------|---------|
| Engineering standup (observer) | 2-3x/week | Understand development workflow |
| Pairing sessions | Weekly | Learn technical implementation |
| Code review observation | Bi-weekly | See compliance feature development |
| Architecture discussions | As needed | Inform specification design |

### Technical Mentorship

| Team Member | Role | Focus Area |
|-------------|------|------------|
| Alyshia Ledlie | CEO | Strategic technical vision |
| Micah Lindsay | Chief Data Scientist | AI evaluation methodology |
| Engineering Lead | TBD | Platform architecture, API design |
| DevRel/Docs (if applicable) | TBD | Technical documentation standards |

---

## Success Metrics

### Technical Deliverables

- [ ] Complete compliance rule JSON schema with validation
- [ ] Publish API integration guide (3+ code examples)
- [ ] Define 10+ evaluation metrics with OpenTelemetry mappings
- [ ] Create audit trail data model specification
- [ ] Design compliance dashboard wireframes
- [ ] Document arbitration evidence export format

### Technical Skill Demonstration

- [ ] Explain OpenTelemetry observability model
- [ ] Read and navigate API documentation independently
- [ ] Author valid JSON Schema definitions
- [ ] Write developer-focused technical documentation
- [ ] Present technical concepts to engineering audience
- [ ] Translate legal requirements into technical specifications

### Legal-Technical Integration

- [ ] Map 6+ jurisdictions' requirements to technical controls
- [ ] Create compliance automation rule templates
- [ ] Design arbitration-ready evidence preservation system
- [ ] Develop evaluation criteria bridging law and engineering

---

## Tools & Technical Access

### Development Environment
- IntegrityStudio platform demo/staging environment
- API access with developer credentials
- Documentation repository access (read/write for docs)
- Collaboration tools (Slack, Notion, GitHub)

### Technical Resources
- OpenTelemetry documentation and examples
- IntegrityStudio SDK documentation
- JSON Schema tooling (ajv, jsonschema)
- Diagramming tools (Mermaid, Excalidraw)

### Learning Resources
- OpenTelemetry Getting Started guides
- API design best practices documentation
- Technical writing style guides
- AI evaluation methodology papers

---

## Post-Internship Technical Pathways

1. **Technical Compliance Analyst:** Continue at IntegrityStudio with engineering collaboration
2. **Compliance Engineering:** Role bridging legal and engineering at AI companies
3. **AI Governance Tooling:** Product roles at compliance/observability platforms
4. **Standards Development:** Technical contributions to AI governance standards bodies
5. **Legal Engineering:** Emerging hybrid roles at law firms with technical practices

### Target Organizations for Future Opportunities

John has identified three organizations aligned with her long-term career interests:

| Organization | Why It Fits | Skills This Internship Develops |
|--------------|-------------|--------------------------------|
| **[Jus Mundi](https://jusmundi.com/)** | Leading legal intelligence platform for international arbitration; partnered with Dubai International Arbitration Centre on AI case management | Arbitration-ready audit trails, evidence preservation schemas, legal-tech API integration, multilingual compliance mapping |
| **[Institute for AI Policy and Strategy (IAPS)](https://www.iaps.ai/)** | AI governance research institute offering policy fellowships; bridges technical AI understanding with policy development | Technical specification writing, regulatory-to-code translation, AI evaluation frameworks, cross-jurisdictional analysis |
| **[OpenAI](https://openai.com/)** | Leading AI lab with growing policy, trust & safety, and compliance functions | OpenTelemetry observability, AI evaluation methodology, compliance automation, technical documentation for AI systems |

### How IntegrityStudio Prepares for These Paths

**For Jus Mundi:**
- Direct experience designing arbitration-ready evidence systems
- Technical understanding of AI-assisted legal research platforms
- API integration skills applicable to legal intelligence tools
- Multilingual regulatory mapping (DE/ES/FR sources)

**For IAPS:**
- Hands-on translation of AI regulations into technical requirements
- Research methodology combining legal analysis with technical specification
- Experience with AI governance frameworks across jurisdictions
- Portfolio of technical policy artifacts (schemas, evaluation criteria)

**For OpenAI:**
- OpenTelemetry and AI observability platform experience
- Understanding of AI evaluation metrics and safety monitoring
- Compliance automation and documentation skills
- Technical communication with engineering teams

---

## Application of John's Unique Strengths (Technical & International Arbitration Track)

| Background | Technical Application |
|------------|----------------------|
| Stockholm LLM in Arbitration | Design evidence preservation schemas; specify chain-of-custody data models |
| Groningen LLB in EU Law | Translate EU AI Act articles into JSON rule schemas; parse regulatory APIs |
| EU AI Act coursework | Immediate productivity mapping legal to technical requirements |
| Native German | Parse German BfDI technical guidance; review DE-language API docs |
| Native Spanish | Analyze AEPD technical specifications; support ES market integrations |
| C2 English | Primary language for technical documentation |
| B1 French | Review CNIL technical guidelines; support FR compliance mapping |
| Research methodology | Systematic approach to technical specification development |
| Enterprise legal experience | Understand compliance workflows that technical tools must support |

---

*This technical and international arbitration track capstone provides John Skelton the opportunity to develop hands-on technical skills while leveraging her legal expertise in cross-border dispute resolution. The combination of compliance knowledge, arbitration methodology, and technical capability positions her for emerging hybrid roles at the intersection of AI governance, international law, and engineering—including future opportunities at organizations like Jus Mundi, IAPS, and OpenAI where legal-technical fluency is increasingly valued.*

---

**Prepared for:** IntegrityStudio.ai Leadership Team
**Date:** January 2026
**Track:** Technical & International Arbitration
**Contact:** sales@integritystudio.ai
