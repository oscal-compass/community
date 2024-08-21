# Contributing

First off all, thank you for taking the time to contribute!

The following is a set of guidelines for contributing. These are just guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

## What to know before getting started

### Code of Conduct

This project adheres to a [Code of Conduct](./CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

Please report unacceptable behavior to one of the Code of Conduct [Committee members](./MAINTAINERS.md).

### Related repositories

In addition to this repository, OSCAL Compass has three main repositories:


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

### Merge details for committers:

1. All merges into develop MUST be conducted by a squash-merge
1. All merges from develop into main MUST be done by a merge commit (e.g. preserving the history of commits into the develop branch).
1. Hotfixes into main, not via develop, MUST be done via a squash merge.
1. Merge's into any branch excluding main and develop are at the developers choice.
1. Use of autocommit is encouraged to ensure commit messages and squash vs merge commit are completed properly.

## Legal

### License Headers

Each source file must include a license header for the Apache
Software License 2.0. Using the SPDX format is the simplest approach.
e.g.

```text
# Copyright (c) 2020 The OSCAL Compass Authors. All rights reserved.
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

### Developer's Certificate of Origin

We have tried to make it as easy as possible to make contributions. This applies to how we handle the legal aspects of contribution. 

We use the [Developer's Certificate of Origin 1.1 (DCO)](https://developercertificate.org/) to manage code contributions (the same approach as the Linux® Kernel [community](https://elinux.org/Developer_Certificate_Of_Origin))

The DCO requires developers to sign off each of their commits to certify that they have the right to submit the code to the project and that they agree to license their contribution under the project's open source license.

You can read more about the DCO and its guidelines [here](https://github.com/cncf/foundation/blob/main/dco-guidelines.md).

Note that DCO sign-off is enforced on all repositories by [DCO bot](https://github.com/probot/dco). Commits with a missing sign-off will be required to be rebased with the sign-off statement added before being accepted.

#### How to Sign Off

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