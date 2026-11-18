[RU](../../notes/mail-boundaries.md) / **EN** · [← Resources](../USEFUL.md) · [OpenPost case](../cases/openpost.md)

# An email client without a disk archive

**OpenPost 0.2.2:** what first-version constraints provide, and what they cost.

## Storage choice

The account and loaded messages live in process memory. No separate on-disk message archive is implemented. Users enter their password again after restarting; offline reading is unavailable.

This reduces the number of states to design and explain in a first version. It does not mean data cannot exist elsewhere: operating-system swap, memory dumps and the email provider remain relevant.

## Reading without changing the inbox

The client opens INBOX with `readonly=True` and fetches messages through `BODY.PEEK[]`. This version exposes no user actions for deleting mail or changing the server's read flag.

| Choice | Benefit for the initial workflow | Deferred capability |
|---|---|---|
| One account | Clear source and reply identity | Multiple-account management |
| Plain-text content | No need to execute HTML or load external images | Rich email layouts |
| No disk archive | No separate message database or migrations | Offline reading and saved history |
| Read-only inbox | First use excludes deletion and moving messages | Folders and server-state changes |

The illustration in a demo message is bundled with the application. It does not imply support for automatically fetching external images from real emails.

## Sending is a separate boundary

Real sending requires a connected account; the built-in demo mailbox does not send mail. Connections verify TLS certificates and the server hostname.

A connection failure after message transfer does not prove that the server rejected the message. The instructions therefore recommend checking delivery before manually sending again.

## Questions for a similar product

1. Where do passwords and messages live: memory, files, a database, system storage or a provider?
2. Which actions change server state?
3. What does the user see when delivery is uncertain?
4. Which familiar-looking features are actually absent?

## Sources

- [Mail transport, reading and sending](https://github.com/r3in04ka-prog/openpost/blob/v0.2.2/openpost/mail.py).
- [Demo data and interface](https://github.com/r3in04ka-prog/openpost/blob/v0.2.2/openpost/shell.py).
- [Features and limitations](https://github.com/r3in04ka-prog/openpost#readme).
- [Product brief template](../templates/product-brief.md).

This note describes specific architectural decisions; it is not an independent security assessment.
