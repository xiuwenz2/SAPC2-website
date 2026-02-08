---
layout: default
title: "Page"
subtitle: "Workshop/Conference · YEAR"
is_home: true
cta_label: "Go to EvalAI"
cta_url: "YOUR_EVALAI_URL"
secondary_cta_label: "Read the Call"
secondary_cta_url: "#call"
hero_meta: >
  Use this short blurb to highlight the key story: the task, who it's for,
  and what people get out of participating (e.g. leaderboard, paper track, prizes).
---

## News

<div class="news-list">

<div class="news-item">
  <div class="news-date">2026-02-08</div>
  <div class="news-text">
    <strong><span style="color: #E84A27;"><a href="https://github.com/xiuwenz2/SAPC-template">SAPC-template</a></span></strong> updated: preprocessing, Track 1 starter kit, and evaluation.
  </div>
</div>

<div class="news-item">
    <div class="news-date">2025-12-03</div>
    <div class="news-text">
      Request the SAP corpus via the official website
      (<a href="https://speechaccessibilityproject.beckman.illinois.edu/conduct-research-through-the-project">link</a>), by
      submitting the DUA
      (<a href="https://speechaccessibilityproject.beckman.illinois.edu/docs/librariesprovider8/default-document-library/data-transfer-and-use-agreement-speech-accessibility-project.pdf?sfvrsn=909bd90f_20">link</a>)
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
    Team <strong><span style="color: #E84A27;">registration is now open</span></strong> through <a href="https://forms.gle/bajUuCF6xZYbVq2A9">link</a>.
  </div>
</div>

<div class="news-item">
  <div class="news-date">2025-12-03</div>
  <div class="news-text">
    SAPC2 Challenge website launched!
  </div>
</div>

</div>

## <a id="call"></a>Introduction
Welcome to the Speech Accessibility Project Challenge 2(SAPC2).<br>

SAPC2 builds on the success of the Interspeech 2025 Speech Accessibility Project Challenge (<a href="https://eval.ai/web/challenges/challenge-page/2362/overview">Challenge API</a>), which demonstrated significant progress in dysarthric speech recognition — reducing Word Error Rate (WER) from the Whisper-large-v2 baseline of 17.82% to 8.11%. This new edition introduces a larger, more diverse, and etiology-balanced corpus, further promoting fairness, robustness, and inclusivity in impaired-speech ASR. The challenge invites the research community to push the state of the art, develop innovative modeling techniques, and set new standards for accessible speech technology.

## <a id="call"></a>Challenge Tracks
The challenge features two complementary tracks:
1. **Unconstrained ASR Track**: Participants may use models of any size or architecture, aiming to advance the state of the art in dysarthric speech recognition.
2. **Efficiency-Constrained/Streaming ASR Track**: Submitted systems will be placed on a Pareto chart of system latency and system accuracy, promoting lightweight and deployable solutions for real-world use.

## <a id="call"></a>Evaluation Metrics
We evaluate system accuracy using transcripts normalized with a fully-formatted normalizer adapted from the HuggingFace ASR leaderboard. Two metrics are used to assess transcription accuracy:
- **Character Error Rate** (CER): Primary metric, chosen for its better correlation with human judgments and for its sensitivity to pronunciation variations in dysarthric speech.
- **Word Error Rate** (WER): Secondary metric, reported for comparison with prior work and related literature.

Both metrics are clipped to 100% at the utterance level. Scores are computed using two references (with/without disfluencies) and the lower error is selected per utterance.

System latency of streaming ASRs will be computed on CPU. Latency will be the fusion of two or more measures including time to first token and time to last token. Non-streaming ASR will be assigned a latency of infinity. 

## <a id="call"></a>Prizes
A total prize of U.S. $10,000 will be divided equally among all teams with a system on the Pareto frontier of accuracy and latency, as measured using the sequestered test2 set. Exactly one non-streaming ASR will win, and at least one streaming ASR will win.

## <a id="call"></a>Scoring
Competitors will submit trained model parameters and inference code though Codabench up to a maximum number of permitted submissions. Results on test1 will be released within three days of submission. Results on test2 will be released after the close of competition.

## <a id="call"></a>Publication
Teams submitting to the competition will be invited to present at a competition workshop, scheduled coincident with a major conference TBA.

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
The Speech Accessibility Project is funded by a grant from the AI Accessibility Coalition. Computational resources for the challenge are provided by the National Center for Supercomputing Applications.
