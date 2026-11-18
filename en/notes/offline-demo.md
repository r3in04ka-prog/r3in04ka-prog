[RU](../../notes/offline-demo.md) / **EN** · [← Resources](../USEFUL.md) · [Purrsonal case](../cases/purrsonal.md)

# A demo that needs no API key

**Purrsonal 0.2.0:** a specific onboarding decision you can adapt to another product.

## Problem and decision

Before connecting a model, visitors can see the kitten but cannot try the chat. Requiring a server, model and key makes first use depend on configuring an external service.

A separate mode with scripted replies lets visitors explore the interface without implying that those replies demonstrate model quality.

| Decision | Benefit | Tradeoff |
|---|---|---|
| One-button entry | Start without an account or model | Replies cover prepared scenarios only |
| Visible “no AI or internet” label | The reply's origin is clear | Demo and normal chat need separate explanations |
| Mode exists only for the current session | Personal server and key remain intact | Demo must be enabled again after restarting |
| Clear conversation when leaving | Examples stay out of real-model requests | The demo conversation cannot continue as a normal chat |

## Boundary

The message handler checks demo mode first and calls a scripted-reply function when enabled. A separate branch uses the model's network client. Replies are displayed as text, not executed as commands.

Application launching and reminders live in the Tasks tab (“Дела”). A demo reply explains where the button is rather than claiming the action has happened.

## Verification

In a check using real application windows, the network function is temporarily replaced with a call counter that also fails on attempted access. A demo message should produce a scripted reply and zero network calls.

Other checks compare saved settings before and after switching, verify the visible demo label and confirm conversation clearing before normal model use. These checks cover a specific application boundary, not all operating-system network activity or model quality.

## Implementation and reuse

- [Demo replies and network chat](https://github.com/r3in04ka-prog/purrsonal/blob/v0.2.0/src/core.cjs).
- [Mode separation in the main process](https://github.com/r3in04ka-prog/purrsonal/blob/v0.2.0/src/main.cjs).
- [Real-window checks](https://github.com/r3in04ka-prog/purrsonal/blob/v0.2.0/scripts/smoke.cjs).
- [Reusable demo checklist](../templates/demo-checklist.md).

[Download 0.2.0](https://github.com/r3in04ka-prog/purrsonal/releases/tag/v0.2.0), choose “Попробовать демо” (Try demo), then ask “Как добавить напоминание?” (How do I add a reminder?). The recorded app interface is in Russian.
