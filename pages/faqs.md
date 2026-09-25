---
layout: default
title: "FAQs"
subtitle: "Advancing universal dysarthric speech recognition from offline to real time"
permalink: /faqs/
---

## FAQs

**Q: Can I use extra data?**  
A: Yes.  The distributed train and dev corpora were recorded using the same protocol
as the test corpora, and are therefore expected to be better-matched to the test data
than any other source. Competing teams may find, however, that system performance benefits
from the use of other datasets; if so, teams are encouraged to describe the other datasets
used, and the method of their use.

**Q: Why are there two test sets (test1 and test2), and which one determines the final ranking?**  
A: All completed submissions are evaluated on both test1 and test2 in parallel. Test1 results
are published within three days of submission and are mainly for benchmarking during the
competition; test2 results are withheld until the competition closes and are used for the
final official ranking.

**Q: How is my final ranking determined among my submissions?**  
A: For both tracks, **all valid submissions** from a team are considered for the final
evaluation. We automatically identify each team's best (Track 1) or Pareto-frontier (Track 2)
submission(s), so you do not need to manually pick a final one.

**Q: What metrics determine the final ranking?**  
A: Ranking is based on **CER** (Character Error Rate), our primary metric — our normalization
procedure is optimized around CER. WER is reported only as a secondary/reference metric and is
not combined with CER. For Track 2, latency uses TTFT-stable and TTLT with equal weight.

**Q: How do I benchmark on the leaderboard?**  
A: Submit your system using the provided <a href="https://github.com/xiuwenz2/SAPC-template">starter template</a> through the CodaBench Challenge page
(<a href="https://www.codabench.org/competitions/14176">Track 1</a>; <a href="https://www.codabench.org/competitions/14177">Track 2</a>) to receive official evaluation and appear on the leaderboard.

**Q: Do I need to open-source my code?**  
A: No. Code submitted to the challenge remains the intellectual property of the submitting
team unless separately open-sourced.

**Q: Is the workshop paper archival, and is it required to attend the workshop?**  
A: No to both. Submitting a paper is optional — teams who don't submit one can still attend the
workshop, and it is not a requirement for the competition or the prize pool. The paper is
**non-archival**, so you are free to submit the same or an extended version of the work to other
venues (e.g., Interspeech, ICASSP) afterward. Review is lightweight: papers are single-blind and
are not rejected based on technical content, only if unrelated to the competition or too unclear
to understand. See the <a href="{{ site.baseurl }}/papers/">Call for Papers</a> for details and
deadlines.
