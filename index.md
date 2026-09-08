---
layout: default
title: "Speech Accessibility Project Challenge 2"
subtitle: 'NeurIPS 2026 Competition Track · Sydney, Australia<br><a href="mailto:sapchallenge@lists.illinois.edu">sapchallenge@lists.illinois.edu</a>'
is_home: true
hero_meta: >
  Advancing accessible speech recognition through unconstrained and streaming ASR, with $10,000 in prizes and a competition workshop at NeurIPS 2026.
---

<p class="contact">
  Contact: <a href="mailto:sapchallenge@lists.illinois.edu">sapchallenge@lists.illinois.edu</a>
</p>

<!-- ## <a id="call"></a>Competition Overview -->
Welcome to the Speech Accessibility Project Challenge 2 (SAPC2). Built on the success of the Interspeech 2025 Speech Accessibility Project Challenge (<a href="https://eval.ai/web/challenges/challenge-page/2362/overview">Challenge API</a>), which demonstrated significant progress in dysarthric speech recognition — reducing Word Error Rate (WER) from the Whisper-large-v2 baseline of 17.82% to 8.11%, SAPC2 introduces a larger, more diverse, and etiology-balanced corpus, and features two complementary tracks: an **Unconstrained ASR Track** for advancing state-of-the-art accuracy, and a **Streaming ASR Track** for lightweight, low-latency systems. The competition deadline is **October 24, 2026 (AoE)**, with a workshop at NeurIPS 2026 in Sydney, Australia.

## <a id="how-to-participate"></a>How to Participate

<div class="how-to-participate">

<div class="step-item">
  <div class="step-title">Step 1: Register Your Team</div>
  <div class="step-text">
    Please register your team for the challenge using the <a href="https://forms.gle/bajUuCF6xZYbVq2A9">Team Registration Form</a>.
  </div>
</div>

<div class="step-item">
  <div class="step-title">Step 2: Request Data Access</div>
  <div class="step-text">
    To access the SAP corpus, please submit the
    <a href="https://speechaccessibilityproject.beckman.illinois.edu/docs/librariesprovider8/default-document-library/data-transfer-and-use-agreement-speech-accessibility-project.pdf?sfvrsn=909bd90f_20">Data Transfer and Use Agreement (DUA)</a>
    and a one-page proposal to <a href="mailto:speechaccessibility@beckman.illinois.edu">speechaccessibility@beckman.illinois.edu</a>.<br>
    <em>Note: Approval typically takes ~2–4 weeks.</em>
  </div>
</div>

<div class="step-item">
  <div class="step-title">Step 3: Develop Your System</div>
  <div class="step-text">
    To help you get started, we have provided a starting kit and local decoding scripts. Check out the
    <a href="https://github.com/xiuwenz2/SAPC-template">SAPC-template on GitHub</a>.
  </div>
</div>

<div class="step-item">
  <div class="step-title">Step 4: Submit to Codabench</div>
  <div class="step-text">
    Competitors will submit trained systems through Codabench:
    <a href="https://www.codabench.org/competitions/14176">Track 1 (Unconstrained ASR)</a>,
    <a href="https://www.codabench.org/competitions/14177">Track 2 (Streaming ASR)</a>.<br>
    <strong>Deadline for submissions: October 24, 2026 AoE</strong>
  </div>
</div>

</div>

## News

<div class="news-list">

<div class="news-item">
  <div class="news-date">2026-09-07</div>
  <div class="news-text">
    <strong><span style="color: #E84A27;">Update: Track 2 Latency Metric (TTFT → TTFT-stable)</span></strong><br>
    To mitigate potential reward-hacking risk, the Time To First Token (TTFT) metric is upgraded to
    <a href="https://github.com/xiuwenz2/SAPC-template/blob/d96ef4872694f56688efdce884d5751ee5916e26/utils/compute_latency.py#L111"><strong>TTFT-stable</strong><\a>, which measures the earliest timestamp
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

## <a id="call"></a>Challenge Tracks
The challenge features two complementary tracks:
1. **Unconstrained ASR Track**: Participants may use models of any size or architecture, aiming to advance the state of the art in dysarthric speech recognition.
2. **Streaming ASR Track**: Submitted systems will be placed on a Pareto chart of system latency and system accuracy, promoting lightweight and deployable solutions for real-world use.

Competitors will submit trained model parameters and inference code through Codabench (<a href="https://www.codabench.org/competitions/14176">Track 1</a>; <a href="https://www.codabench.org/competitions/14177">Track 2</a>) up to a maximum number of permitted submissions. Results on test1 will be released within three days of submission. Results on test2 will be released after the close of competition.

## <a id="call"></a>Evaluation Metrics
- **Accuracy metrics (Track 1 & Track 2)**
  - Accuracy transcripts are normalized with a fully formatted normalizer adapted from the HuggingFace ASR leaderboard.
  - **Character Error Rate (CER):** primary metric, chosen for better correlation with human judgments and sensitivity to pronunciation variations in dysarthric speech.
  - **Word Error Rate (WER):** secondary metric, reported for comparison with prior work and related literature.
  - CER/WER are clipped to **100%** at the utterance level. Scores are computed using two references (with and without disfluencies), and the lower error is selected per utterance.

