---
layout: default
title: "YOUR CHALLENGE NAME"
subtitle: "WORKSHOP/CONFERENCE · YEAR"
---

## News
- **YYYY-MM-DD** — Registration opens.
- **YYYY-MM-DD** — Baselines released.
- **YYYY-MM-DD** — Leaderboard opens.

<div class="callouts">
  <div class="callout">
    <h3>Quick links</h3>
    <p>
      <a href="YOUR_EVALAI_URL">EvalAI challenge page</a> ·
      <a href="YOUR_BASELINES_REPO_URL">Baselines</a> ·
      <a href="YOUR_DATA_URL">Dataset</a>
    </p>
  </div>
  <div class="callout">
    <h3>What you submit</h3>
    <p>One JSONL file (one line per sample): reasoning + final answer.</p>
  </div>
</div>

## Introduction
Write 1–2 paragraphs explaining the problem and why it matters.  
(ARC’s homepage structure is a good pattern: motivation → gap → what the challenge pushes.) :contentReference[oaicite:3]{index=3}

## Challenge Goals
List 3–5 clear goals. Example:
- Robust performance across speakers/environments
- Transparent reasoning / error analysis
- Reproducible systems

## Tracks
### Track 1: Single Model
A single end-to-end model that consumes inputs and emits both a **reasoning trace** and a **final prediction**.  
(ARC uses a similar two-track split: single-model vs agent/system track.) :contentReference[oaicite:4]{index=4}

### Track 2: Agent / System
A tool-using pipeline that can run multiple open components (ASR, diarization, separation, scoring, etc.) with no human-in-the-loop. :contentReference[oaicite:5]{index=5}

## Data & Evaluation (SAP-style template)
If your challenge is ASR/accessibility-like, this is a proven layout:
- **Data**: train/dev + **public leaderboard test set** and **private final test set** (often called Test1/Test2) :contentReference[oaicite:6]{index=6}
- **Platform**: EvalAI; optionally remote evaluation for privacy-sensitive test data :contentReference[oaicite:7]{index=7}
- **Metrics**: a primary accuracy metric (e.g., **WER**) and a meaning-preservation metric (e.g., **semantic score**) :contentReference[oaicite:8]{index=8}

## Submission format (JSONL)
```json
{"id":"<sample_id>","reasoning_prediction":"...","answer_prediction":"..."}
