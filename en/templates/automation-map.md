[RU](../../templates/automation-map.md) / **EN** · [← Resources](../USEFUL.md)

# Automation map

Describe the manual process first. Start with a clear step and a result you can verify.

## Fill in

**Process:** [name]

**Trigger:** [time, event or human action]

**Inputs:** [source; required fields; who keeps them current]

| Step | Today | After the change | Who verifies the result |
|---|---|---|---|
| 1 | [action] | [action] | [role] |
| 2 | [action] | [action] | [role] |
| 3 | [action] | [action] | [role] |

**Output:** [what is created, where it goes and how completion is recognised]

**Human confirmation:** [actions requiring approval]

**Repeated trigger:** [what happens if the same event arrives twice]

**Source failure:** [unavailable source, empty response or invalid data]

**Manual fallback:** [how to complete the task while automation is unavailable]

**Measuring value:** [before/after metric, observation period and person collecting data]

## Example: a daily team summary

**Trigger:** an agreed time at the end of the working day.

**Inputs:** appointments, cancellations and unfinished tasks from the working system.

**Output:** one summary in the agreed channel, with the reporting period and data status.

**Decide first:** timezone, unavailable-source labels, who checks the first report and how to prevent duplicates.

In [SMILE TALK](../cases/smile-talk.md), the summary arrived in Telegram at 19:30. This illustrates a workflow; it does not promise a ready integration for another team. Time savings were not quantitatively measured.

[MIT license](../../templates/LICENSE)
