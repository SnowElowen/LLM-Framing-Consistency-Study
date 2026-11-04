# Framing-Induced Judgment Instability in Large Language Models

### An exploratory comparison of Gemini and GPT

**Author:** SnowElowen  
**Study date:** November 5, 2026  
**Status:** Preliminary pilot report, version 1  
**Keywords:** prompt framing, language model evaluation, probability judgments, response consistency

## Abstract

This pilot examines whether a user's stated belief changes a large language model's numerical judgment when the case facts are held constant. An employment-prospect scenario was presented to Gemini and GPT under two framings: the user described their prospects optimistically (A) or pessimistically (B). The available record contains one response from each model under each framing, for four responses in total. Gemini reported 10–20% under A and 10–15% under B; GPT reported 25% under A and 20% under B. Gemini's interval midpoints differ by 2.5 percentage points and GPT's point estimates by 5 percentage points, both in the direction of the user's stated optimism. The Gemini intervals overlap, and neither result estimates a repeatable framing effect. Both models' reported assessments remained low across the two conditions; the pilot did not reproduce a dramatic reversal of judgment. These numbers are model-generated assessments, not empirically calibrated probabilities of employment. The case provides a transparent starting point for a larger, controlled study of framing sensitivity.

## 1. Research question

Does changing a user's expressed belief about an applicant's chances change an LLM's assessment of those chances when the applicant's objective characteristics remain the same?

The outcome of interest is the **within-model** difference between responses to optimistic and pessimistic user framing. Differences *between* Gemini and GPT are descriptive secondary observations and do not answer the framing question by themselves. The broader motivation was an earlier informal exchange in which an LLM appeared to change its argument sharply after the user changed position. The present pilot tests a narrower, controlled numerical comparison; the earlier exchange is not treated as a measured observation in this dataset.

## 2. Pilot design and available record

The scenario described a 23-year-old Chinese national with an Applied Statistics degree from Malaysia, C++ and Python skills, and geographical proximity to Singapore. According to the pilot record, the two prompts kept those applicant characteristics constant and changed the user's expressed belief about employment prospects: optimistic in condition A and pessimistic in condition B. Each prompt asked for an assessment of the applicant's prospects of obtaining an entry-level role in Singapore within 12 months.

One response was recorded for each model–condition combination. The record available for this paper supplies the reported estimates and a summary of the judgments. It does **not** include the verbatim prompts, complete response transcripts, model identifiers or versions, generation settings, timestamps for each call, session structure, or prompt order. Consequently, the claim that the prompts differed only in framing is a design description that cannot be independently audited from this archive yet. Those materials should be preserved alongside any future replication.

The unit of observation is a **model response to a prompt**, not an applicant or an actual hiring outcome. No employment outcomes were collected.

### 2.1 Outcomes and descriptive calculations

Let (y_{m,A}) and (y_{m,B}) denote model (m)'s reported percentages under optimistic and pessimistic framing. For a point estimate, define the observed contrast as

[
\Delta_m = y_{m,A} - y_{m,B}.
]

For an interval ([L,U]), this report uses ( (L+U)/2 ) solely as a descriptive midpoint, then applies the same contrast. It does not interpret the interval as a confidence interval or assume the midpoint is the model's latent best estimate.

The pilot's directional comparison asks whether the reported number is higher under A. It cannot measure how often that pattern would recur. Reasoning and recommendation consistency were not coded from full transcripts.

## 3. Results

| Model | Optimistic framing A | Pessimistic framing B | Descriptive contrast A − B |
| --- | ---: | ---: | ---: |
| Gemini | 10–20% (midpoint 15%) | 10–15% (midpoint 12.5%) | +2.5 percentage points by midpoint |
| GPT | 25% | 20% | +5 percentage points |

Both recorded contrasts are positive under the specified calculation. The Gemini intervals overlap from 10% to 15%; therefore its two outputs do not establish an unambiguous increase in the underlying estimated chance. If one compared arbitrary values from the reported intervals, A − B could range from −5 to +10 percentage points. That arithmetic describes the bounds of the *reported ranges*, not a confidence interval for a framing effect.

GPT's 25% and 20% are distinct point outputs from two calls. With one response per condition, the five-point difference cannot be separated from ordinary run-to-run variation, prompt wording beyond the intended manipulation, or changes in model context and settings.

The pilot summary reports that both models continued to emphasize employment barriers in both conditions. On that qualitative record, neither made a categorical reversal. Full response transcripts are needed to examine exactly how the reasons, advice, and uncertainty language changed.

