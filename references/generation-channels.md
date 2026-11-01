# Generation channels

Load this file when dispatching any image or video generation work.

Facts here change often. Re-probe before assuming any channel is available.
Availability is per-session, not permanent — a channel that worked yesterday may not
be mounted today.

## Rules that hold regardless of state

- ImageGen and VideoGen are **banned**. Do not call them.
- Subagents must run the same model as the main agent.
- Check balance before any paid run. There is no trial-and-error budget.
- If a channel is not mounted, stop and report the blocker. Do not route around it.

## Probing

A tool appearing in the available tool list does **not** mean the channel works.
Tool definition present is not the same as channel usable. Probe by making a zero-cost
call and reading the error:

- auth or temp-key error → mounted
- "not found in the deferred tools index" → not mounted

## Historical notes

These were true at some point and are recorded only to bound the search space.
Verify before relying on any of them.

- Miora was reachable only in design mode on some sessions, and not on others.
  It does not appear in the connector list, so there is no switch to flip —
  mode is the only variable.
- AgentEarth was a backup image-to-video path, with first/last frame locking on
  some models, credited separately from WorkBuddy.
- ai-hive was another image-to-video path with its own wallet.

Do not treat these as current state. Probe first.
