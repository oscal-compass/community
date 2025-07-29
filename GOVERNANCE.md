# OSCAL Compass Governance

The following document outlines how the OSCAL Compass project governance operates.

## Principles

The OSCAL Compass community adheres to the following principles:

**Open**: OSCAL-Compass is open source. See project guidelines [here](./CONTRIBUTING.md).  
**Welcoming and respectful**: See [Code of Conduct](./CODE_OF_CONDUCT.md).  
**Transparent and accessible**: Work and collaboration should be done in public.  
**Merit**: Ideas and contributions are accepted according to their technical merit and alignment with project objectives, scope, and design principles. See our design proposal [process](./proposals/README.md)  

## Governance Structure Overview

The OSCAL Compass Project has a two-level governance structure with an Oversight Committee (across all projects) and Project Maintainers (individual projects). The oversight committee members are also known as **core maintainers** of the OSCAL-Compass project and only they would be included in the CNCF maintainers list for OSCAL-Compass.

Except where otherwise noted, decisions should always start at the most local level of project governance. If a decision only affects a single project, the discussion should start with the project maintainers. While communication between the different project teams is important as they are all interconnected, minor decisions do not need organization-wide consensus and can be moved forward at the project level.

In case of any conflict between the decision of the oversight committee and that of individual projects, the decision of the oversight committee will be binding.

### Project Maintainers overview

Project Maintainers focus on a single codebase or a group of related codebases. They are responsible for activities surrounding the development and release of code, the operation of any services that they own, or the tasks needed to execute their project. Technical decisions for code reside with the project Maintainers unless there is a decision related to multiple maintainer groups that cannot be resolved by those groups. Those cases can be escalated to the Oversight Committee.

More information about the Maintainer and other project roles can be found in the [Membership](./MEMBERSHIP.md) document. The list of current maintainers for each project can be found in the `MAINTAINERS.md` at the repository level.

### OSCAL Compass 'core' and 'non-core' projects

OSCAL-Compass subprojects are divided into two types: **core** and **non-core**. The core projects are the main code-bases of the OSCAL-Compass project that provide the main functionality of OSCAL-Compass and have to follow a proper maintenance and release process, whereas non-core projects are for demos, documentation, and other purposes. There are currently 3 sets of core projects - **compliance-trestle**, **agile-authoring**, and **compliance-to-policy (C2P)**. Rest all are considered non-core projects unless explicitly included in the core projects list.

Non-core projects have a strong affiliation with the core projects, but they are not required for the functionality of OSCAL-Compass. 

New **core** and **non-core projects** can be added by opening an issue to OSCAL-Compass community reporsitory. After discussions in the oversight committee meeting a vote for inclusion will be called. Core projects can be added only with 2/3 majority, whereas non-core projects can be added with a simple majority of the oversight committee as described below in the voting process.

Changing the status of a project from non-core to core, or core to non-core will require a 2/3 majority of the oversight committee.

## OSCAL Compass Oversight Committee Overview

The Oversight Committee functions as the core maintainer for the OSCAL-Compass organization.

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

### Oversight Committee Chairs

The Oversight Committee will also consist of two selected Chair members who will share committee facilitation responsibilities and call meetings. These meetings can be public or private at the discretion of the Oversight Committee.

The Chairs are expected to perform a variety of functions to support Oversight Committee activities:

- Support onboarding new committee members as needed
- Gathering agenda items for meetings
- Scheduling and facilitating Oversight Committee meetings
- Extending discussion via asynchronous communication to be inclusive of members who cannot attend a specific meeting time
- Facilitating the creation and execution of Oversight Committee activities

The term of the chairs is one year. Every year the oversight committee members will select 2 new chairs from amongst them either through consensus or through voting (if required). To ensure diversity, both chairs should not be from the same company/organization unless there is no other nomination.

### Stepping down policy

Life priorities, interests, and passions can change. If you're an oversight committee member but feel you must remove yourself from the list, inform other members that you intend to step down.

After you've informed other members, create a pull request to remove yourself from the MAINTAINERS file. The outgoing member will be added to Emeritus list.

### Handling inactive oversight committee members

To be considered an _active_ Oversight Committee member, individuals are expected to be consistently engaged in the duties of the committee. Active participation includes, but is not limited to:

* Regularly attending Oversight Committee meetings.
* Actively participating in committee discussions and voting on proposals.
* Helping to maintain the mission, vision, and scope of the project.
* Mentoring other contributors and helping to grow the community.

The process for moving an inactive member to **Emeritus** status is as follows:

