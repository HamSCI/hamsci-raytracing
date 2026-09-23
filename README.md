# HamSCI Ray Tracing

HamSCI Ray Tracing is a HamSCI working group for amateur radio operators, citizen scientists,
software developers, and professional researchers interested in HF propagation and ionospheric
science. The group develops and promotes open-source HF ray-tracing tools, validates ionospheric
models using HamSCI observations, and studies space weather and unusual HF propagation
(including Equatorial Plasma Bubbles and off-great-circle/side-scatter paths). It also runs
tutorials, technical discussions, software feedback sessions, and community research projects.

This work is supported by **NASA ROSES 2024 B.21 Heliophysics Citizen Science Investigations
(H-CSI)**, award **80NSSC26K0051**, *"Ionospheric Model Validation and Development of an
Open-Source HF Ray-Tracing Toolkit Leveraging HamSCI Citizen Science Data"* (PI: Kornyanat
Hozumi, University of Scranton).

**Join us**: [Google Group](https://groups.google.com/g/hamsci-ray-tracing?pli=1) ·
bi-weekly meetings, announced on the mailing list ·
[HamSCI working group page](https://hamsci.org/working-group/raytracing-wg)

## [Check out our website here.](https://hamsci.github.io/hamsci-raytracing)

This repository combines two HamSCI scaffolds:

| Scaffold | Provides |
|---|---|
| [`HamSCI/hamsci-wg`](https://github.com/HamSCI/hamsci-wg) | `docs/` (the Jekyll website), `Gemfile`, `.github/workflows/pages.yml`, `hardware/`, `src/` |
| [`HamSCI/ai_project_template`](https://github.com/HamSCI/ai_project_template) | `CLAUDE.md`, `.claude/`, `ai/`, the `.gitignore`, and the issue templates |

The AI files sit outside `docs/` because everything under `docs/` is published to the web.

## Software

The 3D ray-tracing toolkit itself is under active development in the PI's private repository.
Vetted, publishable components will be ported into `src/` as they mature; see
[`src/README.md`](src/README.md). `src/` does not yet contain the toolkit code.

# AI Use in This Working Group

Working group repositories are public, and their websites more so. The governance scaffolding in
`.claude/` and `ai/` makes the following the default:

- **Never fabricate.** No invented citations, data, numbers, callsigns, or attributions.
- **Humans own the science.** A human reviews AI output before it enters an artifact, including
  website copy, and the scientific claims are the authors'.
- **AI is not an author.** Never in an author block, an acknowledgment, or a `CITATION.cff`.
- **Log before you commit.** Every substantive session, in `ai/ai_usage_log.md`, with a real
  timestamp. The `/commit` command in Claude Code does this for you.
- **Disclose AI use in published outputs**, naming the tool and describing what it did.
- **Protect contributors.** Operator personal data, fine-grained station locations, unpublished
  collaborator data, and ITAR/EAR-controlled material never go to an external AI tool. See
  [`.claude/rules/hamsci-data.md`](.claude/rules/hamsci-data.md).

The full policy stack, including the tiers for institutional and funder requirements, is in
[`.claude/rules/ai-governance.md`](.claude/rules/ai-governance.md).

# About HamSCI Working Groups
## What is a working group?
In professional contexts, a working group is a team of experts assembled to tackle a specific problem, develop a deliverable, or execute a project. The group generally follows a specific work plan and disbands once objectives are met.

For HamSCI, working groups are a way to enable researchers and citizen scientists to develop autonomous projects under the HamSCI umbrella. As our group has grown from a small workshop running short campaigns to a large group with numerous projects, it's no longer feasible for HamSCI's central leadership to take an active role in every project. It's also important for us to ensure that HamSCI projects can be led by amateurs, not just full-time scientists.

 

## How can I join a working group?
Visit www.hamsci.org/working-groups and look for one that suits your interests. Depending on the nature of the working group, you may be able to join the mailing list directly, or may need to email the group leader and ask to join.


## How can I propose a working group?
Contact HamSCI leadership with the following required elements:

- [ ] Full title of your working group
- [ ] Official leadership
- [ ] Group mission statement
- [ ] Link to mailing list
- [ ] Meeting information: a Zoom link for a regular meeting, a Google Calendar link, or a string like "Meeting announcements are sent out on mailing list"
- [ ] Group photo (can just be a picture of whatever you're working on; a photo of lightning for a VLF group, for example)

If applicable, consider sending the following items as well: 
- [ ] A science traceability matrix for the group (or a logic model/theory of change, if applicable)
- [ ] A list of DOIs for relevant data repositories (datasets your group has posted to Zenodo, e.g.)
- [ ] A list of DOIs for academic papers associated with your group
- [ ] DOIs/links for posters published by your group
- [ ] Any reference materials or getting-started guides you would like newcomers to become familiar with
- [ ] Any additional materials you would like shared 

## How can I ensure that my working group will be effective?

**Consider your mission.** Some working groups, such as the K-12 Curricular Integration Group, serve as discussion groups for evergreen topics, while others, such as the Thru-Hole Grape Group, have a specific outcome in mind. What would have to happen for your working group to disband?

**Follow the Heilmeier Catechism.** If your working group revolves around a focused project, consider your answers to the questions of the Heilmeier Catechism:

    What are you trying to do? Articulate your objectives using absolutely no jargon.
    How is it done today, and what are the limits of current practice?
    What is new in your approach and why do you think it will be successful?
    Who cares? If you are successful, what difference will it make?
    What are the risks?
    How much will it cost?
    How long will it take?
    What are the mid-term and final “exams” to check for success? 

**Distinguish between outcomes and outputs.** Outcomes, as discussed above, are the goals of your working group: things that occur which would not have occurred if you had not convened and worked together. Outputs are publications, datasets, and products. It's important to record these (we recommend uploading reports and datasets to the HamSCI community on Zenodo) so that others can follow your work and build upon it in the future. For example, if your working group's task is to organize a data campaign, the activity would be the campaign itself, the data collected would be an output, and the scientific analysis of that data would be the outcome.

**Let your meeting schedule suit your group's needs, not the other way around.** You may assume that your working group will be best served by a weekly or biweekly meeting, but this is not always the case. It's perfectly acceptable to set a meeting schedule of "once a year at Hamvention" or "on Zoom as needed." 

Reach out if your project needs resources. Funding to support your project may be available through ARDC, NASA, the National Science Foundation, and other sources. If you would like assistance in applying for funding to support your project, fill out the Heilmeier Catechism above and reach out to HamSCI's full-time scientists. We can help you determine if your project is likely to be funded and navigate the hidden curriculum of applying for a grant.
 

## How does HamSCI leadership ensure that working groups remain effective?

Working group topics must be approved by scientific leadership at HamSCI. (We aren't here to gatekeep; we just want to verify that new topics aren't redundant or pseudoscientific.) Each year at the HamSCI Workshop, we check to verify that all working groups on the books have shown some activity over the previous year. Those which have not will be archived or reorganized. Over time, we track the progress of working groups. 
