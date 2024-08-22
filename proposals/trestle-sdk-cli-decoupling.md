---
title: Decouple the trestle SDK from the CLI
x-trestle-template-version: 0.0.1
authors:
  - jpower432
description: TBD
begin-design-discussions: 2024-08-22 #Insert
status: accepted #deferred, rejected, withdrawn or replaced - PR's are not accepted. Status is based on main. Rejected is unlikely to exist except where a clear record is required 
---

**Checklist**


<!--> Add extra fields for management here <!-->

- [X] Template passes validation with `trestle`
- [X] Proposal cuts across multiple `oscal-compass` projects


## Summary/Abstract

This proposal outlines the rationale and steps for moving the `trestle` SDK from its current location within the CLI repository to a dedicated, standalone repository and separately managed Python package.

## Background

### Motivation and problem space

- **Community and Ecosystem**: There is no clear separation in `compliance-trestle` between what is designed as part of the `trestle` SDK and what directly supports CLI operations outside of the [`repository.py`](https://github.com/oscal-compass/compliance-trestle/blob/develop/trestle/core/repository.py). This can make it difficult to quickly identify and contribute to reusable logic which can limit adoption and growth.

- **Versioning Misalignment**: Updates to one component can introduce breaking changes for the other, making it difficult to maintain compatibility and avoid regressions.

- **Conflicting Dependencies**: When both the SDK and CLI share a common repository and Python package, they must use compatible versions of dependencies. This can lead to conflicts and limitations in the flexibility of both components. For instance, pinning dependencies for the CLI can provide stability but can limit flexibility and compatibility with different environments and applications for the SDK.

- **Scalability**: Managing the SDK in a separate repository would make it more straightforward to add new SDKs for other languages.

### Impact and desired outcome

**Improved Maintainability**: By reducing complexity and streamlining updates, the separation can make it easier to maintain and support both components.

**Increased Support for SDK Users**: Independent development and testing can lead to enhanced documentation and code quality targeting the SDK user.

## User/User Story (Optional)

None

### Prior discussion and links

Initial discussion occurred in the OSCAL Compass [community meeting](https://www.youtube.com/watch?v=uUGv3HXlTrI&t=19s  ) on June 14, 2024 pertaining to the reusability of `Rule` logic to support this [issue](https://github.com/oscal-compass/compliance-trestle/issues/1475). An [issue](https://github.com/oscal-compass/community/issues/28) in the community repo was subsequently submitted.

## Goals

- `compliance-trestle` continues to contain the `trestle` CLI logic
- `compliance-trestle-python` is created as the Python SDK repository
- `compliance-trestle` and other OSCAL Compass project migration importing the SDK from the new python

## Non-Goals

- Fundamentally changing the architecture or design of the SDK or CLI is out of scope.
- Expanding the SDK to other programming languages is out of scope (future consideration).

## Proposal

> TODO

*This is where we get down to the specifics of what the proposal actually is. It should have enough detail that reviewers can understand exactly what you're proposing, but should not include things like API designs or implementation. This section should expand on the desired outcome and include details on how to measure success.*

## Design Details

> TODO

This section should contain enough information to allow the following to occur:
* potential contributors understand how the feature or change should be implemented
* users or operators understand how the feature of change is expected to function and interact with other components of the project
* users or operators can take action to pre-plan any needed changes within their architecture that impacted by the upcoming feature or change if it's approved for implementation
* decisions or opinions on a specific approach are fully discussed and explained
* users, operators, and contributors can gain a comprehensive understanding of compatibility of the feature or change with past releases of the project.

This may include API specs (though not always required), code snippets, data flow diagrams, sequence diagrams, etc. 

If there's any ambiguity about HOW your proposal will be implemented, this is the place to discuss them. This can also be combined with the proposal section above. It should also address how the solution is backward compatible and how to deal with these incompatibilities, possibly with defaulting or migrations. It may be useful to refer back to the goals and non-goals to assist in articulating the "why" behind your approach.

## Impacts / Key Questions

Some of my main questions around this proposal are the following:

- What will the contribution process look like for logic in `trestle`?
- Will the SDK be maintained by the `compliance-trestle` maintainer or by a new set of maintainers?

### Pros

- **Improved maintainability**: Easier to manage and update individual components.
- **Enhanced reusability**: SDK can be used in more applications and simplify contributions.  
- **Reduced risk of breaking changes**: Fewer unintended consequences around codebase changes.

### Cons

- **Increased complexity**: Managing two separate repositories mean more project infrastructure to manage.
- **Initial effort**: Moving the SDK to a new repository requires upfront work.

## Risks and Mitigations

- **User Impact**: Breaking changes and movement will affect current SDK users and this will require community notifications and discussion as well as migration documentation.

### Security Considerations

- **Increased Attack Surface**: Managing more repositories and  distinct codebases can potentially increase the attack surface.

## Future Milestones (Optional)

- Add a Go SDK to better support the C2P Go version and expand potential for integrations in the cloud native space.

## Implementation Details (Optional) 

### Testing Plan

> TODO

### Update/Rollback Compatibility

The `compliance-trestle-python` SDK could be created first to test the rollout and once confirmed that it works as expected, the duplicate logic in `trestle` can removed and a new major version of `trestle` can be released. Version v3 of `compliance-trestle` will be available for users to rollback.

### Scalability

> TODO

*Describe how the design scales, especially how changes API calls, resource usage, or impacts SLI/SLOs.*

### Implementation Phases/History

Implementation details will be tracked in an issue on `compliance-trestle`. This will be linked here once/if accepted.