* Grace Period: If a member is unable to maintain active participation for a consecutive period of **3 months**, a Committee Chair will reach out privately to check in with them. Based on the outcome of the discussion, the member may choose to remove themselves from the MAINTAINERS file, as noted above in the "Stepping down policy" section. 
* Vote: If the member remains inactive for another month or cannot be reached, a vote may be called. This requires a 2/3 majority vote from the other active members (excluding the member being voted out).
* Offboarding: If the vote passes, a pull request will be opened by another member to remove the individual from the `MAINTAINERS.md` file. Following the merge of the pull request, their privileged access to resources will be revoked. They will be considered an **Emeritus Oversight Committee Members** and are welcome to become active again by following the standard nomination process.
* In such cases, the vacancy will be filled according to the procedures outlined in this document.

## Oversight Committee Succession Procedures

The OSCAL Compass project will hold yearly elections to vote for new members of the Oversight Committee.

### Election Process

The election process is as follows:

1. **Voter Eligibility**: Only current oversight comittee members at the time of the election are eligible to vote.
2. **Call for Nominations**: One month before the election, a call for nominations will be sent out to the OSCAL Compass community.
3. **Nomination Period**: Community members will have one month to nominate candidates for the Oversight Committee. Self-nominations are permitted.
5. **Candidate Statements**: Each candidate will be asked to provide a statement of interest and qualifications.
6. **Vetting**: There is usually a process for the existing committee or another body to review the nominations and confirm that the candidates meet the eligibility criteria.
7. **Voting Period**: A two-week voting period will be held.
8. **Results**: The results of the election will be announced within one week of the close of voting.
9. **Voting Process and Tie-Breaking**: Each voter will be eligible to specify upto N candidates (where N is the number of vacant positions). A ranked list of candidates (based on number of votes received) will be created. In the event of a tie for the last seat(s), a revoting would be done for selection amongst those candidates only.

#### Candidate Eligibility

Key Eligibility Requirements:

* **Required**: The candidate must either be a current or a past (emeritus) oversight commitee member, or current maintainer of any **core** project to be eligibile to be nominated for oversight committee member.
* Technical Expertise: Candidates should be senior, respected technical contributors with significant experience relevant to the project's domain.
* Demonstrated Commitment: They must have the time and willingness to actively participate in meetings, discussions, and the work of the committee.
* Neutrality and Project-First Mindset: A crucial requirement is the ability to act as a neutral party, prioritizing the good of the project over any personal or company interests.
* Good Standing: Candidates should have a clean record with respect to the project's Code of Conduct. The CNCF, for example, requires that candidates for its Code of Conduct Committee have no violations in the past 18 months.

### Term Length

Members of the Oversight Committee will serve a one-year term.

### Company Affiliation

To ensure diversity, no more than 50% of the members employed by the same company may serve on the Oversight Committee simultaneously. If the results of an election would cause this limit to be exceeded, the candidate(s) from the over-represented company with the lowest vote counts will be disqualified, and the seat(s) will be filled by the next highest-voted candidates who do not violate the company representation limit.

### Vacancies

If a seat on the Oversight Committee becomes vacant, the committee may appoint a replacement to serve until the next election.

## Decision Making Process

Generally, there are two methods for decision making for the OSCAL Compass project: by consensus or by explicit voting.

### Consensus

Many of the day-to-day project maintenance can be done through the lazy consensus model. This means that any decision is considered supported by the team making it so long as no one objects. Silence on any consensus decision is implicit agreement. Please note that decisions that warrant wider input should be made public by using the defined [proposal process](./proposals/README.md).

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
- For a vote to pass a majority or supermajority (as the case may be) of oversight committee members should vote in favour. Abstaining from voting means a negative vote.

##### Simple Majority Vote

If a vote is called, the default is a simple majority vote - more than half of the appropriate deciding body. This is the default profile used when calling a vote with `/vote`

##### Supermajority Vote

In some cases, a supermajority vote is required for decision making - at least two-thirds of the appropriate deciding body. You can use `/vote-super` to initiate this type of vote.

Some examples include:

* Carrying out [Code of Conduct](https://oscal-compass.github.io/compliance-trestle/mkdocs_code_of_conduct/) decisions requiring severe censure (supermajority of the Oversight Committee)
* Removing an [oversight committee member or a project maintainer](./MAINTAINERS.md) for any reason (supermajority of the Oversight Committee)
* Non-trivial changes to the governance (this document) (supermajority of the Oversight Committee)
* Licensing and intellectual property changes such as new logos or wordmarks (majority of the Oversight Committee)
* Adding, archiving, or deleting **core** projects (supermajority of the Oversight Committee)
* Adding, archiving, or deleting **non-core** projects (majority of the Oversight Committee)

## Modifications to this Governance

This governance may be modified by a supermajority vote of the Oversight Committee.

Trivial changes that do not introduce policy changes may be approved by two members of the Oversight Committee.

## Acknowledgements

Sections of this document were adapted from [InstructLab](https://github.com/instructlab/community/blob/main/GOVERNANCE.md) and [CoreDNS](https://github.com/coredns/coredns/blob/master/GOVERNANCE.md) projects.
