---
title: Dogfooding trestle for OSCAL-compass community proposals
# Description has been added as a header as it's used by site generators to build social previews
description: "This proposal proposes using `trestle author docs` to manage the proposal documents."
---

## Summary 
The OSCAL Compass community proposals are a structured process where there is a desire for a template to guide the process.
This proposal proposes using `trestle author docs` to manage the proposal documents.


## Background
OSCAL Compass is bootstrapping into a wider community effort with multiple stakeholders.
For this a [proposal process](./README.md) has been defined to govern community wide technical changes.

`trestle author docs` and `trestle author folders` were created to allow uses to manage the lifecycle of 'compliance adjacent' documents such as ADRs using the same tooling as `trestle`. 

## Scope
This applies to the process of OSCAL compass community proposals.
It does not apply to templates within any of the projects.

**It should be considered an exemplar for other projects and communities**

## Solution
Use trestle author docs, combined with a github action pipeline, to enforce the structure of the template.
This provides a perfect case to use `trestle` within the community generating more day-to-day user feedback. 

### Reliance on GitHub for metadata

The proposal intends to rely primarily on GitHub for metadata management (authors, approvers etc.).
This is to keep the process as simple as possible.
Future versions may require more extensive metadata.


## Alternatives Considered

### Use a template but do not use trestle 

Simpler for users to get started, however, is a missed opportunity

### Do not even create a template

Harder to provide a consistent experience for the community when creating a proposal.
Having a template forces the community progressively refine what a proposal must answer before it can be accepted.

## Definition of Done

- [ ] Use this *inception* proposal to define a simple template
- [ ] Enforce the use of this template by using `trestle` and a GitHub Actions pipeline
- [ ] Extend the documentation in the [proposals README.md](./README.md) to cover the use of trestle for proposals

## Technical details

This proposal should be accepted and merged first.
Once the proposal has been accepted and merged a PR will be created to enforce the templates with trestle.