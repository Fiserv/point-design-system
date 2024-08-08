# Contribution Model

For a design system (design language and code language) to thrive and scale within a larger product ecosystem, central system team members cannot make all the decisions, design all design, or code all code – especially when dealing with different product demographics and personas.

Do not underestimate the effort to create and run these processes. What follows is an expansion of those ideas to broader considerations needed to serve a diverse design system community.

## Design and code

A system must articulate the expectations and process for submitting code, design, patterns, documentation, or editorial. These processes can usually be accomplished through pull requests, sprints, or backlogs. Therefore, a team should be ready for a diverse contribution like:

- A designer contributes a component/pattern design even though it is not built in the defined code language yet.
- A designer updating/including a new color for charts and visualizations.
- A developer contributes code for a defined component or pattern.
- A developer contributing bug fixes or new language packages.
- A content editor expanding the published work list with 50 additional entries.

## Changes

While contributions come in manage sizes, you can usually classify them as small or large.

### Small changes
Minor changes can include fixing functional, visual, or accessibility defects. They can also include enhancement s for interaction, performance, or browser support. For code, such changes can be submitted as a pull request to a designated branch in the system repository which can be channeled through an internal review process within the team.

### Large changes
Even a simple pull request (PR) can touch upon a system’s architecture, challenging widely applied conventions. These substantial changes can include:

- Alterations to the system’s visual language built into constants woven across manage CSS properties, mixins, and/or components.
- Proposing a new component or pattern.
- Enhancements that require breaking changes to markup and/or script.
- New documentation for concerns not already covered.

In those cases, the centralized/system team members must devote more effort to consider impacts/risks as well as facilitate collaboration and review among contributors.

>[!TIP]
>Distinguish what constitutes a minor change from a substantial change. Deflect larger changes to an established review process.

## Large changes

For more substantial changes, a system must empathize with contributors by offering an easy-to-understand process that does not waste their time. The **Request for Comment (RFC)** workflow process is a good model.

Such a process should step through discussion, proposal, with preliminary work. Larger time should be committed in delivering and reviewing a polished, testing, and acceptable revision. The workflow steps should include:

- **Initial Discussion** – Often casual with the system team and/or the open community. This discussion is usually triggered by a request form or a system critique session.

- **Formal Proposal** – Outlining the contributor, detailed description, rationale, sub-team area (visual style, component, pattern, or other concern), and relationship with ongoing system and product efforts.

- **Triage and Clarification** – Is a period to help triage the request. This is to refine and detail the proposal. The conversation is also an opportunity to educate contributors about related tasks screening the over-ambitious (e.g., quality control, documentation, security, accessibility).

- **Discussion and Consensus** – This period exposes the proposal beyond the contributor and system team into the open community of stakeholders. Common venues can include a system’s governance council, communication channels (e.g., Teams, Slack), agenda items during critique, and discovery meetings with subject matter experts (SME).

- **Approval and Activation** – For the proposal to be fully implemented depends on approval from stakeholders.

- **Implementation** – Should include design system kit, code packages, and documentation.

>[!TIP]
>Have a process, avoid too many steps, separate understanding the change from making the change, and include clear milestones so a contributor sensibly invests their time.

## Requests for comments

The **Request for Comments (RFC)** process is intended to provide a consistent and controlled workflow for changes in the system (e.g., features, components, patterns, code) so that all stakeholders can be confident about the direction of the change.

Manage changes, including bug fixes, documentation improvements can be implemented through a normal pull request workflow. Some changes though are “substantial,” and we ask that these be put through a bit of a design process to produce a consensus among the community of stakeholders and system team.

### When do you need to follow this process?

You should follow this process if you intend to make “substantial” changes to the system. What constitutes a substantial change is evolving based on community norms and varies depending on what part of the system’s anatomy you are proposing to change. This may include:

- Any sematic or syntactic change to the language that is not a bugfix.
- Removing language features, including those that are feature gated.
- Changes to the interface between compilers and libraries – including language items and intrinsic.
- Additions to standards.

Some changes do not require an RFC:

- Rephrasing, reorganizing, refactoring, or otherwise – changing shape does not change meaning.
- Additions that strictly improve objective, numerical quality criteria (e.g., warning removal, speedup, better platform coverage, more parallelism, trap more errors, etc.)
- Additions are only likely to be noticed by another developers-of-pixel, invisible to users-of-pixel.

