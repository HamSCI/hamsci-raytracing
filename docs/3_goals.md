---
layout: page
title: Goals
permalink: /goals/
mermaid: true
---
## Goals
{:.no_toc}

## Table of Contents 
{:.no_toc}
* TOC
{:toc}

## Research Objectives

1. **Developing a 3D HF Ray-Tracing Toolkit**: Implement a 3D HF ray-tracing engine natively in
   Python, based on the Jones & Stephenson ray-tracing formulation, enabling accurate modeling of
   HF propagation through complex ionospheric conditions and understudied off-great-circle paths
   such as side-scatter.
2. **Validating Ionospheric Models with Empirical Data**: Use observational HamSCI data with 3D
   ray-tracing to validate ionospheric models, and provide feedback to model developers,
   particularly on the bottomside ionosphere.
3. **Simulating HF Response to Critical Ionospheric Phenomena**: Focus on Equatorial Plasma
   Bubbles (EPBs) and quantify their effects on HF communication reliability, bridging
   research-to-operations (R2O) gaps in predicting space-weather-induced HF disruptions.
4. **Enhancing Accessibility and Usability**: Provide comprehensive documentation and tutorials
   to enable broad adoption by the public.
5. **Fostering Public Engagement**: Host bi-weekly online seminars for citizen scientists to
   train users, help them set up their own research problems, and gather real-world feedback.

## Work Plan

Adapted from the funded NASA proposal's work plan (subject to change as the project proceeds).
Two things have changed since the proposal was written:

- **Official period of performance**: **February 2026 – January 2029**, a uniform 5-month shift
  from the proposal's nominal September 2025 – August 2028. The dates below reflect this official
  schedule. In practice, active work did not begin until **mid-May 2026** (a further ~3-month
  slip) because of the PI's leave — but the official end date, January 2029, has **not** changed.
  That means the remaining milestones below represent the plan of record, not a re-planned
  schedule compressed to fit the shorter practical working time; they will be revised here as the
  team re-prioritizes to still target the January 2029 end date.
- **Approach to Objective 1**: some milestones still describe the proposal's original
  PyLap/PHaRLAP-extension approach; the toolkit is now implemented natively in Python instead
  (see [About]({{ '/about/' | relative_url }})).

| Date | Milestone |
| --- | --- |
| February 2026 | Develop open-source core computational engine. |
| April 2026 | Start bi-weekly seminars and collect feedback from citizen scientists. |
| May 2026 | Process and analyze HamSCI data for integration. |
| September 2026 | Prepare ionospheric model outputs to meet ray-tracing requirements for model validation and for generating anomalous HF propagation. |
| January 2027 | Integrate the new core engine with the existing 2D PyLap and test. |
| April 2027 | Develop 3D functionality and conduct initial testing. |
| July 2027 | Integrate the new core engine with 3D functionality and conduct comprehensive testing. |
| August 2027 | Integrate ionospheric model outputs into 3D ray-tracing. |
| September 2027 | Study understudied off-great-circle propagation and document findings. |
| November 2027 | Study EPBs' effect on anomalous HF propagation and refine the toolkit. |
| February 2028 | Begin toolkit packaging and testing. |
| July 2028 | Complete toolkit packaging and finalize tests. |
| August 2028 | Validate ionospheric models against HamSCI data. |
| September 2028 | Create tutorial based on feedback from bi-weekly seminars. |
| November 2028 | Finalize examples and comprehensive documentation for the toolkit. |
| **January 2029** | Complete project report and disseminate findings — official award end date. |
