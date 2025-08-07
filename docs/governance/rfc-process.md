---
sidebar_label: 'RFC Process'
title: 'RFC (Request for Comments) Process'
draft: true
---

## What is an RFC?

An RFC (Request for Comments) is how we propose, discuss, and decide on significant changes to our platform. This includes, but is not limited to:

* Changes to the project's core architecture.
* The introduction of new, complex features.
* Changes to code conventions or contribution processes.
* Decisions that affect the experience of all users or contributors.

The goal is to have a transparent, public, and collaborative process to guide the project's evolution, leveraging the collective wisdom of the community.

## The Simplified Process

Our process is designed to be agile and is based on the use of **GitHub Issues**.

### Step 1: The Proposal (Opening the RFC)

* Anyone can propose an RFC.
* To do so, you must create a **new Issue on GitHub** using our specific **"RFC Proposal (Request for Comments)"** template.
* The template will guide the author to provide all necessary context:
    * A clear summary of the proposal.
    * The motivation and the problem it solves.
    * A technical breakdown of the suggested implementation.
    * The alternatives that were considered.
    * Potential drawbacks or risks.

### Step 2: The Discussion

* Once the RFC Issue is opened, it enters a public discussion period. The RFC author should add the `rfc-discussion` label.
* The entire community is encouraged to read the proposal and leave their comments, questions, and suggestions in the Issue itself.
* The RFC author is responsible for answering questions and, if necessary, refining the proposal based on the feedback received.

### Step 3: The Decision

* We do not have a formal committee. The decision is made based on **rough consensus** among the project maintainers after a reasonable discussion period (usually 7 to 14 days).
* If the proposal is accepted, the Issue is marked with the `rfc-accepted` label and closed. Implementation can then begin (usually through one or more Pull Requests that reference the RFC Issue).
* If it is rejected, the Issue is marked as `rfc-rejected`, with a final comment explaining the reasons for the refusal, and it is closed.

This process ensures that all major decisions are well-documented, publicly discussed, and archived on GitHub for future reference.

## RFC States and Labels

To make it easier to visualize and track the lifecycle of a proposal, we use a standardized set of labels on GitHub. Each RFC must always have one (and only one) state label.

Here are the possible states and their meanings:

* **rfc-proposal** (Suggested color: gray ⚪)
    * State: Proposal.
    * Description: This is the initial state of every newly created RFC. It means the proposal has been formalized, but in-depth discussion has not yet begun or is in its early stages.

* **rfc-discussion** (Suggested color: blue 🔵)
    * State: In Discussion.
    * Description: The proposal is actively seeking feedback from the community and maintainers. This is the main period for comments, suggestions, and refinements.

* **rfc-accepted** (Suggested color: green 🟢)
    * State: Accepted.
    * Description: The proposal has been approved after the discussion period and has reached a rough consensus among the maintainers. The RFC is considered "finalized," and implementation can begin.

* **rfc-rejected** (Suggested color: red 🔴)
    * State: Rejected.
    * Description: After discussion, the proposal was declined. A final comment from the maintainers should explain the reasons for the rejection.

* **rfc-withdrawn** (Suggested color: orange 🟠)
    * State: Withdrawn.
    * Description: The original author of the RFC has decided to withdraw the proposal from consideration. This can happen for various reasons, such as a change of mind or finding a better solution.

* **rfc-superseded** (Suggested color: `purple` 🟣)
    * State: Superseded.
    * Description: The proposal has become obsolete because it was replaced by another, more recent, and approved RFC. The issue of the superseding RFC should be referenced.

### Lifecycle Flow
The typical flow of an RFC follows this path:

`rfc-proposal` → `rfc-discussion` → [ `rfc-accepted` | `rfc-rejected` | `rfc-withdrawn` | `rfc-superseded` ]