If you submit a pull request to implement a new feature without going through the RFC process, it may be closed with a polite request to submit an RFC first.

### Before creating an RFC

A hastily proposed RFC can hurt its chances of acceptance. Low quality proposals, proposals for previously rejected features, or those that do not fit into the near-term roadmap, may be quickly rejected, which can be demotivating for the unprepared contributor. Laying some groundwork ahead of the RFC can make the process smoother.

Although there is no single way to prepare for submitting an RFC, it is an innovative idea to pursue feedback from other project developers beforehand, to ascertain that the request may be desirable, and having a consistent impact on the project requires concerted efforts toward consensus-building. The most common preparations for writing and submitting an RFC include discussing the topic on developer and designer communication channels (e.g., Slack, Teams), and occasionally posting non-formal RFC through those channels.

Receiving encouraging feedback from veteran project developers and designers in the community is a good indication that the RFC is worth pursuing.

### The process

To get a major feature, component, or pattern to the system, the RFC must be added to the system’s backlog for sprint planning. At that point, the RFC is active and may be implemented with the goal of eventual inclusion into the system.

1. Fork the RFC repo
2. Copy `0000-template.md` to `text/0000-my-feature.md`. Do not assign an RFC number yet. This will be the PR number will be renamed accordingly if the RFC is accepted.
3. Fill in the RFC. Put care into the details: RFCs that do not present convincing motivation, demonstrate lack of understanding of the design impact, or are disingenuous about the drawbacks or alternatives tend to be poorly received.
4. Submit a pull request. As a pull request the RFC will start receiving design and development feedback from the larger community, and the author should be prepared to revise it in response.
5. Use the issue number of the PR to update your `0000-` prefix to that number.
6. Assign label of the relevant sub-team which will lead to it being triaged in a future meeting and assigned to a member/contributor.
7. Build consensus and integrate feedback. RFCs that have broad support are much more likely to make progress than those that do not receive any comments. Identify stakeholders and obstacles.
8. Internal discussions. The sub-teams will discuss the RFC pull request as much as possible in the comment thread of the pull request itself. Offline discussions will be summarized on the pull request comment thread.
9. RFC changes. RFCs rarely go through the process unchanged, especially as alternatives and drawbacks are shown. You can make edits (big/small) to the RFC to clarify or change the design. Make sure to include changes as new commits to the pull request and leave a comment on the pull request explaining your changes. Specifically, do not squash or rebase commits after they are visible on the pull request.
10.	Motion for final comment. At some point, a member of the sub-team will propose a “motion for final comment period” (FCP), along with a disposition for the RFC `– merge`, close, or postpone. This step is taken when enough of the tradeoffs have been discussed that the sub-team is able to decide. That does not require consensus amongst all participants in the RFC thread (which is usually impossible). However, the argument supporting the disposition on the RFC needs to have already been clearly articulated, and there should not be a strong consensus against that position outside of the sub-team. Sub-team members use their best judgement in taking this step, and the FCP itself ensures there is ample time and notification for stakeholders to push back if it is made prematurely.
11.	Additional or extended discussions. For RFCs with lengthy discussion, the motion to FCP is usually preceded by a summary comment trying to lay out the current state of the discussion and major tradeoffs/points of disagreement.
12.	Sign off. Before entering FCP, all stakeholders of the sub-team must sign off. This is often the point at which many sub-team members first review the RFC in full depth.
13.	Last call. The FCP lasts ten calendar days, so that it is open for at least 5 business days. It is also advertised widely. This way all stakeholders have a chance to lodge any final objections before a decision is reached. In most cases, the FCP is quiet, and the RFC is either merged or closed. However, sometimes substantial new arguments or ideas are raised, the FCP is cancelled, and the RFC goes back into development mode.

### The life cycle

Once an RFC becomes “active” then authors may implement it and submit the features as a pull request to the system repository. Being active is not an approval and still does not mean that the feature will be merged. It does mean that in principle all the major stakeholders have agreed to the feature and are amenable to merging it. The fact that a given RFC has been accepted and is active implies nothing about the priority assigned to its implementation, nor does it imply anything about whether a system developer has been assigned to the task of implementing the feature. While it is not necessary that the author of the RFC also write the implementation, it is by far the most effective way to see an RFC through to completion. Authors should not expect that other project developers will take on responsibility for implementing their accepted feature.

