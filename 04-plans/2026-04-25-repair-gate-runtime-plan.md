# Repair Gate Runtime Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a reusable runtime gate that creates Flatsome pages in draft, runs repair-gate verification, writes `Fix Pass` and `Final Verification` artifacts, and only leaves the page public when checks pass.

**Architecture:** Keep `VPS/tmp/publish_wp_page_from_shortcode.py` as a low-level publish utility, extract reusable WordPress session and verification helpers into one shared runtime module, then add one orchestration script that performs `draft-first -> preflight -> publish -> public verify -> revert to draft on fail`. Generate task artifacts directly from the runtime result so future page tasks reuse the same gate.

**Tech Stack:** Python 3, requests, pytest, WordPress admin form publish flow, Markdown artifact rendering

---

### Task 1: Add failing tests for repair-gate primitives

**Files:**
- Create: `VPS/tmp/tests/test_flatsome_runtime_gate.py`
- Create: `VPS/tmp/flatsome_runtime_gate.py`

- [ ] Add tests for raw shortcode leak detection.
- [ ] Add tests for failure classification into the company error groups.
- [ ] Add tests for `Fix Pass` and `Final Verification` markdown rendering.

### Task 2: Implement the shared runtime helper

**Files:**
- Modify: `VPS/tmp/flatsome_runtime_gate.py`

- [ ] Implement shared WordPress login and page upsert helpers.
- [ ] Implement `verify_surfaces` with `draft preflight` and `public verify` modes.
- [ ] Implement raw shortcode leak detection for known closing tags.
- [ ] Implement render helpers for `Fix Pass` and `Final Verification`.

### Task 3: Reuse the helper in the existing verification script

**Files:**
- Modify: `VPS/tmp/verify_wp_page_surfaces.py`

- [ ] Reuse shared raw leak detection and verification logic.
- [ ] Preserve current CLI behavior for existing tasks.
- [ ] Make the script fail on raw closing-tag leaks, not just `[section` / `[row`.

### Task 4: Add the runtime orchestration script

**Files:**
- Create: `VPS/tmp/run_flatsome_repair_gate.py`

- [ ] Create page as `draft`.
- [ ] Run `edit + builder` preflight.
- [ ] Publish only if preflight passes.
- [ ] Run public verification after publish.
- [ ] Revert page to `draft` if public verification fails.
- [ ] Write `Fix Pass` and `Final Verification` artifacts into the requested reports directory.

### Task 5: Verify the runtime locally

**Files:**
- Modify: `VPS/docs/superpowers/flatsome-native/05-flows/UI Build Script.md`

- [ ] Run pytest for the new helper tests.
- [ ] Run the verification script help/CLI sanity check.
- [ ] Update the flow doc to point runtime execution at the new script.
