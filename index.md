---
layout: default
title: "Page"
subtitle: "Workshop/Conference · YEAR"
is_home: true
hero_meta: >
  Use this short blurb to highlight the key story: the task, who it's for,
  and what people get out of participating (e.g. leaderboard, paper track, prizes).
---

## News

<div class="news-list">

<div class="news-item">
  <div class="news-date">2026-02-27</div>
  <div class="news-text">
  <strong><span style="color: #E84A27;">Starter Template: </span></strong>To help you begin, SAPC-template (https://github.com/xiuwenz2/SAPC-template) is now available.
  </div>
</div>

<div class="news-item">
    <div class="news-date">2025-12-03</div>
    <div class="news-text">
      <strong><span style="color: #E84A27;">SAP Data: </span></strong>Request the SAP corpus via
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
    <strong><span style="color: #E84A27;">Registration:</span></strong> Team registration is now open through <a href="https://forms.gle/bajUuCF6xZYbVq2A9">link</a>.
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
2. **Streaming ASR Track**: Submitted systems will be placed on a Pareto chart of system latency and system accuracy, promoting lightweight and deployable solutions for real-world use.

Competitors will submit trained model parameters and inference code through <strong><span style="color: #E84A27;">Codabench</span></strong> (<a href="https://www.codabench.org/competitions/14176">Track 1</a>; <a href="https://www.codabench.org/competitions/14177">Track 2</a>) up to a maximum number of permitted submissions. Results on test1 will be released within three days of submission. Results on test2 will be released after the close of competition.

## <a id="call"></a>Evaluation Metrics
### Accuracy Metrics
Accuracy transcripts are normalized with a fully formatted normalizer adapted from the HuggingFace ASR leaderboard.

- **Character Error Rate (CER):** Primary metric, chosen for its better correlation with human judgments and its sensitivity to pronunciation variations in dysarthric speech.
- **Word Error Rate (WER):** Secondary metric, reported for comparison with prior work and related literature.

CER/WER are clipped to **100%** at the utterance level. Accuracy scores are computed using two references (with and without disfluencies), and the lower error is selected per utterance.

### Latency Metrics (Track 2 only)
Latency is computed from streaming partial results on the streaming manifest (`*_streaming.csv`) and reported as median (**P50**, in ms). Reference implementation:
[`compute_latency.py`](https://github.com/xiuwenz2/SAPC-template/blob/main/utils/compute_latency.py).

- **Time To First Token (TTFT, P50, ms):**  
  `first_non_empty_partial_time - (audio_send_start_time + mfa_speech_start)`
- **Time To Last Token (TTLT, P50, ms):**  
  `final_visible_time - audio_end_oracle_time`, where `audio_end_oracle_time = audio_send_start_time + audio_duration_sec`

For robustness analysis, P90 latency is also be reported in detailed outputs. Non-streaming ASR is assigned infinite latency for Pareto comparison.

## <a id="call"></a>Prizes & Publication
A total prize of U.S. $10,000 will be divided equally among all teams with a system on the Pareto frontier of accuracy and latency, as measured using the sequestered test2 set.

To clarify how winners are selected across tracks:

- **Track 1 (Unconstrained ASR):** submissions are non-streaming systems and are ranked by recognition accuracy. For Pareto comparison, Track 1 latency is set to **inf**. Exactly **one non-streaming ASR** system will win.
- **Track 2 (Streaming ASR):** submissions are ranked by the competition's accuracy-latency criteria, and **one or more** streaming systems may win.

Teams submitting to the competition will be invited to present their work at a competition workshop, scheduled in conjunction with a major conference (TBA).

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