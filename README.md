# Adaptive AI Interfaces for Assistive Robotics in Inclusive Agriculture

> **MSc/PhD Research Thesis** — Maynooth University (ARGUS Research & Innovation)

---

## Overview

This repository supports the thesis research project:

**"Adaptive AI Interfaces for Assistive Robotics in Inclusive Agriculture"**

The project investigates how Large Language Models (LLMs) can dynamically adapt robot control interfaces for elderly users in agricultural settings, enabling inclusive and accessible human–robot interaction in greenhouse farming environments.

---

## Researcher & Affiliations

| Role | Name / Institution |
|---|---|
| **Researcher** | Eashana (MSc/PhD Candidate) |
| **University** | Maynooth University — ARGUS Research & Innovation |
| **Supervisor** | Majid Sorouri |
| **Collaborating Institution** | Universität Leipzig |
| **Industry Partner** | MechWorks.io |

---

## System Architecture

The system is built on a **3-layer LLM-adaptive pipeline**:

```
┌─────────────────────┐
│  Layer 1            │
│  Behaviour Sensing  │  ← 8 modular sensors capture user interaction signals
└────────┬────────────┘
         │
         ▼
┌─────────────────────┐
│  Layer 2            │
│  LLM Engine         │  ← Interprets behaviour and selects the optimal UI layout
└────────┬────────────┘
         │
         ▼
┌─────────────────────┐
│  Layer 3            │
│  Adaptive UI        │  ← Renders one of three layouts in real time
└─────────────────────┘
```

### Adaptive UI Layouts

| Layout | Name | Description |
|---|---|---|
| **UI-A** | Card Stack | Sequential, card-based interaction for step-by-step guidance |
| **UI-B** | Side Panel | Contextual side panel with task controls and status |
| **UI-C** | Dashboard | Full overview dashboard for users comfortable with complex displays |

> **Safety Rule:** The LLM controls the interface only — it never directly commands the robot.

---

## Sensing & Task Design

- **8 modular sensors** capture behavioural signals (e.g., gaze, touch, hesitation, task completion time)
- **4 experiment tasks (T1–T4)** cover core FarmBot greenhouse operations

---

## Study Design

| Parameter | Value |
|---|---|
| **Participants** | 35 elderly adults (age 60+) |
| **Cohorts** | 4 |
| **Session Duration** | 90 minutes per session |
| **Statistical Tests** | Friedman test, Wilcoxon signed-rank test |
| **Effect Size Threshold** | r > 0.3 |

---

## Deliverables

| Deliverable | Description |
|---|---|
| **Workshop Presentation** | 10-slide PowerPoint deck (farm-green theme) |
| **Concise Deck** | 3-slide summary presentation |
| **Speaker Script** | Accompanying speaker notes |
| **Elder Tutorial PPT** | Tutorial slides for elderly participants (light green background + FarmBot image) |
| **Elderly Questionnaire** | Word document with professor's revisions applied |
| **Leipzig Presentation** | Slides prepared for Universität Leipzig (white background) |

> The **FarmBot greenhouse photo** is used consistently throughout all presentation materials.

---

## Key Research Questions

1. Can LLM-driven interface adaptation improve usability for elderly users operating agricultural robots?
2. Which UI layout (UI-A, UI-B, or UI-C) achieves the highest task performance and user satisfaction across cohorts?
3. What behavioural signals are most predictive of the need for interface adaptation?

---

## Statistical Analysis Plan

- **Friedman test** — non-parametric comparison of UI layouts across repeated measures
- **Wilcoxon signed-rank test** — pairwise post-hoc comparisons between layouts
- **Effect size r > 0.3** — threshold for reporting practically significant differences

---

## Repository Structure

```
college-thesis/
├── README.md           # This file
├── presentations/      # Workshop, concise, elder tutorial, and Leipzig slides
├── questionnaires/     # Elderly participant questionnaire (Word doc)
├── scripts/            # Speaker scripts and session notes
├── data/               # (Anonymised) experiment data and analysis
└── system/             # LLM engine, sensor modules, and adaptive UI code
```

---

## License

This project is part of an ongoing academic research programme. All materials are copyright © Maynooth University / ARGUS Research & Innovation unless otherwise stated.
