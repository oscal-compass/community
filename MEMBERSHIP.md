# Community roles and membership

This document outlines the various responsibilities of contributor roles in the OSCAL Compass organization. OSCAL Compass is made up of several projects that are defined as codebases and services with different release cycles, thus the responsibilities for roles are scoped to individual projects. Where applicable for OSCAL Compass overall, contributor status is equal to the highest status that they have on any project.

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

* You have made **multiple contributions** to the project or community. Contributions may include, but are not limited to:
  * Authoring or reviewing PRs on GitHub.
  * Filing or commenting on issues on GitHub.
  * Contributing to community discussion, for example, meetings or on Slack.
* You have been sponsored by **two Maintainers**. **Note the following requirements for sponsors**:
  * Sponsors must have close interactions with the prospective member - e.g. code/design/proposal review, coordinating on issues, etc.
  * One of the sponsors should be from a **core** OSCAL-Compass project.
  * Sponsors must be from multiple member companies to demonstrate integration across community.

If you have met these expectations and wish to become an established member, you can be nominated by a contributor, or you can nominate yourself. To nominate a contributor or yourself:

* Open an issue in the repository of interest detailing contributions to the project so far.
* Ensure that the sponsors are `@mentioned` on the issue.
* Make sure that the list of contributions included is representative of the work on the project.
* Have your sponsoring maintainers reply confirmation of sponsorship: +1

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

* Member for at least **3 months**.
* Primary reviewer or author for at least **5 substantial PRs** to the codebase.
* You have made multiple contributions to the project or community. Contribution may include, but is not limited to:
  * Triaging open issues or PRs.
  * Authoring or reviewing PRs on GitHub.
  * Demonstrating knowledge of the codebase.
  * Participating in design discussions.
  * Contributing to community discussions (e.g. meetings, Slack).
* You have been sponsored by **two Maintainers**. **Note the following requirements for sponsors**:
  * Sponsors must have close interactions with the prospective Reviewer - e.g. code/design/proposal review, coordinating on issues, etc.
  * Sponsors must be from multiple member companies to demonstrate integration across community.
  * One of the sponsor has to be from the same sub-project.
  * With no objections from other maintainers of the same sub-project

Any person who meets the requirements may be nominated by a contributor, including themselves. To nominate a contributor or yourself:

* Open an issue in the repository of interest detailing contributions to the project so far.
* Ensure that the sponsors are `@mentioned` on the issue.
* Make sure that the list of contributions included is representative of the work on the project.
* Have your sponsoring maintainers reply confirmation of sponsorship: +1

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

* You have been a Reviewer for at least **3 months**.
* Primary reviewer or author for at least **10 substantial PRs** to the codebase.
* You have a deep understanding of the technical goals and direction of the project.
* You have a deep understanding of the technical domain of the project.
* You have made sustained contributions to design and direction by:
  * Authoring and reviewing proposals.
  * Initiating, contributing, and resolving discussions, such as emails, Slack, GitHub issues, meetings.
  * Identifying subtle or complex issues in designs and implementation pull requests.
* You have directly contributed to the project through implementation and/or review.
* You have been sponsored by **two Maintainers**. **Note the following requirements for sponsors**:
  * Sponsors must have close interactions with the prospective Maintainer - e.g. code/design/proposal review, coordinating on issues, etc.
  * Sponsors must be from multiple member companies to demonstrate integration across community.
  * One of the sponsor has to be from the same sub-project
  * With no objections from other maintainers of the same sub-project

One of the sponsors should open an pull request in the relevant repository to add the nominee to the `MAINTAINERS.md` file and add relevant details per the requirements.

Maintainers will vote publicly on the pull request, expressing their support via a GitHub comment or emoji reaction to the nomination summary. Any concerns may be discussed privately amongst the existing Maintainer team. If feedback needs to be given to the nominee, the sponsor should provide that feedback privately. Upon a decision, the pull request will be merged or closed.

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

## Stepping Down and the Emeritus Process

Life priorities, interests, and passions can change. Contributors can retire and move to _emeritus Maintainers_. If a
contributor needs to step down from their current role, they should inform the appropriate project Maintainers. No vote
is required for a contributor to remove themselves, and any project Maintainer can approve the PR. Maintainers who step
down become emeritus Maintainers.

If a contributor has not been performing the duties of their role for a consecutive period of 12 months, they can be
removed by the appropriate project's Maintainers. Maintainers will make reasonable efforts to contact the absent
contributor.

If an emeritus Maintainer or other retired contributor wants to regain an active role, they can do so by renewing their
contributions, after which they can be re-instated by a decision of the appropriate project's Maintainers.

## Changes to contributor roles

Changes to contributor roles must be approved by a vote of the Oversight Committee or a majority of the current project's Maintainers.

## OSCAL-Compass Ecosystem

OSCAL-Compass also has a 'lab' GitHub organization for incubating new projects and hosting closely related projects from the community. If you are an OSCAL-Compass org member, you are implicitly eligible for membership in the related 'lab' Github org, and can request membership when it becomes relevant, by creating a PR directly or opening an issue against the 'lab' Github org community repo.

However, if you are a member of the 'lab' GitHub org but not of the OSCAL-Compass org, you will need explicit sponsorship for your membership request.

## Acknowledgements

Contributor roles and responsibilities were adapted from InstructLab [contributor roles](https://raw.githubusercontent.com/instructlab/community/main/CONTRIBUTOR_ROLES.md) and [Kubernetes](https://github.com/kubernetes/community/blob/master/community-membership.md).
