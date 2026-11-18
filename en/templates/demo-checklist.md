[RU](../../templates/demo-checklist.md) / **EN** · [← Resources](../USEFUL.md)

# Demo checklist

Use this before showing a product to someone without an account. Record the result, version and method for each check.

## Entry and explanation

- [ ] The demo is accessible from the first screen without registration or a secret.
- [ ] The user understands whether they are seeing sample content or a real action.
- [ ] Examples are labelled rather than presented as real messages, payments or model replies.
- [ ] Exiting the demo and connecting a personal account is clear.

## Data and actions

- [ ] Sample data is fictional.
- [ ] Network dependencies are explicit; an offline demo makes no network requests.
- [ ] Example buttons do not send real messages or perform real actions without an explicit transition and confirmation.
- [ ] Sample settings do not overwrite personal keys, servers or preferences.
- [ ] Demo conversations are not included in real-model requests after switching.
- [ ] Repeated entry and exit leave no unfinished operation or mixed state.

## Usable outcome

- [ ] The main journey works without a presenter explaining each step.
- [ ] Main actions are accessible by keyboard.
- [ ] Exit and settings remain visible at another display scale.
- [ ] The report states what these checks do not cover.

## Example results record

| Check | Method | Record |
|---|---|---|
| No model required | Start with a clean application profile and enter demo | No server or key was needed |
| No AI request | Replace the network function with a call counter during the check | Zero calls |
| Settings preserved | Compare settings before entering and after leaving | Key and server address unchanged |
| Demo/model boundary | Send a demo message, exit and open normal chat | Demo messages cleared |

This covers part of [Purrsonal's behavior](../notes/offline-demo.md). It does not replace testing a real model or email delivery.

[MIT license](../../templates/LICENSE)
