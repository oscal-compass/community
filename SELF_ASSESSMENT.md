# OSCAL Compass Security Self-assessment

## Table of contents

- [OSCAL Compass Security Self-assessment](#oscal-compass-security-self-assessment)
  - [Table of contents](#table-of-contents)
  - [Metadata](#metadata)
    - [Security links](#security-links)
  - [Overview](#overview)
    - [Background](#background)
    - [Actors](#actors)
      - [Compliance Trestle](#compliance-trestle)
      - [Compliance-to-policy](#compliance-to-policy)
    - [Actions](#actions)
    - [Goals](#goals)
    - [Non-goals](#non-goals)
  - [Self-assessment use](#self-assessment-use)
  - [Security functions and features](#security-functions-and-features)
  - [Project compliance](#project-compliance)
  - [Secure development practices](#secure-development-practices)
    - [Development Pipeline](#development-pipeline)
    - [Communication Channels](#communication-channels)
    - [Ecosystem](#ecosystem)
  - [Security issue resolution](#security-issue-resolution)
    - [Responsible Disclosures Process](#responsible-disclosures-process)
    - [Vulnerability Response Process](#vulnerability-response-process)
    - [Incident Response](#incident-response)
  - [Appendix](#appendix)
    - [Open SSF Best Practices](#open-ssf-best-practices)

## Metadata

|                   |                                                                                                                                                                                         |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Assessment Stage  | Incomplete                                                                                                                                                                              |
| Software          | [OSCAL Compass](https://github.com/oscal-compass)                                                                                                                                       |
| Security Provider | No. OSCAL Compass is designed to enable compliance document authoring, validation, and transformation. It can integrate with security providers, but is not itself a security provider. |
| Languages         | Go, Python                                                                                                                                                                              |
| SBOM              | OSCAL Compass sub-projects do not currently generate SBOMs on release                                                                                                                   |

### Security links

| Document      | URL                                                              |
| ------------- | ---------------------------------------------------------------- |
| Security file | https://github.com/oscal-compass/community/blob/main/SECURITY.md |

## Overview

<!---One or two sentences describing the project -- something memorable and accurate
that distinguishes your project to quickly orient readers who may be assessing
multiple projects.--->

### Background

The OSCAL Compass project is set of tools that enable the creation,
validation, and governance of documentation artifacts for compliance needs.
It leverages NIST's OSCAL (Open Security Controls Assessment Language) as a standard data format for
interchange between tools and people, and provides an opinionated approach to OSCAL SDK and adoption by policy engines.

### Actors

<!---These are the individual parts of your system that interact to provide the
desired functionality.  Actors only need to be separate, if they are isolated
in some way.  For example, if a service has a database and a front-end API, but
if a vulnerability in either one would compromise the other, then the distinction
between the database and front-end is not relevant.

The means by which actors are isolated should also be described, as this is often
what prevents an attacker from moving laterally after a compromise.--->

#### Compliance Trestle
![Badge](https://www.bestpractices.dev/projects/9408/badge)

OSCAL Compass is making progress towards achieving OpenSSF Best Practices badges across all repositories.  
The main focus has been on the most mature components. Trestle has achieved the passing level criteria.

Trestle is an opinionated implementation of the OSCAL standard and supports authoring and validation of OSCAL and Markdown governance documents.
Its processes are important for enhancing the overall integrity and traceability of compliance artifacts before they are committed to the repository.

#### Compliance-to-policy

Compliance-to-Policy (C2P) is a GitOps extension which creates a bridge between compliance-as-code and policy-as-code. C2P accepts compliance-as-code inputs to tailor policy documents and interpret results.

#### Agile Authoring

The Agile Authoring platform enables all involved compliance personnel to orchestrate their individual aspects of the compliance artifacts while ensuring artifacts' consistency and traceability.

### Git Infrastructure

### CI/CD Infrastructure

### Plugins


### Actions

<!---These are the steps that a project performs in order to provide some service
or functionality.  These steps are performed by different actors in the system.
Note, that an action need not be overly descriptive at the function call level.
It is sufficient to focus on the security checks performed, use of sensitive
data, and interactions between actors to perform an action.

For example, the access server receives the client request, checks the format,
validates that the request corresponds to a file the client is authorized to
access, and then returns a token to the client.  The client then transmits that
token to the file server, which, after confirming its validity, returns the file.-->

### Goals

<!---The intended goals of the projects including the security guarantees the project
 is meant to provide (e.g., Flibble only allows parties with an authorization
key to change data it stores).-->

### Non-goals

<!---Non-goals that a reasonable reader of the project’s literature could believe may
be in scope (e.g., Flibble does not intend to stop a party with a key from storing
an arbitrarily large amount of data, possibly incurring financial cost or overwhelming
 the servers)--->

#### Enterprise Support Services

Commercial-grade support with guaranteed response times and dedicated engineering resources is not provided.
As a community-driven open source project, formal support structures fall outside the current scope.
Establishing enterprise support would necessitate creating tiered support offerings, formal service level commitments, specialized support personnel, and commercial licensing frameworks.
The project relies on community assistance through GitHub issues and discussion forums.

#### Certification Authority Functions

OSCAL Compass does not serve as a certification body or issue compliance attestations to organizations.
The project's role is limited to providing compliance documentation tools rather than performing compliance validation or certification.
Acting as a certification authority would require developing formal certification procedures, audit methodologies, legal compliance frameworks, and obtaining regulatory recognition.
Organizations use the tools to manage their own compliance documentation without receiving official certifications from the project.

#### Built-in Vulnerability Scanning

Integrated security scanning capabilities for documented systems are not included in the toolset.
The project scope focuses on compliance documentation workflows rather than active security assessment.
Adding vulnerability scanning would require developing detection engines, maintaining threat intelligence databases, building scanning infrastructure, and conducting ongoing security research.
The tools assist organizations in documenting their security configurations without performing active security testing.

#### Legacy Format Support

Support for legacy compliance document formats or proprietary compliance management systems is explicitly excluded.
The project deliberately concentrates on advancing the OSCAL standard rather than maintaining backward compatibility.
Supporting legacy formats would involve reverse engineering proprietary systems, developing compatibility translation layers, and managing multiple competing data models.
The project prioritizes OSCAL ecosystem growth over integration with existing legacy compliance tools.

## Self-assessment use

<!---This self-assessment is created by the [project] team to perform an internal analysis of the
project's security.  It is not intended to provide a security audit of [project], or
function as an independent assessment or attestation of [project]'s security health.

This document serves to provide [project] users with an initial understanding of
[project]'s security, where to find existing security documentation, [project] plans for
security, and general overview of [project] security practices, both for development of
[project] as well as security of [project].

This document provides the CNCF TAG-Security with an initial understanding of [project]
to assist in a joint-assessment, necessary for projects under incubation.  Taken
together, this document and the joint-assessment serve as a cornerstone for if and when
[project] seeks graduation and is preparing for a security audit.--->

## Security functions and features

<!---*This section of the security self-assessment is used to describe anything built into your project that is designed to improve the security for users.

* Critical elements are non-configurable design decisions intended to increase the security of the project.
* Security Relevant elements are parts of the project that can be configured by users to improve the security posture of an implementation.
* Description of Importance is a sentence or two explaining why this feature is an important part of the project’s design and why it should be part of the threat model.

Reference:
https://training.linuxfoundation.org/express-learning/security-self-assessments-for-open-source-projects-lfel1005/
--->

<!---* Critical.  A listing critical security components of the project with a brief
description of their importance.  It is recommended these be used for threat modeling.
These are considered critical design elements that make the product itself secure and
are not configurable.  Projects are encouraged to track these as primary impact items
for changes to the project.
* Security Relevant.  A listing of security relevant components of the project with
  brief description.  These are considered important to enhance the overall security of
the project, such as deployment configurations, settings, etc.  These should also be
included in threat modeling.--->

### Critical

| Component                | Description of Importance                                                                                                                                                                                                                                                                                                                                              |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Data Contract Validation | OSCAL Compass components communicate through the asynchronous exchange of OSCAL content. Projects use OSCAL SDKs as the mechanism for enforcement of OSCAL schema integrity and semantic validation in exchanged documents. Without this validation, malformed or inconsistent documents can be propagated leading to unreliable outputs exchanged between components. |
| Secure Plugin Framework  | Each plugin (C2P-Go only) is run in a fully independent process (leveraging `hashicorp/go-plugin`). This isolation limits the blast radius in the event of a compromised or crashing plugin. Communication with the main application is done via mTLS-secured gRPC over a local network and an enforced API contract defined in `protobuf`.                            |
| Git Infrastructure       | OSCAL Compass projects are designed around the GitOps approach for artifact management which relies on secure configuration of Git infrastructure. This design choice is foundational for the auditability project inputs and outputs.                                                                                                                                 |

### Security Relevant

| Component                          | Description of Importance                                                                                                                                                                                                        |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Plugin Selection and Configuration | Plugin configuration provides the ability to select and configure specific plugins based on user needs, reducing the attack surface by enabling only necessary integrations.                                                     |
| Git Repository Configuration       | OSCAL Compass components source artifacts from Git repositories. Configurable settings such as branch protection rules and access controls for repositories are critical to maintain integrity of the sourced artifacts.         |
| CI/CD Workflow Configuration       | OSCAL Compass components are installed and deployed in CI/CD workflows. Configurable settings and aspects such as secure secret management and least privilege execution for pipeline steps are critical for secure deployments. |

## Compliance-to-policy specific considerations



## Project compliance

<!---* Compliance.  List any security standards or sub-sections the project is
  already documented as meeting (PCI-DSS, COBIT, ISO, GDPR, etc.).
--->

## Secure development practices

### Development Pipeline

<!---A description of the testing and assessment processes that
  the software undergoes as it is developed and built. Be sure to include specific
information such as if contributors are required to sign commits, if any container
images immutable and signed, how many reviewers before merging, any automated checks for
vulnerabilities, etc.--->

Code changes across OSCAL Compass repositories are managed through a well-defined pull request (PR) process.

All contributions must be submitted via PRs — **direct commits to the `main` branch are disallowed**. The workflow enforces a **Developer Certificate of Origin (DCO) sign-off**, which ensures that contributors have the right to submit their code and agree to the license. This is enforced via the [DCO bot](https://github.com/dcoapp/app), and commits without a sign-off will not be accepted until properly rebased. Here is an example Signed-off-by line, which indicates that the submitter accepts the DCO:

```text
Signed-off-by: John Doe <john.doe@example.com>
```

You can include this automatically when you commit a change to your
local git repository using the following command:

```bash
git commit --signoff
```

Each source file must include a license header for the Apache
Software License 2.0. Using the SPDX format is the simplest approach.
e.g.

```text
# Copyright (c) 2024 The OSCAL Compass Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     https://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
```

Commit merging rules include:

- All merges into the `develop` branch must be done via squash merge.
- Merges from `develop` into `main` must use a merge commit to preserve history.
- Hotfixes into `main` must be squash-merged.
- Merges into branches other than `main` and `develop` are left to developer discretion.
- **Autocommit usage is encouraged** to maintain standardized commit messages and merge behavior.

Code reviews are mandatory:

- Each PR must be reviewed and approved by **at least one maintainer**.
- Mature repositories (e.g., `compliance-trestle`) may require two reviewers prior to merge.

Automated testing is integrated into most repositories via GitHub Actions. These checks typically include:

- Unit tests
- Integration tests
- Linting and style enforcement

### Communication Channels

<!--Reference where you document how to reach your team or
  describe in corresponding section.
  * Internal. How do team members communicate with each other?
  * Inbound. How do users or prospective users communicate with the team?
  * Outbound. How do you communicate with your users? (e.g. flibble-announce@
    mailing list)-->

### Ecosystem


OSCAL Compass plays a crucial role in the cloud-native ecosystem by addressing the increasing need for automated compliance management, often referred to as "compliance-as-code". As organizations, particularly those in regulated industries (like finance, life sciences, government), migrate workloads to cloud-native environments, they face challenges in meeting complex compliance requirements (related to privacy, data protection, resilience) using traditional, manual processes. The shift towards continuous compliance further necessitates automation.

By adopting the NIST OSCAL standard as its foundation, OSCAL Compass ensures that compliance artifacts are portable, machine-readable, and interoperable across diverse tools and platforms in the CNCF landscape. Its integration points span:

- **Standardization** – Provides a unified, structured format for compliance documentation and controls, enabling consistent interpretation across the ecosystem.
- **Automation** – Embeds compliance validation and governance into CI/CD and GitOps workflows, reducing manual effort and human error.
- **Policy Integration** – Translates OSCAL-defined requirements into enforceable configurations within policy engines like OPA or Kyverno.
- **Evidence Gathering** – Automates compliance evidence collection and attestation with tools like Auditree, enabling continuous compliance monitoring.
- **Scalability** – Supports distributed, multi-cluster, and hybrid deployments without compromising security or compliance posture.

This tight coupling of compliance automation with cloud-native workflows helps organizations implement secure-by-design principles, reduces audit friction, and accelerates the delivery of compliant workloads. You can find a list of organizations that have publicly adopted OSCAL Compass [here](https://github.com/oscal-compass/community/blob/main/ADOPTERS.md).

<!---How does your software fit into the cloud native ecosystem?  (e.g.
  Flibber is integrated with both Flocker and Noodles which covers
virtualization for 80% of cloud users. So, our small number of "users" actually
represents very wide usage across the ecosystem since every virtual instance uses
Flibber encryption by default.)-->

## Security issue resolution

### Responsible Disclosures Process

<!--- A outline of the project's responsible
  disclosures process should suspected security issues, incidents, or
vulnerabilities be discovered both external and internal to the project. The
outline should discuss communication methods/strategies.-->

### Vulnerability Response Process

<!---Who is responsible for responding to a
    report. What is the reporting process? How would you respond?-->

### Incident Response

<!--A description of the defined procedures for triage,
  confirmation, notification of vulnerability or security incident, and
patching/update availability.--->

## Appendix

<!---* Known Issues Over Time. List or summarize statistics of past vulnerabilities
  with links. If none have been reported, provide data, if any, about your track
record in catching issues in code review or automated testing.-->

### [Open SSF Best Practices](https://www.bestpractices.dev/en)

OSCAL Compass is making great progress towards earning OpenSSF Best Practices badges across all repositories!
🚀 The team has focused on the most mature components, and we are excited to share that Trestle has already met the passing level criteria!
✅ We're on track to achieve full compliance soon! 🎯

<!---* Case Studies. Provide context for reviewers by detailing 2-3 scenarios of
  real-world use cases.
* Related Projects / Vendors. Reflect on times prospective users have asked
  about the differences between your project and projectX. Reviewers will have
the same question.-->