- **Latency metrics (Track 2 only)**
  - Latency is computed from streaming partial results on the streaming manifest (`*_streaming.csv`) and reported as median (**P50**, in ms).
  - Reference implementation: [`compute_latency.py`](https://github.com/xiuwenz2/SAPC-template/blob/main/utils/compute_latency.py).
  - <s>**Time To First Token (TTFT, P50, ms):** `first_non_empty_partial_time - (audio_send_start_time + mfa_speech_start)`.</s>
  - <span style="color: #E84A27;">**Time To First Token, stable (TTFT-stable, P50, ms):** `first_stable_partial_time - (audio_send_start_time + mfa_speech_start)`, where `first_stable_partial_time` is the earliest time at which a system's first word has already settled to its final value. TTFT-stable replaces TTFT to reduce reward-hacking risk from guessing an early word before enough audio has been processed. Submissions with a [stable sentence-prefix match rate](https://github.com/xiuwenz2/SAPC-template/blob/main/utils/stable_sentence_prefix_match.py) below **1/3** will be rejected.</span>
  - **Time To Last Token (TTLT, P50, ms):** `final_visible_time - audio_end_oracle_time`, where `audio_end_oracle_time = audio_send_start_time + audio_duration_sec`.
  - For robustness analysis, P90 latency may also be reported in detailed outputs.
  - For Pareto comparison, we use the average of TTFT-stable and TTLT as latency; non-streaming ASR is assigned infinity.

## <a id="call"></a>Prizes & Publication
A total prize of U.S. $10,000 will be divided equally among all teams with a system on the Pareto frontier of accuracy and latency, as measured using the sequestered test2 set.

To clarify how winners are selected across tracks:

- **Track 1 (Unconstrained ASR):** submissions are non-streaming systems and are ranked by recognition accuracy. For Pareto comparison, Track 1 latency is set to **inf**. Exactly **one non-streaming ASR** system will win.
- **Track 2 (Streaming ASR):** submissions are ranked by the competition's accuracy-latency criteria, and **one or more** streaming systems may win.

Teams submitting to the competition will be invited to present their work at the **SAPC2 competition workshop at NeurIPS 2026 in Sydney, Australia**. NeurIPS 2026 Workshops & Competitions will take place on **December 11–12, 2026**; the exact SAPC2 session date and time will be announced later.

## References
- [1] Hasegawa-Johnson, M., et al. *Community-supported shared infrastructure in support of speech accessibility.* JSLHR, 67(11), 4162–4175, 2024.
- [2] Zheng, X., et al. *The Interspeech 2025 Speech Accessibility Project Challenge.* Proc. Interspeech, 2025.
- [3] Gohider, N., et al. *Towards Inclusive and Fair ASR: Insights from the SAPC Challenge for Optimizing Disordered Speech Recognition.* Proc. Interspeech, 2025.
- [4] Ducorroy, A., et al. *Robust fine-tuning of speech recognition models via model merging: application to disordered speech.* Proc. Interspeech, 2025.
- [5] La Quatra, M., et al. *Exploring Generative Error Correction for Dysarthric Speech Recognition.* Proc. Interspeech, 2025.
- [6] Baumann, I., et al. *Pathology-Aware Speech Encoding and Data Augmentation for Dysarthric Speech Recognition.* Proc. Interspeech, 2025.
- [7] Wagner, D., et al. *Personalized Fine-Tuning with Controllable Synthetic Speech from LLM-Generated Transcripts for Dysarthric Speech Recognition.* Proc. Interspeech, 2025.
- [8] Wang, S., et al. *A Self-Training Approach for Whisper to Enhance Long Dysarthric Speech Recognition.* Proc. Interspeech, 2025.
- [9] Takahashi, K., et al. *Fine-tuning Parakeet-TDT for Dysarthric Speech Recognition in the Speech Accessibility Project Challenge.* Proc. Interspeech, 2025.
- [10] Tan, T., et al. *CBA-Whisper: Curriculum Learning-Based AdaLoRA Fine-Tuning on Whisper for Low-Resource Dysarthric Speech Recognition.* Proc. Interspeech, 2025.
- [11] Thennal, D.K., et al. *Advocating Character Error Rate for Multilingual ASR Evaluation.* Findings of ACL: NAACL 2025.

## <a id="call"></a>Acknowledgements
The Speech Accessibility Project is funded by a grant from the AI Accessibility Coalition. Computational resources for the challenge are provided by the National Center for Supercomputing Applications (NCSA). We would also like to thank Rob Kooper (NCSA), Wei Kang (Xiaomi Corp.), and Maisy Wieman (SoundHound AI) for their expertise and invaluable assistance in setting up the challenge.
