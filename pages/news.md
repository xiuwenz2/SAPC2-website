---
layout: default
title: "News"
permalink: /news/
---

## News

<div class="news-list">

<div class="news-item">
  <div class="news-date">2026-09-07</div>
  <div class="news-text">
    <strong><span style="color: #E84A27;">Update: Track 2 Latency Metric (TTFT → TTFT-stable)</span></strong><br>
    To mitigate potential reward-hacking risk, the Time To First Token (TTFT) metric is upgraded to
    <a href="https://github.com/xiuwenz2/SAPC-template/blob/d96ef4872694f56688efdce884d5751ee5916e26/utils/compute_latency.py#L111"><strong>TTFT-stable</strong></a>, which measures the earliest timestamp
    where the hypothesis’s first word has already settled to its final value.
    In addition, submissions will be <strong>rejected</strong> if their
    <a href="https://github.com/xiuwenz2/SAPC-template/blob/main/utils/stable_sentence_prefix_match.py">stable sentence-prefix match rate</a>
    falls below <strong>1/3</strong>.
  </div>
</div>

<div class="news-item">
  <div class="news-date">2026-08-24</div>
  <div class="news-text">
    <strong><span style="color: #E84A27;">Update: Submission Limit Increased</span></strong><br>
    Following the competition deadline extension, the total submission limit has been increased
    from <strong>50 to 68 submissions</strong>, accounting for the additional submission allowance
    of <strong>one submission every three days</strong>.
  </div>
</div>

<div class="news-item">
  <div class="news-date">2026-08-14</div>
  <div class="news-text">
    <strong><span style="color: #E84A27;">Update: SAPC2 Deadline Extension</span></strong><br>
    SAPC2 has been accepted as a <strong>NeurIPS 2026 Challenge</strong>. 
    The final competition deadline has been extended:
    <s style="color: #888;">August 31, 2026</s> → 
    <strong>October 24, 2026 (AoE)</strong>.<br>
    Participating teams are invited to present at the SAPC2 workshop at NeurIPS 2026 in Sydney.
  </div>
</div>

<div class="news-item">
  <div class="news-date">2026-08-05</div>
  <div class="news-text">
    <strong><span style="color: #E84A27;">SAPC2 Accepted to the NeurIPS 2026 Competition Track</span></strong><br>
    We are excited to announce that the Speech Accessibility Project Challenge 2 (SAPC2)
    has been accepted to the <strong>NeurIPS 2026 Competition Track</strong>!<br>
    SAPC2 is one of 16 competitions selected for NeurIPS 2026 and will conclude with
    a competition workshop in Sydney, Australia.<br>
    <a href="https://speechaccessibilityproject.beckman.illinois.edu/article/2026/08/05/speech-accessibility-project-selected-to-neural-information-processing-systems-competition"
       target="_blank" rel="noopener noreferrer">
      Read the official Speech Accessibility Project announcement.
    </a>
  </div>
</div>

<div class="news-item">
  <div class="news-date">2026-04-07</div>
  <div class="news-text">
    <strong><span style="color: #E84A27;">Update: SAPC2 Deadline Extension</span></strong><br>
    The submission deadline has been extended: 
    <s style="color: #888;">End of April 2026</s> → 
    <strong>August 31, 2026</strong><br>
    This extension aims to accommodate ongoing submissions, particularly for Track 2, 
    and teams with pending Data Use Agreements (DUAs). 
    We hope this provides additional time for participation and preparation.
  </div>
</div>

<div class="news-item">
  <div class="news-date">2026-03-18</div>
  <div class="news-text">
    <strong><span style="color: #E84A27;">Update: Inference Time Limit (Track 1)</span></strong><br>
    The Ingestion time limit per submission has been increased: 
    <s style="color: #888;">15000s</s> → 
    <strong>21600s</strong>
  </div>
</div>

<div class="news-item">
  <div class="news-date">2026-03-12</div>
  <div class="news-text">
    <strong><span style="color: #E84A27;">Starter Template Update: </span></strong>
    <strong>Local decoding script</strong> is now available for both tracks 
    (<a href="https://github.com/xiuwenz2/SAPC-template/tree/main/track1_starting_kit#local-dev-test-with-dev-set">Track 1</a>; 
    <a href="https://github.com/xiuwenz2/SAPC-template/tree/main/track2_starting_kit#local-dev-test-with-dev-set">Track 2</a>). 
    In addition, the <code>Dev_streaming</code> subset for latency measurement is shared through Box, and the corresponding code has been added to 
    <a href="https://github.com/xiuwenz2/SAPC-template/blob/aac08c079ed610e3f83bc2d8d72dc42c94d81d33/preprocess.sh#L94">preprocess.sh</a>.
  </div>
</div>

<div class="news-item">
  <div class="news-date">2026-02-27</div>
  <div class="news-text">
  <strong><span style="color: #E84A27;">Competition Pages & Leaderboards: </span></strong>The Codabench API for (<a href="https://www.codabench.org/competitions/14176">Track 1</a>; <a href="https://www.codabench.org/competitions/14177">Track 2</a>) has been released.
  </div>
</div>

<div class="news-item">
  <div class="news-date">2026-02-27</div>
  <div class="news-text">
  <strong><span style="color: #E84A27;">Starter Template: </span></strong>To help you begin, SAPC-template (https://github.com/xiuwenz2/SAPC-template) is now available.
  </div>
</div>

<div class="news-item">
    <div class="news-date">2025-12-03</div>
    <div class="news-text">
      <strong><span style="color: #E84A27;">Data Access: </span></strong>Request the SAP corpus via
      (<a href="https://speechaccessibilityproject.beckman.illinois.edu/conduct-research-through-the-project">the official website</a>), by
      submitting the
      (<a href="https://speechaccessibilityproject.beckman.illinois.edu/docs/librariesprovider8/default-document-library/data-transfer-and-use-agreement-speech-accessibility-project.pdf?sfvrsn=909bd90f_20">DUA</a>)
      and a one-page proposal to <a href="mailto:speechaccessibility@beckman.illinois.edu">email</a>.<br>
      <em>Note: <strong><span style="color: #E84A27;">Approval typically takes ~2–4 weeks.</span></strong> Upon approval, access will be immediately granted
      to the SAP Research Release, which contains most of the same waveforms that will be part of
      the official competition release, but in a different data format.  The official competition
      release will be made available on <strong>2026-03-01</strong> to early approvals, or immediately
      once approved after that date.</em>
    </div>
  </div>

<div class="news-item">
  <div class="news-date">2025-12-03</div>
  <div class="news-text">
    <strong><span style="color: #E84A27;">Team Registration:</span></strong> Team registration is now open through <a href="https://forms.gle/bajUuCF6xZYbVq2A9">link</a>.
  </div>
</div>

<div class="news-item">
  <div class="news-date">2025-12-03</div>
  <div class="news-text">
    SAPC2 Challenge website launched!
  </div>
</div>

</div>
