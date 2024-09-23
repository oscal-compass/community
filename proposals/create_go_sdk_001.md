---
title: Create Go SDK
x-trestle-template-version: 0.0.1
authors:
- jpower432
description: New project - Go SDK and OSCAL API (vote required)
begin-design-discussions: 2024-09-19
status: accepted #deferred, rejected, withdrawn or replaced - PR's are not accepted. Status is based on main. Rejected is unlikely to exist except where a clear record is required 
---

**Checklist**


<!--> Add extra fields for management here <!-->

- [X] Template passes validation with `trestle`
- [X] Proposal cuts across multiple `oscal-compass` projects

## Summary/Abstract

This proposal outlines the development of an OSCAL Go SDK. The primary objective is to expand OSCAL adoption and project integrations within the Go development community.

Benefits:

**Simplified Integration**: Streamline the process of incorporating OSCAL capabilities into cloud-native applications.  
**Leveraging Go's Strengths**: Utilize Go's performance, concurrency, and ecosystem to build a robust and efficient SDK.  

## Background

### Motivation and problem space

**Support Cloud-Native Development**: Expand integration options with cloud-native applications by providing an SDK in Go, a language commonly used in this space.  
**Multi-Language OSCAL Compass Support**: Address the need in OSCAL Compass existing projects for OSCAL SDKs in both Python (existing) and Go (proposed).  

### Impact and desired outcome

Desired outcomes include
- A high-quality, efficient, and flexible Go OSCAL SDK.
- Increased adoption of OSCAL in Go projects.

### Prior discussion and links

Prior discussion on this topic was captured in the following meetings and issues:

- [Proposal Issue 68](https://github.com/oscal-compass/community/pull/68)
- [September 10th OSCAL Compass Community meeting](https://www.youtube.com/watch?v=flFozzcYFzE)

## User/User Story (Optional)

As a developer, I want to create custom APIs that interact with OSCAL content so that I can build tailored security applications for specific use cases.
As a security engineer, I want to integrate OSCAL with my automation tool so that I can automate security tasks based on the defined security controls.

## Goals

**Native Go implementation**: Create a purely Go-based OSCAL SDK.  

## Non-Goals

**Extensive feature parity**: While aiming for functional parity, it's not guaranteed that the Go SDK will have all the exact features of the Python SDK.

## Proposal

This proposal advocates for a single repository containing a `go-sdk` implemented entirely in Go. Porting the Python SDK directly to Go is not recommended due to potential limitations explored below.

## Design Details

The SDK will consist of two key components:

`core-library` (may be imported from an existing Go library):
- OSCAL data types and core logic
- Import or define functionalities for OSCAL document validation and parsing

`go-sdk`:
- High-level OSCAL transformations and normalized workflows (e.g. OSCAL profile Resolution)
- Inheritance and leveraged authorization workflows
- Validation and transformation for OSCAL fragments

### Native Go SDK vs. Go Bindings

While Go bindings offer a faster initial implementation path, they may introduce limitations:

**Python Runtime Dependency**: Using Go bindings would necessitate installing Python and the compliance-trestle library, increasing usage complexity.  
**Performance Overhead**: Python is generally slower than Go, especially for computationally intensive tasks. Calling Python code from Go can introduce significant performance overhead, especially if the Python code is executed frequently.  

## Impacts / Key Questions

### Pros

**Enhanced developer experience**: Provides a native Go SDK, making it easier for Go developers to integrate OSCAL into their projects.     
**Stronger community support**: Attracts a wider developer base and fosters collaboration within the Go community.  
**Alignment with cloud-native trends**: Positions OSCAL Compass as a more accessible solution for cloud-native applications.  

### Cons

**Initial development effort**: Creating a new SDK requires significant upfront development time and resources.  
**Potential for divergence**: Maintaining parity with the Python SDK could be challenging over time.  

## Risks and Mitigations

**Risk**: The Go SDK functionality could diverge from the Python SDK.  
**Mitigation**: Implement a community design proposal process for functional changes to either SDK which would result in new test cases.

### Security Considerations

Security considerations will be addressed throughout the development process to ensure the SDK adheres to best practices for security in Go applications.

## Future Milestones (Optional)

None

## Implementation Details (Optional) 

### Testing Plan

The below testing approach would be done in conjunction with [Proposal Issue 68](https://github.com/oscal-compass/community/pull/68) and [Proposal Issue 61](https://github.com/oscal-compass/community/pull/61).

> Note: While the `testinfra` is being built out, we can prototype with the Python SDK to validate ideas and design feasibility.

1. Define high level workflows that we want each SDK to be able to perform.
2. Develop an approach for conformance testing. This could be writing test cases with Python or using something like [Cucumber](https://cucumber.io/).
   1. The testing could be delivered as a pre-built GitHub Action or git submodules could be used.
   2. Each SDK could implement a CLI wrapper for testing purposes.
   3. Validation of OSCAL outputs and perform `oscal-cli` testing should be completed where applicable.
3. Create a common `testinfra` repository to store centralized test data, common OSCAL schemas, and conformance testing.
   1. A proposal to support new OSCAL versions in OSCAL Compass can be captured here and releases can
   be coordinated to ensure we maintain project compatibility across the organization.

### Update/Rollback Compatibility

This is a proposal for a new project so this section is not applicable.

### Scalability

This proposal will address scaling in terms of code maintenance as this advocates for the management of
multi-language SDKs. To note, multi-language SDKs are a common pattern both within and outside the cloud-native space.

Below are some strategies to managed this:
- As is done with `compliance-trestle` currently, using code generation for OSCAL data types and centrally managed OSCAL schemas for the organization.
- Developing cross-language test cases and test data for functional testing to ensure consistency.

### Implementation Phases/History

Following proposal approval, the development process will involve:

**Research & Exploration**: Identifying existing Go libraries for OSCAL data types and low-level functionalities.
> Note: [`go-oscal`](https://github.com/defenseunicorns/go-oscal) candidate library to explore.

**SDK Design**: Defining common SDK interfaces and developing cross-language test cases.
**Implementation & Documentation**: Building the Go SDK followed by comprehensive documentation creation.   
**Feedback & Testing**: Facilitating a period for community feedback and rigorous testing of the SDK.   