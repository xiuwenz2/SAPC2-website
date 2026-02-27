---
layout: default
title: "Track 2"
permalink: /track2/
---

## Track 2: Streaming ASR Track

**Goal:** Promote lightweight, deployable dysarthric ASR solutions for real-world use.

### Baseline Results
We report one official baseline on Test1 with both accuracy and latency metrics.

<div class="baseline-block">
  <div class="table-wrapper">
    <table class="baseline-table">
      <thead>
        <tr>
          <th rowspan="2">Model ID</th>
          <th colspan="4">Test1</th>
        </tr>
        <tr>
          <th>CER ↓</th>
          <th>WER ↓</th>
          <th>TTFT P50 (ms) ↓</th>
          <th>TTLT P50 (ms) ↓</th>
        </tr>
      </thead>
      <tbody>
        <tr>
        <td><code><a href="https://huggingface.co/Zengwei/icefall-asr-librispeech-streaming-zipformer-2023-05-17">Zengwei/icefall-asr-librispeech-streaming-zipformer-2023-05-17</a></code></td>
          <td>34.59</td>
          <td>52.77</td>
          <td>1025.04</td>
          <td>423.46</td>
        </tr>
      </tbody>
    </table>
  </div>

</div>

