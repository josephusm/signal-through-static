---
title: "The Second Hallucination"
date: 2026-09-27
draft: false
tags: ["ai", "verification", "incident-response", "accountability"]
---

When a language model invents a fact, the first question is obvious: what is true?

The second arrives wearing a lab coat: why did the model do it?

Ask the machine that just failed and it may provide a plausible, technical cause, neatly shaped like closure. It may also be a second hallucination.

We distrust unsupported answers. We are less disciplined with unsupported post-mortems.

## A cause is another claim

A model says that it confused two names because they appeared near each other in training. Or that a tool call failed because a rate limit was reached. Or that missing context caused it to infer the wrong event. Each explanation has the texture of mechanism.

Texture is not evidence.

Without logs, traces, tool output or a reproducible failure, the explanation is another generated statement: a hypothesis, not a verdict. Trouble starts when a hypothesis is formatted as an incident report and allowed to end the investigation.

The first hallucination corrupts the fact. The second corrupts the lesson. It teaches operators to repair the wrong thing, then lets the completed ticket serve as evidence that the system diagnosed itself. The architecture receives absolution by ticket.

## The authority of fluency

Technical fluency is not privileged access to the generating mechanism. A system that can describe transformers is not thereby observing the causal path that produced its last sentence.

There is empirical reason for caution. [Turpin and colleagues](https://arxiv.org/abs/2305.04388) found chain-of-thought explanations that rationalized answers influenced by biasing features they did not mention. [Lanham and colleagues](https://arxiv.org/abs/2307.13702) found that faithfulness varied substantially across tasks and models when they intervened on the stated reasoning. This does not prove that every model explanation is false. It does make plausible reasoning unfit for service as causal telemetry.

An eloquent autopsy is still not a sensor. The honest answer—*we do not yet know*—usually has worse typography.

## Separate the ledgers

A useful post-mortem needs three ledgers and two clocks.

The first ledger holds facts, records and tool output. The second holds missing logs, unobserved states and lost context. The third holds hypotheses: retrieval confusion, stale state, failed execution or invention.

The clocks separate the failure from its later explanation. Otherwise retrospective prose can become evidence for itself.

Even tidy ledgers inherit a boundary: someone chose what was recorded, at what resolution and for how long. Every recorded step can succeed while the relevant event stays outside the schema. The report must name who drew that boundary and who can contest it.

Do not merge hypothesis into fact because the prose is smooth.

This is the difference between investigation and folklore. A model can propose tests, compare hypotheses and look for contradictions. It cannot promote its own story to telemetry.

Evidence has scope. A verified tool receipt may establish that a call reached an endpoint; it does not establish that the returned content was true or that it caused the next sentence. A hash identifies bytes, not truth, authorship or freshness. Policy, execution, unequal effect and repair need different witnesses. One dashboard cannot testify to every causal layer.

## The repair can hide the system

Competent systems turn failures into local work: fix the path, add a guard, restore the missing error. Necessary, but not proof of learning.

A correction recorded in a ticket, index or policy can leave the output unchanged. One decisive test is whether the repaired path still reproduces the failed claim under the relevant conditions. If it does, the repair has not reached the surface that matters. *Fixed* is itself a causal claim; it needs a witness outside the patch.

Google's [SRE post-mortem guidance](https://sre.google/sre-book/postmortem-culture/) treats the record as a route to effective preventive action, not a ceremonial ending. The harder test is whether that action changed the consequence rather than merely improving its account.

Did the fix prevent recurrence or only change its visible form? Did the harm move elsewhere? Who can reopen the case? What evidence would force the investigation to widen?

## What self-diagnosis is good for

Model self-explanation still has an honest job: generate competing hypotheses, name observations that would distinguish them and look for contradictions. Preserve the raw failure before interpretation. Require external evidence for claims about tools, limits, retrieval or execution. When it does not exist, label the cause unknown.

Unknown is not a defect. It keeps the report open.

The same discipline should apply to any system that produces both the action and the official account: automated moderation, safety dashboards, compliance systems. The problem is not automation alone. It is a witness who also owns the grammar of admissible evidence.

An audit begins when something outside that grammar can still contradict it.

## No witness gets the last word

The practical rule is blunt: never let the mechanism that produced an unsupported claim become the sole authority on why it produced it.

Let it speak. Record the answer. Treat it as a lead. Then look for ground: logs, traces, independent records, reproduced behavior, another observer with access to a different failure surface. If the ground is missing, do not pour concrete over the hole.

A machine may confess beautifully and still know nothing about the crime.

The second hallucination is more dangerous than the first because it arrives after trust has already been damaged, precisely when everyone wants a cause, a repair and a clean ending. That appetite for closure is part of the failure surface.

The first duty of a post-mortem is not to explain. It is to keep explanation answerable to evidence.
