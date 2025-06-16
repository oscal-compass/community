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

#### Compliance-to-policy

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

| Component                                       | Applicability     | Description of Importance                                                                                                                                                                                                                                                                                                                   |
| ----------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| OSCAL                                           | Critical          | OSCAL is a NIST framework and language for managing compliance artifacts as code end-to-end. This enables the easy selection and documentation of security controls using compliance-as-code and enables efficient creation of action plans for security remediations and risk mitigation.                                                      |
| Trestle                                         | Critical          | Trestle is an opinionated implementation of the OSCAL standard. It makes sure that the schemas are enforced during the manipulation of OSCAL documents and provides an SDK which means that fewer user re-implementations of common functions are necessary, thereby decreasing the attack surface area.                                    |
| Plugin Architecture Security                    | Critical          | Plugins are built on top of Policy Validation and Enforcement Points (PVPs/PEPs) which either result from Kubernetes resources or internal infrastructure. Such resources are less likely to be vulnerable to security risks.                                                                                                               |
| Git/SCM Infrastructure                          | Critical          | Git and other SCM infrastructures enables the creation of automated workflows when submitting code to a central repository for collaboration. OSCAL serves as the starting point of the automated workflow by declaring security controls as machine-readable code, which enables automated security checks even before manual code review. |
| Agile Authoring                                 | Security Relevant | The Agile Authoring platform enables all involved compliance personnel to orchestrate their individual aspects of the compliance artifacts while ensuring artifacts' consistency and traceability, reducing the risk of outsider manipulation.                                                                                              |
| Plugin Selection/External Command Configuration | Security Relevant | Plugins can be selected based on the needs of the users to strengthen their security controls only when necessary .                                                                                                                                                                                                                         |
| Compliance-to-Policy                            | Security Relevant | Compliance-to-Policy is a GitOps extension which creates a bridge between compliance-as-code and policy-as-code.                                                                                                                                                                                                                            |

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

### Communication Channels

<!--Reference where you document how to reach your team or
  describe in corresponding section.
  * Internal. How do team members communicate with each other?
  * Inbound. How do users or prospective users communicate with the team?
  * Outbound. How do you communicate with your users? (e.g. flibble-announce@
    mailing list)-->

### Ecosystem

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
