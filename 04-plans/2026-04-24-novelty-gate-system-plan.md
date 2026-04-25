# Novelty Gate System Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Turn `Layout DNA` and `No Repeat Law` from reference docs into a hard-gate system that blocks repetitive layouts before build and before release.

**Architecture:** Add four new operating files for layout pool, hero family rotation, novelty scoring, and recent-page memory. Then wire those files into the law layer, build flow, QA flow, templates, and entry docs so every future page must pass a novelty gate.

**Tech Stack:** Markdown knowledge hub, Flatsome operating law, templates, reports

---

### Task 1: Add the novelty gate source files

**Files:**
- Create: `VPS/docs/superpowers/flatsome-native/03-factory/Layout Pool.md`
- Create: `VPS/docs/superpowers/flatsome-native/03-factory/Hero Family Matrix.md`
- Create: `VPS/docs/superpowers/flatsome-native/01-platform/Novelty Scoring Rule.md`
- Create: `VPS/docs/superpowers/flatsome-native/07-reports/Recent Page Memory.md`

- [ ] Write a layout pool file that forces builders to choose from distinct layout families instead of drifting into the same safe pattern.
- [ ] Write a hero family matrix that makes hero rotation explicit and prevents repeated hero behavior.
- [ ] Write a novelty scoring rule with pass, warn, and blocked thresholds.
- [ ] Create a recent page memory file with the latest live pages and their structural traits so workers compare against real history.

### Task 2: Wire the new rules into the operating docs

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/Operating Law.md`
- Modify: `VPS/docs/superpowers/flatsome-native/03-factory/No Repeat Law.md`
- Modify: `VPS/docs/superpowers/flatsome-native/03-factory/Factory Overview.md`
- Modify: `VPS/docs/superpowers/flatsome-native/03-factory/README.md`
- Modify: `VPS/docs/superpowers/flatsome-native/01-platform/README.md`
- Modify: `VPS/docs/superpowers/flatsome-native/README.md`
- Modify: `VPS/docs/superpowers/flatsome-native/START HERE.md`
- Modify: `VPS/docs/superpowers/flatsome-native/07-reports/README.md`

- [ ] Promote novelty from recommendation to hard gate in the law layer.
- [ ] Make the factory layer point to layout pool, hero matrix, and recent-page memory before any build.
- [ ] Update entry docs so future workers read the anti-repeat system early.

### Task 3: Wire the gate into templates and execution flow

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/05-flows/UI Build Script.md`
- Modify: `VPS/docs/superpowers/flatsome-native/05-flows/Final QA Checklist.md`
- Modify: `VPS/docs/superpowers/flatsome-native/06-templates/Page Plan Template.md`
- Modify: `VPS/docs/superpowers/flatsome-native/06-templates/Native Scoring Template.md`
- Modify: `VPS/docs/superpowers/flatsome-native/06-templates/README.md`

- [ ] Add a mandatory pre-build novelty gate to the UI build script.
- [ ] Add novelty blocking checks to final QA.
- [ ] Extend the page plan so builders must record pool, hero family, comparison pages, predicted risk, and predicted novelty score.
- [ ] Extend scoring templates so release requires both native score and novelty score evidence.

### Task 4: Self-audit and sync status

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/07-reports/Recent Page Memory.md`

- [ ] Re-check the new file paths and cross-references.
- [ ] Make sure the recent page memory includes the repetitive pages discovered so the new system has immediate context.
- [ ] Confirm the new hard-gate language is consistent across law, plan, QA, and templates.
