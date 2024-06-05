# Proposal Process

This document outlines the how to propose large scale or architectural project changes in the OSCAL Compass organization.

> Note: This is a draft process

# When to use this process

On many occassions, ideas for new functionality or upgrades can be brought forth in a GitHub issue or dicussion concerning the project. These suggestions are publicly discussed among maintainers, contributors, users, and other concerned stakeholders. Once an agreement is reached among participants, the proposed alterations move through the pull request process, during which the implementation specifics are examined, approved, or rejected by maintainers.

Some change may be larger in scale or affect multplie projects. For changes such as these, we ask for a change proposal process be followed
so that all stakeholders can agree before implementation.

An example of a change that would require a proposal:

* New projects or codebases that are not part of an existing project
* API breaking changes that affect more than one codebase
* Impactful UX changes
* Drop capabilities or existing integrations

Examples of changes to handle on the project level:

* Feature requests or bugs affecting a single codebase
* Fixing a flaky test
* Code Refactoring

# How to engage in the process

## Prerequisites

Complete the following steps before creating a change proposal:

* Circulate your idea within the community to see if there is interest
* Optionally, create a prototype in your own fork
* If a new project or codebase is proposed, identify project maintainers

## Process 

* Submit a change proposal under `proposals` by opening a pull request. A proposal template with be created in the future.
* At least two maintainers have to approve the proposal before it can be merged.
* Once merged, the proposal may be implemented in target project(s). The progress could be tracked using the pull request number from the merged proposal.