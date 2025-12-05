---
layout: default
title: "Track 1"
permalink: /track1/
---

## Track 1: Unconstrained ASR

**Goal:** Advance the state of the art in dysarthric speech recognition.

<h3 style="margin-bottom:0;">Baseline Results</h3>
<div class="baseline-block">
  <p class="baseline-note">
    Official baselines follow the same ranking system as the <a href="https://huggingface.co/spaces/hf-audio/open_asr_leaderboard">HuggingFace Open ASR Leaderboard</a>.<br>
    <!-- Official baselines and reproducible code are available at
    <a href="YOUR_BASELINES_REPO_URL" target="_blank" rel="noopener">this repository</a>. -->
  </p>

  <div class="table-wrapper">
    <table class="baseline-table">
      <thead>
        <tr>
          <th rowspan="2">Model ID</th>
          <th colspan="2">CER ↓</th>
          <th colspan="2">WER ↓</th>
        </tr>
        <tr>
          <th>Dev</th>
          <th>Test1</th>
          <th>Dev</th>
          <th>Test1</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td><code><a href="https://huggingface.co/nvidia/canary-qwen-2.5b">nvidia/canary-qwen-2.5b</a></code></td>
          <td>14.43</td>
          <td>17.97</td>
          <td>20.58</td>
          <td>24.82</td>
        </tr>
        <tr>
          <td><code><a href="https://huggingface.co/nvidia/parakeet-tdt-0.6b-v2">nvidia/parakeet-tdt-0.6b-v2</a></code></td>
          <td>13.53</td>
          <td>16.12</td>
          <td>20.29</td>
          <td>23.20</td>
        </tr>
        <tr>
          <td><code><a href="https://huggingface.co/openai/whisper-large-v2">openai/whisper-large-v2</a></code></td>
          <td>13.33</td>
          <td>15.25</td>
          <td>19.00</td>
          <td>21.74</td>
        </tr>
      </tbody>
    </table>
  </div>

  Note: Reproducible code will be announced soon.
</div>


