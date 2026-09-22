# hamsci-wg
A template repository for HamSCI working groups: a website, a place for the group's hardware and
software, and the HamSCI AI governance scaffolding, in one repository.

## [Check out the example site here.](https://hamsci.github.io/hamsci-wg)

This template combines two HamSCI scaffolds, and stays compatible with both:

| Scaffold | Provides |
|---|---|
| This repository | `docs/` (the Jekyll website), `Gemfile`, `.github/workflows/pages.yml`, `hardware/`, `src/` |
| [`HamSCI/ai_project_template`](https://github.com/HamSCI/ai_project_template) | `CLAUDE.md`, `.claude/`, `ai/`, the `.gitignore`, and the issue templates |

The AI files sit outside `docs/` because everything under `docs/` is published to the web.
Otherwise they are the upstream files, so a working group repository can be kept in step with
`ai_project_template` as that template evolves.

# How to Use This Repository

## The website
- [X] Create a new repository using this template.
- [ ] Update docs/_config.yml with information about your working group. You'll need to change where it says "hamsci-wg" to whatever you want the working group's link to be.
- [ ] Populate the docs pages. You can edit their titles or add/delete pages as needed; they will appear on the site in filename order.
- [ ] Edit CITATION.cff file, if you want to be able to cite this repo. If not, delete that file.
- [ ] [Select a license](https://choosealicense.com/non-software/) and add a LICENSE.txt file. Record the same license in `CITATION.cff`.
- [ ] Under Settings>Pages, set this to deploy via Github Actions. (It will run the pages.yml actions already in the repository.)
- [ ] Verify that the documentation pages are published on hamsci.github.io.
- [ ] Optionally, replace the favicons in \docs\assets with favicons related to your working group. These can be generated at https://favicon.io/.
- [ ] To create an archive of the group's work by archiving this repository, [synchronize to a Zenodo repository](https://help.zenodo.org/docs/github/enable-repository/), publish a release, and add DOI badge here.

## The AI scaffolding
- [ ] Read [`ai/GETTING_STARTED.md`](ai/GETTING_STARTED.md) if you are new to Claude Code or to AI-use policy.
- [ ] Fill in the placeholders in `CLAUDE.md`, `ai/ai_usage_log.md`, and `CITATION.cff`. Find them with `grep -rn '{{' --exclude-dir=.git --exclude-dir=docs --exclude-dir=_site --exclude-dir=workflows .` (the `docs/` and `workflows` exclusions matter, because Jekyll and GitHub Actions use the same braces).
- [ ] Clear the existing entries in `ai/ai_usage_log.md`; they belong to the template's own development.
- [ ] Trim the policy tiers in `.claude/rules/ai-governance.md`: delete Tier 2 if no institution governs the work, Tier 3 if the project is unfunded. Tier 1 stays.
- [ ] Prune the optional rule files: `rm .claude/rules/latex-writing.md` if there is no LaTeX, `rm .claude/rules/python-code.md` if there is no Python. Remove the matching lines from `CLAUDE.md`.
- [ ] Delete `ai/GETTING_STARTED.md` once the project is running.

## Finally
- [ ] Change the paragraph above to add a description of your working group, and delete these checklists from the README.

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