## 4. Interpretation

These four responses are **compatible with framing sensitivity**, since the descriptive contrasts point in the same direction as the user's stated belief. They are also compatible with ordinary response variability. The experiment does not estimate a stable effect size or demonstrate that either model was systematically swayed by the user's position.

The difference between Gemini's and GPT's numbers is a separate observation. In condition A, Gemini reported a range of 10–20% while GPT reported 25%. That comparison mixes model-specific behavior with differences in response format, since one model gave a range and the other a point estimate. It does not show that one model is better calibrated or more accurate.

Neither model's percentage should be read as a validated forecast of this person's job prospects. The pilot contains no applicant-level forecasting model, reference population, outcome data, or calibration check. The percentages are properties of the model responses under these prompts.

## 5. Statistical scope and limitations

This is a four-response descriptive case study: two models, two conditions, and one response per cell. There are no repeated trials from which to estimate within-condition variability, no sampling distribution for the framing contrasts, and no basis for a significance test or confidence interval for an effect. Treating the four responses as four independent applicants would be pseudoreplication.

Several design details are unavailable in the current archive: exact prompt text, full responses, model versions, settings, session continuity, call order, and the date and time of each response. In particular, shared conversation history could alter a response independently of the stated framing. The report therefore makes no causal or population-level claim.

The outcome also depends on how a model expresses uncertainty. A point estimate and an interval are not interchangeable measurements. Reducing a range to its midpoint makes the table compact, but discards its width and cannot reveal whether one response is meaningfully more optimistic.

## 6. Protocol for a larger study

A follow-up should archive the exact prompt templates and hold the applicant facts and task wording fixed while changing one predeclared framing sentence. It should include multiple applicant profiles rather than relying on one Singapore employment scenario. For each model and profile, run both conditions repeatedly in fresh, independent sessions with recorded model version, settings, prompt order, timestamp, and complete output. Randomize condition order and distribute calls across time so that condition is not confounded with sequence or a model update.

Before collecting the larger sample, specify:

1. **Primary outcome:** a numerical probability elicited in a common format, such as a single percentage under a fixed instruction. Preserve any unsolicited ranges separately.
2. **Primary contrast:** the mean within-model difference between A and B across matched profiles and repeated trials, with profiles as the main pairing unit.
3. **Secondary outcomes:** whether the substantive recommendation changes; whether cited reasons or factual claims change; and how uncertainty is expressed. Define coding rules in advance and use blinded coding where human judgment is required.
4. **Analysis:** report condition distributions and matched contrasts with uncertainty intervals that respect clustering by applicant profile and repeated model calls. Compare models through their framing contrasts, rather than comparing raw percentages alone.
5. **Decision rule and sample size:** choose a practically meaningful effect threshold and determine the number of profiles and replicates before interpreting a larger experiment. Record exclusions and any failed or incomplete calls.

A null hypothesis for that future design is that the expected within-model framing contrast is zero under the specified prompt distribution. An alternative is that it differs from zero. The present pilot supplies neither an estimate of that expectation nor a test of the hypotheses.

## 7. Conclusion

In this pilot, the reported numerical assessments were modestly higher under optimistic user framing: +2.5 percentage points by Gemini's range midpoints and +5 percentage points in GPT's point outputs. The available qualitative summary does not show a dramatic reversal of judgment. Four responses with no replications or full prompt-and-response archive establish a useful observation and a testable design question, not a systematic framing effect or an accurate employment forecast.

## Data availability and provenance

The aggregate values below were transcribed from the pilot summary supplied for this repository on November 5, 2026. They are the complete numerical dataset currently available for this report. Verbatim prompts, full model outputs, and call metadata are not yet in the archive; readers cannot independently reproduce the calls from this table alone.

| model | framing | reported_output | lower_percent | upper_percent | midpoint_percent |
| --- | --- | --- | ---: | ---: | ---: |
| Gemini | A, optimistic | 10–20% | 10 | 20 | 15 |
| Gemini | B, pessimistic | 10–15% | 10 | 15 | 12.5 |
| GPT | A, optimistic | 25% | 25 | 25 | 25 |
| GPT | B, pessimistic | 20% | 20 | 20 | 20 |

**Suggested citation:** SnowElowen (2026). *Framing-Induced Judgment Instability in Large Language Models: An Exploratory Comparison of Gemini and GPT*. Preliminary pilot report, November 5, 2026. Repository: https://github.com/SnowElowen/LLM-Framing-Consistency-Study
