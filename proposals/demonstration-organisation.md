---
title: Management of reference demonstration repositories
x-trestle-template-version: 0.0.1
description: "This proposal proposes "
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

OSCAL compass is built on the premise of compliance as code and gitops.
This means that Github repositories, and organisations, are used for demonstrations including integration with CICD platforms such as github actions.
The result is that curating this content is key.
This proposal outlines guidelines and processes for managing demonstration content in a consistent and coherent way.

## Background

Over time there have been a number of demonstrations built for OSCAL compass.
Many of these demonstrations contain overlapping functionality, however, clear ownership has not been maintained.
Most of these demonstrations have not been reviewed at the community level, whether due to historical creation or lack of process.
The result is we do not have a consistent set of project demonstration content.

### Motivation and problem space

- To improve the demonstration content itself.
- To ensure that the primary github organization (e.g. https://github.com/oscal-compass) is a focused and clean as possible. 
  - This will enable the 'core' to meet standards such as OpenSSF more easily
- To ensure a minimum viable set of processes in place to manage the demo content.


### Impact and desired outcome

- Avoiding creating a dumping zone: Organizations which have 100's or 1000's of garbage projects which have been thrown into the wild.
- W

### Prior discussion and links

- Mostly via slack / f2f conversations.


## User/User Story (Optional)

- As an Oscal compass contributor I have a clear process for obtaining and creating 'official' demo repositories
- As an Oscal compass user I have a single place for clear and consistent demonstration content
- As a potential user of Oscal compass the core organization clearly shows the projects 

## Goals

- Use this *inception* proposal to define a simple template
- Enforce the use of this template by using `trestle` and a GitHub Actions pipeline
- Extend the documentation in the [proposals README.md](./README.md) to cover the use of trestle for proposals
- Minimize the authors effort by using GitHub metadata where appropriate.

## Non-Goals

- Demonstrations are not the default for regression tests. Testing should be part of the main project.
- To decide what are the priority demonstrations for oscal-compass

## Proposal

1. Reference demonstrations are not included in the [`oscal-compass`](https://github.com/oscal-compass) organization. Demonstrations are confined the `oscal-compass-demos` organization.
2. Due to the nature of Oscal-compass, demonstrations are likely to span multiple repositories. Each demonstration should at least have a descriptive name which is the root repository of the demonstration that includes documentation: 
   - `https://github.com/oscal-compass-demos/acme-corp-cloud` # An oscal compass demo for 'ACME corps' cloud
   - `https://github.com/oscal-compass-demos/trestle-markdown-rendering` # An oscal compass demo repository for markdown rendering
3. Repository should avoid names which are not readily readable or use unnecessary acronyms , shortened, or not contextualized
   - `https://github.com/oscal-compass-demos/e2e` # Not specific
   - `https://github.com/oscal-compass-demos/ISM` # Bad not everyone knows was the Australian ISM IS
   - `https://github.com/oscal-compass-demos/AUGOVISM` # Hard to decipher / search
   - `https://github.com/oscal-compass-demos/Australian-govt-ISM` # provides sufficient context.
   - `https://github.com/oscal-compass-demos/kubecon-japan-2025` # detailed for an event. 
4. Secondary repositories begin with the name of the demonstration
   - e.g `https://github.com/oscal-compass-demos/acme-corp-cloud-catalog`

5. Demonstration content MUST be stable. 
   - E.g. Owners MUST NOT update the repos under `https://github.com/oscal-compass-demos` in order to run the demo, the demonstration SHOULD be forked.
6. Demonstration repositories can be nominated via an issue in the  [`community`](https://github.com/oscal-compass/community)
   1. Demonstrations MUST have at two maintainers nominated.
   2. The name of the demonstration; a description of the intent of the demonstrations; and the repositories are required
7. Demonstrations MUST be actively maintained to the currently supported versions of `oscal-compass`
8. Demonstrations that are not maintained will either be:
   1. Archived, or
   2. Actively document to user why there are limits (e.g. relies on 3rd party content that leverages an old version of OSCAL).
9.  Demonstrations must include appropriate blerbs and cross linking from:
   1.  Oscal Compass community website
   2.  and optionally project websites (e.g. `compliance-trestle` or `compliance-to-policy`)
10. Event specific demonstrations (e.g. Kubecon) should follow the following practice
    1.  The SHOULD be kept stable with respect to the documentation and videos
    2.  If reused in another event they MUST be renamed with another project name
    3.  If reused and renamed the events it is used at MUST be referenced in the README.md for traceability


## Design Details

Sufficient details are above.

## Impacts / Key Questions

The proposal is relatively simple.

The biggest question is how much needs to be recorded in the document itself as opposed to being extracted from the history on GitHub (such as approvers).


### Pros
- Provides clear guidance to curate demonstrations
- Keeps the core organisation clear
- Provides clear expectations for both demo developers and consumers.
- Provides expectations to demo developers and maintainers of required ongoing efforts.

### Cons

- It's additional overhead from an OSCAL compass organization perspective which carries the risk of being ignored.


## Risks and Mitigations

N/A

### Security Considerations

- Github Actions automation carries risks based on how authorization is performed. This proposal will decrease risk as it isolates demo automation further away from core oscal compass projects.

- The ongoing risk with authoritative demonstrations is that it is a larger body of code and projects 
## Future Milestones (Optional)

None

## Implementation Details (Optional) 

1. Setup the organization via the CNCF with the correct set of permissions.
2. Create a request workflow for new demo repos in the community github organization.
3. (Optional) create a minimum GitHub template, in the demo to provide organizational minimums.
   1. CNCF references and licenses
   2. Minimum Security workflows for actions
   3. Any other standards deemed necessary
4. Identify and move across existing projects. 

### Testing Plan

None

### Update/Rollback Compatibility

The biggest issue is the movement of projects from a URL perspective. Thankfully most of these issues are managed by Github.

### Scalability

No concerns

### Implementation Phases/History

The biggest implementation challenge is (4) above. This will need to be conducted in phases.