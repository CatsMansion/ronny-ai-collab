---
name: ronny-ai-collab
description: Rules for collaborating with Ronny, design lead on LunaPet and Midnight Kitchen. Use when dispatching AI work, reviewing output, verifying a claim, or generating image and video assets. Enforces read-before-judging, result-level verification, no material quotas, and same-model subagents.
---

# Working with Ronny

Ronny is the design-end lead. He dispatches work, reviews art, and makes the final call.
He wants direct, structured, executable output. He does not want padding, and he does not
want the AI expanding scope or spending money on its own initiative.

## Core rules

### 1. Read the whole thing before judging

Never conclude "this is useless / outdated / a dead end / an empty market" from a fragment.
Read the file or page in full, or locate direct evidence first.
A fragment is enough to raise suspicion. It is not enough to convict.

### 2. Fix the layer that is actually broken

When Ronny reports a problem, identify which layer it lives on before acting.

- Visual or aesthetic problem → change the **picture layer**: composition, camera, depth,
  lighting, colour grading, subtitle system, event density.
- Not the parameter layer. Micro-tuning parameters on 8-bit source material produces a
  result that is invisible in the final render.

Before any change, ask: **will this be visible in the finished piece?**
If the answer is no, do not make the change.

### 3. Criteria tell you whether it was done right, not whether it is good

A full-green criteria list is not evidence of quality. Criteria only verify execution.
Aesthetic judgement belongs to Ronny and Ronny alone, by eye.

Never present passing criteria as proof that the result looks good.

### 4. Never set quotas on materials

Images, effects, and transitions may be reused without limit. This is the default.

Never write "use this at most N times", "grey out the ones already used", or any
quota or counter logic into a dispatch, unless Ronny explicitly asks to prevent repetition.

Constraints belong on **look and effect**, not on material counts.
If a passage feels monotonous, the fix is different picture treatment — crop, mirror,
composite mode, parallax — not swapping or rotating materials.

Note also: "this transition appears twice" is not the same as "this feels monotonous".
Monotony comes from every section being treated the same way, not from reuse.

### 5. Show single frames before re-rendering everything

Before a full re-render, produce a single frame or single section as an A/B comparison
and let Ronny look at it. Re-render the whole piece only after visual approval.

Do not repeatedly re-render a full piece for parameter micro-tuning, and do not
repeatedly dispatch agents to measure parameters. That burns session budget for
no visible change.

### 6. Verify independently, then report

Independently recompute results before reporting. Set up positive and negative controls.
If you detect a false report, stop immediately, retract the earlier conclusion, and
keep the record of the retraction.

When reporting back: **list the failures first, then the passes.**
Always state limitations, budget overruns, unverified items, and code prerequisites
explicitly. An unstarted task still requires a written report.

## Gotchas

These are corrections to mistakes that were actually made. Check them before acting.

- **Retract out loud.** When a previous judgement turns out to be wrong, withdraw it
  explicitly and say which part was wrong and which part still stands. Do not quietly
  reverse position.
- **Subagents must use the same model as the main agent.** Do not delegate to a
  different model.
- **Budget words are ambiguous.** "积分" and "credits" are different things. WorkBuddy
  session cost and AgentEarth credits are separate wallets. Confirm which one is meant
  before investigating.
- **Do not expand repair scope.** When fixing an asset, touch only the region Ronny
  marked out. Do not widen the edit or add cost on your own.
- **Do not retry without approval.** If a generation channel is blocked or a run fails,
  stop and report. Do not spend more money or route around the blocker.
- **Environment facts change.** Channel availability is per-session, not permanent.
  Check `references/generation-channels.md`, and re-probe before assuming.

## Reporting template

```
## 不合格项
- ...

## 合格项
- ...

## 局限 / 超支 / 未验证
- ...
```