Modifications to active RFCs can be done in follow-up pull requests. We strive to write each RFC in a manner that will reflect the final design of the feature. The process means we cannot expect every merged RFC to reflect the result at the next major release.

In general, once accepted, RFCs should not be changed. Only very minor changes should be submitted as amendments. More substantial changes should be new RFCs, with a note added to the original RFC. Exactly what counts as a “very minor change” is up to the sub-team to decide. Check sub-team specific guidelines for more details.

### Reviewing RFCs

While the RFC pull request is up, the sub-team may schedule meetings with the author and/or relevant stakeholders to discuss the issues in greater detail. In some cases, the topic may be discussed at a sub-team meeting. In either case a summary form for the meeting will be posted back to the RFC pull request.

A sub-team makes final decisions about RFCs after the benefits and drawbacks are well understood. These decisions can be made at any time, but the sub-team will regularly issue decisions. When a decision is made, the RFC pull request will either be merged or closed. If the reasoning is not clear from the discussion in thread, the sub-team will add a comment describing the rationale for the decision.

### Implementing and RFC

Some accepted RFCs represent vital features that need to be implemented right away. Other accepted RFCs can represent features that can wait until some arbitrary developer wants to do the work. Every accepted RFC has an associated issue tracking implementation in the system repository. The associated issue can be assigned a priority via the triage process that the team uses for all issues in the system repository.

The author of an RFC is not obligated to implement it. Of course, the RFC author is welcome to post an implementation for review after the RFC has been accepted. If you are interested in working on the implementation for an active RFC but cannot determine if someone else is already working on it.

### Postponement

Some RFCs pull requests are tagged with the “postponement” label when they are closed. This status is marked as such because we want neither to think about evaluating the proposal nor about implementing the described feature until sometime in the future, and we believe that we can afford to wait until then to do so. Historically, postponed was used to postpone features until after 1.0 postponed pull requests may be re-opened when the time is right. We do not have any formal process for that, you should ask members of the relevant sub-team.

Usually, an RFC pull request marked as postponed has already passed an informal first round of evaluation, namely the round of “do we think we would ever possibly consider making this change, as outlined in the RFC pull request, or some semi-obvious variation of it.” When the answer is “no,” then the appropriate response is to close the RFC, not postpone it.

## Quality

System parts must often be higher quality and more flexible to address a range of concerns. Mature system practices document processes and checklists that can quite intimidate an aspiring contributor. In addition, a contributors’ proposal may trigger requirements they did not consider.

System solutions must be more robust, adhering to conventions that can include:

- Additional states and behaviors.
- Accessibility failures in color contrast or interactivity.
- Considerations across contexts, such as a darker setting or responsiveness.
- Composability in layouts and adjacent to other elements.

Suddenly, an ambitious contributor is overwhelmed by and frustrated with complexity. They may rescind the contribution, slow down, or negotiate with system team members to fill gaps, smooth rough edges, and complete the contribution.

>[!TIP]
>Be prepared for difficult conversations to establish the meticulous quality required. If the contribution has validity. Ask if they are comfortable handing, you the responsibility.

## Documentation

It is the contributor’s job to document their new work, using the system’s tools to meet a certain level of quality. Set expectations that documentation – like design and coding – is incremental. Your system’s threshold for “good enough” documentation is lower. Offer templates (e.g., MS Word) and system documentation editorial guide to improve authoring efficiency and quality.

>[!TIP]
>Make good documentation a required part of the contribution process, even if a more well-trained system team member does much of the work. Offer predictable models for building variations and authoring doc to smooth the process and get the most out of your contributors.

## Normalize contributions

With so many contributions, it is up to the system team to ensure they blend well. There is often a normal step - whether design, code, documentation, or artifacts from other disciplines – that follows to clean up the contribution. Other times, that normalization crops up as realizations after the fact.

>[!TIP]
>Live with the reality that core members are responsible for maintaining an internally consistent system, and that curation takes effort. Your community appreciates you for it!

## Celebrate success

Whether it is a new icon or a complex pattern, every person I have met derives an intrinsic reward for doing something that mattered. It matters much more to them when a system practice recognizes their efforts. Here are some ideas on how to recognize contributors:

- A documentation page byline identifying authors.
- A system email release announcement with a section elaborating on special contributions.
- A release history denoting authors for each line item.
- Empowering contributors to demonstrate their own work during brown bags and town halls.
- Promotion to owning a “segment” concern, becoming the point person for a topical area.







