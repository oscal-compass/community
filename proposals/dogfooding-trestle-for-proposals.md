---
title: Dogfooding trestle for OSCAL-compass community proposals.
x-trestle-template-version: 0.0.1
description: "This proposal proposes using `trestle author docs` to manage the proposal documents using the CNCF design proposals template"
authors:
  - butler54
begin-design-discussions: 2024-07-31 #Insert
status: accepted #deferred, rejected, withdrawn or replaced - PR's are not accepted. Status is based on main. Rejected is unlikely to exist except where a clear record is required 
---

**Checklist**


<!--> Add extra fields for management here <!-->

- [x] Template passes validation with `trestle`
- [x] Proposal cuts across multiple `oscal-compass` projects



## Summary/Abstract

The OSCAL Compass community proposals are a structured process where there is a desire for a template to guide the process.

This proposal proposes using `trestle author docs` to manage the proposal documents.

## Background

### Motivation and problem space

As OSCAL-compass is maturing as a project there exists the need to develop more substantial processes.
One of the processes is a design proposal process described at a [high level here](./README.md)
There exist many templates for proposals, however, the [CNCF has a template](https://github.com/cncf/project-template/blob/main/DESIGN-PROPOSALS.md) which aligns with the communities goals.

Ensuring rigour in the process can be difficult. The objective is to ensure the templates are followed for all uses.



### Impact and desired outcome

- Using the proposal's process itself to solidify and agree on a template and flush out issues in the pipeline.
- Demonstrate in a practical way the use of trestle itself to the community. 
- Enforce proposal structure and workflow.


### Prior discussion and links

- See the [PR](https://github.com/oscal-compass/community/pull/58/) for the discussion


## User/User Story (Optional)

- As a contributor to the OSCAL-compass community I would like a clear template by which to build proposals

- As a reviewer of proposals I would like to know that I can easily assess whether the proposal has covered all bases.

## Goals

- Use this *inception* proposal to define a simple template
- Enforce the use of this template by using `trestle` and a GitHub Actions pipeline
- Extend the documentation in the [proposals README.md](./README.md) to cover the use of trestle for proposals
- Minimize the authors effort by using GitHub metadata where appropriate.

## Non-Goals

- Apply to individual project issues / design goals
- Be a stand alone demostration of trestle.

## Proposal

Use trestle author docs, combined with a github action pipeline, to enforce the structure of the template.
This provides a perfect case to use `trestle` within the community generating more day-to-day user 
feedback. 

## Design Details

In the case of this proposal the design and implementation are self-contained as it is self-referential.

## Impacts / Key Questions

The proposal is relatively simple.

The biggest question is how much needs to be recorded in the document itself as opposed to being extracted from the history on GitHub (such as approvers).


### Pros

- Alignment with CNCF standards.
- Self-referential demonstration of trestle
- Not inventing a new standard template

### Cons

- The CNCF template is bulky for some scenarios
- There is overhead to new community members by using / mandating trestle.

## Risks and Mitigations

Describe the risks of this proposal and how they can be mitigated. This should be broadly scoped and describe how it will impact the larger ecosystem and potentially adopters of the project; such as if adopters need to immediately update, or support a new port or protocol. It should include drawbacks to the proposed solution. 

### Security Considerations

This proposal relies on the underlying configuration of the underlying GitHub project to maintain security of the process.

The process is not intended for security-related processes such as responsible disclosure.


## Future Milestones (Optional)

None

## Implementation Details (Optional) 

In addition to this pull request:
  
1. GitHub actions will need to be configured.
2. GitHub project configuration should ensure the required reviewers and actions pipelines are required.


### Testing Plan

Post implementation the first proposal which is not authored by this PR's should examine the workflow.


### Update/Rollback Compatibility

None - this is the starting point.

### Scalability

No concerns

### Implementation Phases/History

This is self contained to this PR and is net new capability.
Lifecycle management can be conducted using the ability of `trestle author docs` to support multiple template revisions. 