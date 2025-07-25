# Maintainers Guidelines

Maintainers are defined in our contributor ladder [documentation](/MEMBERSHIP.md#maintainer). The below documentation describes the Maintainer onboarding and offboarding processes.

## Maintainer Nomination Process

Any person who meets the requirements for the maintainer role may be nominated by a contributor, including themselves. To nominate a contributor or yourself:

1. Secure sponsorship from two existing Maintainers.
2. Open an issue in the repository of interest detailing contributions to the project so far. Make sure that the list of contributions included is representative of the work on the project. Ensure that the sponsors are `@mentioned` on the issue.
3. One of the sponsors should open an pull request in the relevant repository to add the nominee to the `MAINTAINERS.md` file and link the issue as the nomination summary.
4. Maintainers will vote publicly on the pull request, expressing their support via a GitHub comment or emoji reaction to the nomination summary. Any concerns may be discussed privately amongst the existing Maintainer team. If feedback needs to be given to the nominee, the sponsor should provide that feedback privately.
5. Upon a decision, the pull request will be merged or closed. If the pull request is merged, an existing Maintainer with access to the `*-maintainers` [GitHub Team](https://docs.github.com/en/organizations/organizing-members-into-teams/about-teams) will update the role of the new Maintainer. The OSCAL Compass [admins](./MAINTAINERS.md#org-admins) can assist as needed.

## Stepping Down and the Emeritus Process

It is inevitable that people's focuses will change over time. Maintainers may resign from their role at any time. If a contributor needs to step down, they should inform the appropriate project Maintainers, ideally by opening a pull request to remove themselves from the relevant `MAINTAINERS.md` file(s).
No vote is required for a contributor to step down, and any project Maintainer can approve the change.

Maintainers who step down in good standing become **Emeritus Maintainers**. Emeritus Maintainers do not retain elevated privileges or binding votes but are encouraged to remain involved in the community.

If an Emeritus Maintainer or other retired contributor wants to regain an active role, they can do so by following the role requirements defined in the [Membership](./MEMBERSHIP.md) document.

### Maintainer Inactivity

To ensure the project remains healthy and active, Maintainers who have been inactive may be moved to an **Emeritus** status. This process is not punitive but rather a necessary step to keep the project's leadership clear and responsive.

Activity is defined as participation in code reviews, responding to issues, participating in project meetings, or other significant contributions.

The process for moving an inactive Maintainer to **Emeritus** status is as follows:

* Grace Period: If a Maintainer has shown no activity for a consecutive period of **6 months**, another Maintainer will reach out privately to check in with them.
* Vote: If the Maintainer remains inactive or cannot be reached, a vote may be called. This requires a simple majority vote from the other active Maintainers on that specific project.
* Offboarding: If the vote passes, a pull request will be opened to remove the individual from the `MAINTAINERS.md` file. Following the merge of the pull request, their privileged access to project resources will be revoked. They will be considered an **Emeritus Maintainer** and are welcome to become active again by following the standard nomination process.

