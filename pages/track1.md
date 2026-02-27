---
layout: default
title: "Track 1"
permalink: /track1/
---

## Track 1: Unconstrained ASR Track

**Goal:** Advance the state of the art in dysarthric speech recognition.

### Baseline Results
Official baselines follow the same ranking system as the <a href="https://huggingface.co/spaces/hf-audio/open_asr_leaderboard">HuggingFace Open ASR Leaderboard</a>.
<!-- Official baselines and reproducible code are available at
<a href="YOUR_BASELINES_REPO_URL" target="_blank" rel="noopener">this repository</a>. -->
<div class="baseline-block">
  <div class="table-wrapper">
    <table class="baseline-table">
      <thead>
        <tr>
          <th rowspan="3">Model ID</th>
          <th colspan="4">CER ↓</th>
          <th colspan="4">WER ↓</th>
        </tr>
        <tr>
          <th colspan="3">Dev</th>
          <th rowspan="2">Test1</th>
          <th colspan="3">Dev</th>
          <th rowspan="2">Test1</th>
        </tr>
        <tr>
          <th>All</th>
          <th>Shared</th>
          <th>Unshared</th>
          <th>All</th>
          <th>Shared</th>
          <th>Unshared</th>
        </tr>
      </thead>

      <tbody>
        <tr>
          <td><code><a href="https://huggingface.co/nvidia/canary-qwen-2.5b">nvidia/canary-qwen-2.5b</a></code></td>
          <td>14.38</td>
          <td>15.86</td>
          <td>13.50</td>
          <td>17.93</td>
          <td>20.25</td>
          <td>22.60</td>
          <td>18.89</td>
          <td>24.54</td>
        </tr>

        <tr>
          <td><code><a href="https://huggingface.co/nvidia/parakeet-tdt-0.6b-v2">nvidia/parakeet-tdt-0.6b-v2</a></code></td>
          <td>13.43</td>
          <td>16.47</td>
          <td>11.61</td>
          <td>16.07</td>
          <td>19.59</td>
          <td>24.04</td>
          <td>17.00</td>
          <td>22.83</td>
        </tr>

        <tr>
          <td><code><a href="https://huggingface.co/openai/whisper-large-v2">openai/whisper-large-v2</a></code></td>
          <td>13.27</td>
          <td>16.40</td>
          <td>11.39</td>
          <td>15.19</td>
          <td>18.70</td>
          <td>22.87</td>
          <td>16.27</td>
          <td>21.46</td>
        </tr>
        
        <tr>
          <td><code><a href="https://huggingface.co/xiuwenz2/whisper-large-v2-ft-SAP-0430-pd-merged-ct2">xiuwenz2/whisper-large-v2-ft-SAP-0430-pd-merged-ct2</a></code></td>
          <td>9.10</td>
          <td>8.79</td>
          <td>9.29</td>
          <td>13.49</td>
          <td>13.04</td>
          <td>12.12</td>
          <td>13.58</td>
          <td>19.05</td>
        </tr>
      </tbody>
    </table>
  </div>

</div>

