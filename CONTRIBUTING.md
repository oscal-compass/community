# Contributing

First off all, thank you for taking the time to contribute!

The following is a set of guidelines for contributing. These are just guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

## What to know before getting started

### Code of Conduct

This project adheres to a [Code of Conduct](./CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

Please report unacceptable behavior to one of the Code of Conduct [Committee members][MAINTAINERS.md].

### Related repositories

In addition to this repository, InstructLab has three related repositories:


* [Trestle](https://github.com/oscal-compass/compliance-trestle) - Command line tool and SDK for interacting with OSCAL-based documents

* [Agile Authoring](https://github.com/oscal-compass/compliance-trestle-agile-authoring) - Ready to use CI/CD pipeline configuration and setup using a GitOps approach with Trestle for OSCAL document management and collaboration.

* [Compliance to Policy](https://github.com/oscal-compass/compliance-to-policy) (aka C2P) - C2P is a GitOps extension as a pluggable bridge to normalize the policy administration in the policy validation tools. Bridge between compliance-as-code and policy-as-code.

The following sections provide a general overview for contributing to any of the OSCAL Compass repositories.

## Contributing overview

Participating in the OSCAL Compass project can come by contributing to any one of the repositories. The following workflow is designed to help you understand contribution best practices, and to help you begin your contribution journey. It will guide you through creating and picking up issues, working through them, having your work reviewed, and then getting your pull request merged.

Help on open source projects is always welcome and there is always something that can be improved. For example, documentation can always use improvement, code can always be clarified, variables or functions can always be renamed or commented on, and there is always a need for more test coverage. If you see something that you think should be fixed, take ownership!

To contribute code or documentation, please submit a pull request to the relevant repository. Note that contribution to any repository has its own set of requirements and expectations, and users should familiarize themselves with those expectations before contributing.

## Getting started with contribution

Our project welcomes external contributions. If you have an itch, please feel
free to scratch it.

To contribute code or documentation, please submit a **pull request** to respective repository.

A good way to familiarize yourself with the codebase and contribution process is
to look for and tackle low-hanging fruit in the **issues** of respective repositories.
Before embarking on a more ambitious contribution, please quickly [get in touch](MAINTAINERS.md) with us.

**Note: We appreciate your effort, and want to avoid a situation where a contribution
requires extensive rework (by you or by us), sits in backlog for a long time, or
cannot be accepted at all!**

We have also adopted [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md).

### Proposing new features

If you would like to implement a new feature, please raise an issue in the respective repository
labelled `enhancement` before sending a pull request so the feature can be discussed. This is to avoid
you wasting your valuable time working on a feature that the project developers
are not interested in accepting into the code base.

### Fixing bugs

If you would like to fix a bug, please raise an issue labelled `bug` before sending a
pull request so it can be tracked.

### Merge approval

The project maintainers use LGTM (Looks Good To Me) in comments on the code
review to indicate acceptance. A change requires LGTMs from one of the maintainers.

For a list of the maintainers, see the [maintainers](MAINTAINERS.md) page.

### Merging and release workflow

OSCAL Compass projects operate on a simple, yet opinionated, method for continuous integration. It's designed to give developers a coherent understanding of the objectives of other past developers.
The criteria for this are below. OSCAL Compass effectively uses a gitflow workflow with one modification: PR's merge into develop are squash merged as one commit.

In the CI environment this results in the following rules:

1. All Commit's *MUST* be signed off with `git commit --signoff` irrespective of the author's affiliation. This ensures all code can be attributed.
   1. This is enforced by DCO bot and can be overrided by maintainers presuming at least one commit is signed-off.
1. All commits *SHOULD* use [conventional commits](https://www.conventionalcommits.org/en/v1.0.0-beta.2/)
   1. This is as github, when only one commit is in a PR, will use the native git commit message as the merge commit title.
      1. When only a single commit is provided the commit MUST be an conventional commit and will be checked the `Lint PR` aciton.
1. All PR's title's MUST be formed as an [convention commit](https://www.conventionalcommits.org/en/v1.0.0-beta.2/)
   1. This is checked by the `Lint PR` action
1. All PR's to `develop` and hotfix PR's to `main` must close at least one issue by [linking the PR to an issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword).
1. Trestle will release on demand the default approach for a hot fix should be to merge into `develop`, followed by releasing to `main`, unless this will release functionality that is not ready.
1. Each feature/fix/chore (PR into develop) be represented by a single commit into develop / main with a coherent title (in the PR).
   1. The trestle preference for doing this is to use squash merge functionality when merging a PR into develop.
1. Developers *MUST* pass the required CI checks for each PR.
1. Developers are encouraged to use GitHub's automated merge process where possible to keep the number of active PR's low.

### Merge details for committers:

1. All merges into develop MUST be conducted by a squash-merge
1. All merges from develop into main MUST be done by a merge commit (e.g. preserving the history of commits into the develop branch).
1. Hotfixes into main, not via develop, MUST be done via a squash merge.
1. Merge's into any branch excluding main and develop are at the developers choice.
1. Use of autocommit is encouraged to ensure commit messages and squash vs merge commit are completed properly.

## Legal

Each source file must include a license header for the Apache
Software License 2.0. Using the SPDX format is the simplest approach.
e.g.

```text
# Copyright (c) 2020 IBM Corp. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     https://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
```

We have tried to make it as easy as possible to make contributions. This
applies to how we handle the legal aspects of contribution. We use the
same approach - the [Developer's Certificate of Origin 1.1 (DCO)](https://oscal-compass.github.io/compliance-trestle/contributing/DCO/) - that the Linux® Kernel [community](https://elinux.org/Developer_Certificate_Of_Origin)
uses to manage code contributions.

We simply ask that when submitting a patch for review, the developer
must include a sign-off statement in the commit message.

Here is an example Signed-off-by line, which indicates that the
submitter accepts the DCO:

```text
Signed-off-by: John Doe <john.doe@example.com>
```

You can include this automatically when you commit a change to your
local git repository using the following command:

```bash
git commit --signoff
```

Note that DCO signoff is enforced by [DCO bot](https://github.com/probot/dco). Missing DCO's will be required to be rebased
with a signed off commit before being accepted.
