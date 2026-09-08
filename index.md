---
layout: default
title: "Speech Accessibility Project Challenge 2"
subtitle: "Advancing universal dysarthric speech recognition from offline to real time."
is_home: true
---

<p>
  Welcome to the <strong>Speech Accessibility Project Challenge 2 (SAPC2)</strong>.
</p>

<p>
  Building on the success of the
  <a href="https://eval.ai/web/challenges/challenge-page/2362/overview">
    Interspeech 2025 Speech Accessibility Project Challenge
  </a>,
  where the best system reduced WER from the Whisper-large-v2 baseline of
  <strong>17.82%</strong> to <strong>8.11%</strong>, SAPC2 introduces a
  <strong>larger, more diverse, and etiology-balanced speech corpus</strong>.
</p>

<p>
  <strong>Competition Deadline:</strong> October 24, 2026 (AoE) | 
  <strong>Workshop:</strong> NeurIPS 2026, Sydney, Australia | 
  <strong>Contact:</strong>
  <a href="mailto:sapchallenge@lists.illinois.edu">
    sapchallenge@lists.illinois.edu
  </a>
</p>


## <a id="call"></a>Challenge Tracks
The challenge features two complementary tracks:
1. **Unconstrained ASR Track**: Participants may use models of any size or architecture, aiming to advance the state of the art in dysarthric speech recognition.
2. **Streaming ASR Track**: Submitted systems will be placed on a Pareto chart of system latency and system accuracy, promoting lightweight and deployable solutions for real-world use.

Competitors will submit trained model parameters and inference code through Codabench (<a href="https://www.codabench.org/competitions/14176">Track 1</a>; <a href="https://www.codabench.org/competitions/14177">Track 2</a>) up to a maximum number of permitted submissions. Results on test1 will be released within three days of submission. Results on test2 will be released after the close of competition.

## <a id="call"></a>Prizes & Publication
A total prize of U.S. $10,000 will be divided equally among all teams with a system on the Pareto frontier of accuracy and latency, as measured using the sequestered test2 set.

To clarify how winners are selected across tracks:

- **Track 1 (Unconstrained ASR):** submissions are non-streaming systems and are ranked by recognition accuracy. For Pareto comparison, Track 1 latency is set to **inf**. Exactly **one non-streaming ASR** system will win.
- **Track 2 (Streaming ASR):** submissions are ranked by the competition's accuracy-latency criteria, and **one or more** streaming systems may win.

Teams submitting to the competition will be invited to present their work at the **SAPC2 competition workshop at NeurIPS 2026 in Sydney, Australia**. NeurIPS 2026 Workshops & Competitions will take place on **December 11–12, 2026**; the exact SAPC2 session date and time will be announced later.

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

## <a id="call"></a>Organizers/Contact
- **Mark Hasegawa-Johnson** ([jhasegaw@illinois.edu](mailto:jhasegaw@illinois.edu)) — University of Illinois
- **Xiuwen Zheng** ([xiuwenz2@illinois.edu](mailto:xiuwenz2@illinois.edu)) — University of Illinois
- **Subhashini Venugopalan** ([vsubhashini@google.com](mailto:vsubhashini@google.com)) — Google Research
- **Dhruuv Agarwal** ([dhruuv@google.com](mailto:dhruuv@google.com)) — Google DeepMind
- **Venkatesh Ravichandran** ([veravic@amazon.com](mailto:veravic@amazon.com)) — Amazon
- **Colin Lea** ([colin.lea@apple.com](mailto:colin.lea@apple.com)) — Apple
- **Ed Cutrell** ([cutrell@microsoft.com](mailto:cutrell@microsoft.com)) — Microsoft

General inquiries: [sapchallenge@lists.illinois.edu](mailto:sapchallenge@lists.illinois.edu)

## <a id="call"></a>Acknowledgements
The Speech Accessibility Project is funded by a grant from the AI Accessibility Coalition. Computational resources for the challenge are provided by the National Center for Supercomputing Applications (NCSA). We would also like to thank Rob Kooper (NCSA), Wei Kang (Xiaomi Corp.), and Maisy Wieman (SoundHound AI) for their expertise and invaluable assistance in setting up the challenge.

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
