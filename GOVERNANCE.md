# OSCAL Compass Governance

The following document outlines how the OSCAL Compass project governance operates.

## Principles

The OSCAL Compass community adheres to the following principles:

**Open**: OSCAL-Compass is open source. See project guidelines [here](./CONTRIBUTING.md).  
**Welcoming and respectful**: See [Code of Conduct](./CODE_OF_CONDUCT.md).  
**Transparent and accessible**: Work and collaboration should be done in public.  
**Merit**: Ideas and contributions are accepted according to their technical merit and alignment with project objectives, scope, and design principles. See our design proposal [process](./proposals/README.md)  

## Governance Structure Overview

The OSCAL Compass Project has a two-level governance structure with an Oversight Committee and Project Maintainers.

Except where otherwise noted, decisions should always start at the most local level of project governance. If a decision only affects a single project, the discussion should start with the project maintainers. While communication between the different project teams is important as they are all interconnected, minor decisions do not need organization-wide consensus and can be moved forward at the project level.

### Project Maintainers overview

Project Maintainers focus on a single codebase or a group of related codebases. They are responsible for activities surrounding the development and release of code, the operation of any services that they own, or the tasks needed to execute their project. Technical decisions for code reside with the project Maintainers unless there is a decision related to multiple maintainer groups that cannot be resolved by those groups. Those cases can be escalated to the Oversight Committee.

To be considered an _active project Maintainer_, it is required to be associated with at least one active, non-archived project. If only listed on archived projects, they become _emeritus Maintainers_ and are no longer eligible to become an organization Maintainer.

More information about the Maintainer role can be found in the [Membership](./MEMBERSHIP.md) document. The list of current maintainers for each project can be found in the `MAINTAINERS.md` at the repository level.

#### Stepping Down and the Emeritus Process

It is inevitable that people's focuses will change over time. Contributors can retire and move to emeritus Maintainers. If a contributor needs to step down from their current role, they should inform the appropriate project Maintainers. No vote is required for a contributor to remove themselves, and any project Maintainer can approve the PR. Maintainers who step down become emeritus Maintainers.

If a contributor has not been performing the duties of their role for a consecutive period of 12 months, they can be removed by the appropriate project's Maintainers. Maintainers will make reasonable efforts to contact the absent contributor.

If an emeritus Maintainer or other retired contributor wants to regain an active role, they can do so by following the role requirements defined in in the [Membership](./MEMBERSHIP.md) document.

### OSCAL Compass Oversight Committee Overview

The Oversight Committee functions as the organization maintainers.

An initial Oversight Committee was appointed by the founding sponsors of the OSCAL Compass project. This bootstrap committee will serve until the first election of the Oversight Committee using processes and timing as determined by this group. Current Oversight Committee members are defined in the community [MAINTAINERS.md](./MAINTAINERS.md) file.

The Oversight Committee consists of 3 to 7 leaders on the OSCAL Compass project. These members will serve to supervise the overall project and its health.

The Oversight Committee is responsible for the following duties:

* Maintaining the mission, vision, values, and scope of the project
* Refining the governance and charter as needed
* Making project-level decisions, including setting technical policies that apply across all components
* Resolving escalated project decisions when the team responsible is blocked
* Managing the OSCAL Compass brand
* Controlling access to OSCAL Compass assets such as source repositories and hosting
* Deciding what projects are part of the OSCAL Compass project
* Overseeing the resolution and disclosure of security issues
* Managing financial decisions related to the project

The Oversight Committee will also consists of a two selected Chair members who will share committee facilitation responsibilities and call meetings. These meetings can be public or private at the discretion of the Oversight Committee.

#### Oversight Committee Chairs

The Chairs are expected to perform a variety of functions to support Oversight Committee activities:

- Support onboarding new committee members as needed
- Gathering agenda items for meetings
- Scheduling and facilitating Oversight Committee meetings
- Extending discussion via asynchronous communication to be inclusive of members who cannot attend a specific meeting time
- Facilitating the creation and execution of Oversight Committee activities

#### Oversight Committee Succession Procedures

This process is currently being determined by the bootstrap Oversight Committee.

## Decision Making Process

Generally, there are two methods for decision making for the OSCAL Compass project: by consensus or by explicit voting.

### Consensus

Many of the day-to-day project maintenance can be done through the lazy consensus model. This means that any decision is considered supported by the team making it so long as no one objects. Silence on any consensus decision is implicit agreement, and equivalent to explicit agreement. Please note that decisions that warrant wider input should be made public by using the defined [proposal process](./proposals/README.md).

In the event that consensus cannot be reached, a Maintainer can call for a vote on a decision.

### Explicit Voting

The secondary decision-making process is done by explicit voting.

#### Process

We use the [GitVote](https://github.com/cncf/gitvote) bot to streamline our voting efforts.

- Organization-level voting must take place in the community (this repository) repository.
- Only GitHub Issues and Pull Requests are supported.

The GitVote [repository](https://github.com/cncf/gitvote/blob/main/README.md) has additional information on usage.

There are some constant configurations between voting profiles:

- The Oversight Committee members have binding votes in the community repository. All in the community can and are encouraged to participate in the vote, even if their vote is not binding.
- The duration for voting is four weeks with status checks occurring at the two week mark.

##### Simple Majority Vote

If a vote is called, the default is a simple majority vote - more than half of the appropriate deciding body. This is the default profile used when calling a vote with `/vote`

##### Supermajority Vote

In some cases, a supermajority vote is required for decision making - at least two-thirds of the appropriate deciding body. You can use `/vote-super` to initiate this type of vote.

Some examples include:

* Carrying out [Code of Conduct](https://oscal-compass.github.io/compliance-trestle/mkdocs_code_of_conduct/) decisions requiring severe censure (supermajority of the Oversight Committee)
* Removing a [Maintainer](./MAINTAINERS.md) for any reason other than inactivity (supermajority of the Oversight Committee)
* Non-trivial changes to the governance (this document) (supermajority of the Oversight Committee)
* Licensing and intellectual property changes such as new logos or wordmarks (majority of the Oversight Committee)
* Adding, archiving, or removing projects (majority of the Oversight Committee)

## Modifications to this Governance

This governance may be modified by a supermajority vote of the Oversight Committee.

Trivial changes that do not introduce policy changes may be approved by two members of the Oversight Committee.

## Acknowledgements

Sections of this document were adapted from [InstructLab](https://github.com/instructlab/community/blob/main/GOVERNANCE.md) and [CoreDNS](https://github.com/coredns/coredns/blob/master/GOVERNANCE.md) projects.
