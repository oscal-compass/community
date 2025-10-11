# Community roles and membership

This document outlines the various responsibilities of contributor roles in the OSCAL Compass organization. OSCAL Compass is made up of several projects that are defined as codebases and services with different release cycles, thus the responsibilities for roles are scope to individual projects. Where applicable for OSCAL Compass overall, contributor status is equal to the highest status that they have on any project.

This document outlines a core number of contributor roles for OSCAL Compass projects, such as _Member_, _Reviewer_, and _Maintainer_. An _Oversight Committee_ also serves to supervise the overall OSCAL Compass project and its health. Using transparent criteria, the journey between roles is based on individual participation. Criteria will be reevaluated periodically to ensure that we can meet the needs of each project with the resources available to contribute.

OSCAL Compass welcomes new contributors. Not all contributors are able to provide sustained contribution, but each contribution is welcome. Established contributors are expected to demonstrate their adherence to the criteria in this document, familiarity with project organization, roles, policies, etc., and technical and/or writing ability. Role-specific expectations, responsibilities, and requirements are explained below.

## Current roles

The following table provides information about the current roles available to the OSCAL Compass project.

| Role       | Responsibilities                             | Requirements                                                  | Defined by                    |
|------------|----------------------------------------------|---------------------------------------------------------------|-------------------------------|
| Member     | Active contributor in the community          | Multiple contributions and sponsored by 2 Maintainers         | OSCAL Compass GitHub org member |
| Reviewer    | Reviews issues and PRs                      | History of issue triage and PR review and sponsored by 2 Maintainers           | OSCAL Compass GitHub Reviewer team member       |
| Maintainer | Sets direction and priorities for a project | Demonstrated responsibility and excellent technical judgement. Nominated and approved by Maintainers team. | OSCAL Compass GitHub Maintainer team member, [CODEOWNERS](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners), and `MAINTAINERS.md` in each project |

### Team to GitHub Permissions

| Role       | GitHub Permissions                           |
|------------|----------------------------------------------|
| Member     | Read                                         |
| Reviewer   | Write with merge restricted by CODEOWNER approval |
| Maintainer | Maintain                                     |

> Note: Each project will require branch protection rule to require CODEOWNER approval for PRs to default branches. In GitHub, this would mean setting the `Require review from Code Owners` in branch protection rule setting.

### Member

Members are active contributors in the community. They can have issues and pull requests (PRs) assigned to them. Members are expected to be active contributors to the community.

#### Member requirements

To become a project Member, you must meet the following requirements:

* You have made multiple contributions to the project or community. Contributions may include, but are not limited to:

  * Authoring or reviewing PRs on GitHub.
  * Filing or commenting on issues on GitHub.
  * Contributing to community discussion, for example, meetings or on Slack.

* You have been sponsored by two Maintainers.

If you have met these expectations and wish to become an established member, you can be nominated by a contributor, or you can nominate yourself. To nominate a contributor or yourself:

* Open an issue in the repository of interest detailing contributions to the project so far.
* Ensure that the sponsors are `@mentioned` on the issue.
* Make sure that the list of contributions included is representative of the work on the project.

#### Member responsibilities and privileges

As a project Member, you have the following responsibilities and privileges:

* You are responsive to issues and the pull requests assigned to them.
* You are an active owner of code that you have contributed, unless ownership is explicitly transferred:
  * You provide code that consistently pass tests.
  * You consistently address bugs or issues that are discovered after code has been accepted.

### Reviewer

Reviewers are knowledgeable about the codebase and are able review code for quality and correctness. They should expect issues and pull requests (PRs) to be assigned to them and respond per community expectations.

#### Reviewer requirements

To become a project Reviewer, you must meet the following requirements:

* You have made multiple contributions to the project or community. Contribution may include, but is not limited to:
  * Triaging open issues or PRs.
  * Authoring or reviewing PRs on GitHub.
  * Demonstrating knowledge of the codebase
  * Participating in design discussions.
  * Contributing to community discussions (e.g. meetings, Slack).

* You have been sponsored by two Maintainers.

Any person who meets the requirements may be nominated by a contributor, including themselves. To nominate a contributor or yourself:

* Open an issue in the repository of interest detailing contributions to the project so far.
* Ensure that the sponsors are `@mentioned` on the issue.
* Make sure that the list of contributions included is representative of the work on the project.

#### Reviewer responsibilities and privileges

As a project Reviewer, you have the following responsibilities and privileges:

* You have the permission to approve and merge a PR with CODEOWNER approval
* You have permission to label issues and PRs.
* You consistently assign, close, and reopen issues or PRs.
* You actively triage issues and PRs with high quality.
* You will be assigned PRs to review in the project.
* You will be assigned issues to investigate in the project.

### Maintainer

Maintainers are first and foremost contributors that have shown they are committed to the long term success of a project. Maintainership is about building trust with the community and being a person that everyone can depend on to make consistent decisions in the best interest of the project.

#### Maintainer requirements

To become a project Maintainer, you must meet the following requirements:

* You have been a Member for at least 1 month.
* You have a deep understanding of the technical goals and direction of the project.
* You have a deep understanding of the technical domain of the project.
* You have made sustained contributions to design and direction by:
  * Authoring and reviewing proposals.
  * Initiating, contributing, and resolving discussions, such as emails, Slack, GitHub issues, meetings.
  * Identifying subtle or complex issues in designs and implementation pull requests.
* You have directly contributed to the project through implementation and/or review.
* You have been sponsored by two Maintainers.

The process for Maintainer nomination can be found in the Maintainer [guidelines](./MAINTAINER_GUIDELINES.md).

#### Maintainer responsibilities and Privileges

As a project Maintainer, you have the following responsibilities and privileges:

* You make and approve technical design decisions.
* You set technical direction and priorities.
* You define milestones and releases.
* You mentor and guide contributors to the project, including mentoring and sponsoring potential Reviewer and Maintainer candidates.
* You ensure the continued health of the project.
* You are responsive to review requests.
* You review assigned PRs that are related to your area of expertise.
* You focus on quality and correctness, including testing code and factoring content.
* You are responsible for project quality control via code reviews.
* You perform adequate test coverage to confidently release.
* The tests that you perform are passing reliably (i.e. not flaky) and are fixed when they fail.
* You ensure that a healthy process for discussion and decision making is in place.
* You work with other Maintainers to maintain the project's overall health and success holistically.
* Unless otherwise specified, you will be provided with permission to merge commits to the project repository branches.

## Changes to contributor roles

Changes to contributor roles must be approved by a vote of the Oversight Committee or a majority of the current project's Maintainers.

## Acknowledgements

Contributor roles and responsibilities were adapted from InstructLab [contributor roles](https://raw.githubusercontent.com/instructlab/community/main/CONTRIBUTOR_ROLES.md)
