---
title: Modernisation and standardisation of release management across OSCAL compass
x-trestle-template-version: 0.0.1
authors:
  - butler54
description: TBD
begin-design-discussions: 2024-08-08 #Insert
status: accepted #deferred, rejected, withdrawn or replaced - PR's are not accepted. Status is based on main. Rejected is unlikely to exist except where a clear record is required 
---

**Checklist**


<!--> Add extra fields for management here <!-->

- [x] Template passes validation with `trestle`
- [x] Proposal cuts across multiple `oscal-compass` projects



## Summary/Abstract

OSCAL compass has grown to a number of projects. Today all of these projects are software (not a service) which is being built and distributed via package registries.
CI & release infrastructure has been developed and coded individually over time matching the capabilities of emerging systems. The result has been duplication and variation between projects. In addition to this some aspects, such as the use of `setuptools` are aging.

Here we are proposing to:
1. Rationalize on a modernized set of build configuration and management infrastructure, as much as is realistically possible.
2. Establish a set of common pipelines that are reused. Keeping the code as "DRY" as possible.
3. Continuing to use platforms that are freely available for open source projects. 


## Background

### Motivation and problem space

Today the CI and project release infrastructure is increasingly complex due to: 

1. An external forced march due to version changes in the OSCAL schema
2. Autogeneration tasks within the pipeline related to the schema.
3. Inter-project dependencies (e.g `compliance-trestle` is a dependency of [compliance-trestle-fedramp](https://github.com/oscal-compass/compliance-trestle-fedramp) and []`compliance-to-policy`](https://github.com/oscal-compass/compliance-to-policy).
4. General improvements required to match CNCF and broader industry trends.
5. Each project has built its' own pipelines.
6. Historically `compliance-trestle` restricted the toolset to python. However, this has led to choices who are not best in breed.
7. The pipelines are tightly coupled. The result is changes to the pipelines often induce unnecessary releases.

In addition for this there are two areas where state of the art has evolved significantly:

1. GitHub Actions: `compliance-trestle` was an early adopter of GitHub actions. The result is there are features which could streamline operations which have not been adopted.
2. Python package management: Python has had a number of options for package and release management. This has created multiple approaches and configuration files (`setup.py` vs `setup.cfg` vs `pyproject.toml` vs `yafp` etc.)



### Impact and desired outcome

Oscal compass codebase has common pipelines for CICD. The common pipelines 


### Prior discussion and links

- [Conventional commits](https://www.conventionalcommits.org/en/v1.0.0/)
- []
- []
- []

#### Current related issues

- []()
- []


## User/User Story (Optional)

- As a developer I want to minimize duplicate code in the cicd pipelines
- As a community I want to have consistentcy in CICD behaviour across different pipelines
- As a external contributor I want to be easily be able to run the GitHub actions pipelines
- As a developer I want a single place to configure the project tooling
- 
## Goals

List the desired goal or goals that the design is intended to achieve. These goals can be leveraged to structure and scope the design and discussions and may be reused as the "definition of done" -  the criteria you use to know the implementation of the design has succeeded in accomplishing its goals.

## Non-Goals

This proposal does not want to change the branching or releasing strategy where the teams are hitting a decent cadence.

## Proposal


## Design Details


### Local lintning toolchain (`pre-commit`)





### Python package management and configuration


### CICD

#### Establish common build stages (across languages)

This section should contain enough information to allow the following to occur:
* potential contributors understand how the feature or change should be implemented
* users or operators understand how the feature of change is expected to function and interact with other components of the project
* users or operators can take action to pre-plan any needed changes within their architecture that impacted by the upcoming feature or change if it's approved for implementation
* decisions or opinions on a specific approach are fully discussed and explained
* users, operators, and contributors can gain a comprehensive understanding of compatibility of the feature or change with past releases of the project.

This may include API specs (though not always required), code snippets, data flow diagrams, sequence diagrams, etc. 

If there's any ambiguity about HOW your proposal will be implemented, this is the place to discuss them. This can also be combined with the proposal section above. It should also address how the solution is backward compatible and how to deal with these incompatibilities, possibly with defaulting or migrations. It may be useful to refer back to the goals and non-goals to assist in articulating the "why" behind your approach.

## Impacts / Key Questions

List crucial impacts and key questions, some of which may still be open. They likely require discussion and are required to understand the trade-offs of the design. During the lifecycle of a design proposal, discussion on design aspects can be moved into this section. After reading through this section, it should be possible to understand any potentially negative or controversial impact of the design. It should also be possible to derive the key design questions: X vs Y.

This will also help people understand the caveats to the proposal, other important details that didn't come across above, and alternatives that could be considered. It can also be a good place to talk about core concepts and how they relate. It can be helpful to explicitly list the pros and cons of each decision. Later, this information can be reused to update project documentation, guides, and Frequently Asked Questions (FAQs).

### Pros

Pros are defined as the benefits and positive aspects of the design as described. It should further reinforce how and why the design meets its goals and intended outcomes. This is a good place to check for any assumptions that have been made in the design.

### Cons
Cons are defined as the negative aspects or disadvantages of the design as described. This section has the potential to capture outstanding challenge areas or future improvements needed for the project and could be referenced in future PRs and issues. This is also a good place to check for any assumptions that have been made in the design.

## Risks and Mitigations

Describe the risks of this proposal and how they can be mitigated. This should be broadly scoped and describe how it will impact the larger ecosystem and potentially adopters of the project; such as if adopters need to immediately update, or support a new port or protocol. It should include drawbacks to the proposed solution. 

### Security Considerations



When attempting to identify security implications of the changes, consider the following questions:
* Does the change alter the permissions or access of users, services, components - this could be an improvement or downgrade or even just a different way of doing it?
* Does the change alter the flow of information, events, and logs stored, processed, or transmitted?
* Does the change increase the 'surface area' exposed - meaning, if an operator of the project or user were to go rogue or be uninformed in its operation, do they have more areas that could be manipulated unfavorably?
* What existing security features, controls, or boundaries would be affected by this change?

This section can also be combined into the one above.


## Future Milestones (Optional)

Currently `oscal compass` is mostly python with some go.
The focus of this proposal is to flush out details on the python ecosystem. 
Parts will need to be extended for the go projects.

## Implementation Details (Optional) 

Some projects may desire to track the implementation details in the design proposal. Some sections may include:

### Testing Plan

Testing CICD is hard without having side effects.
In order to test this it is recommended that a fork is developed including **fully releasing** to a testing pypi project to ensure that, at least for `compliance trestle`, there are no broken releases. 


### Update/Rollback Compatibility

There are three considerations:
1. GitHub actions workflow: This is effectively a hard cut-over for the maintaining team. Once the changes are introduced into develop the changes should be releases as soon as possible to avoid any issues relating to hot fixes.

2. End users (installers): Technically there is no breaking change here. The buildtools which change are for develop time not install time. 

3. Developers: Developers will need to update their environment. Rolling back will be difficult but not impossible.
  
### Scalability

There are no scalability concerns with this approach at this time. 

### Implementation Phases/History

Describe the development and implementation phases planned to break up the work and/or record them here as they occur. Provide enough detail so readers may track the major milestones in the lifecycle of the design proposal and correlate them with issues, PRs, and releases occurring within the project.