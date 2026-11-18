[RU](../../templates/release-card.md) / **EN** · [← Resources](../USEFUL.md)

# Clear release card

Copy the section below into a release description. File names must match the actual attachments.

## [Product] [version]

### What changed

- [Specific new behavior for the user]
- [Fixed issue and when it occurred]

### What to download

**Installer:** `[exact-file-name.exe]` for [OS and architecture].

**Checksum:** `[file name]`, if published.

**Source code:** files for developers; state clearly if they are not a ready-to-run application.

### First launch

1. [Install]
2. [First useful action]
3. [Settings needed for the user's task]

### Updating

[Close the old version? Are settings preserved? Does the data format change? How can the user return to an earlier version, if supported?]

### Limitations

[Missing features, external services required, installer signing status and material incompatibilities.]

### Feedback

[Bug report or feature request link]

## Example: Purrsonal 0.2.0

**Change:** a first-screen demo button requiring no model, key or network.

**File:** `Purrsonal-0.2.0-x64-Setup.exe`, Windows x64.

**First action:** click the kitten, then “Попробовать демо” (Try demo).

**Boundary:** replies are scripted; open-ended conversation requires a connected model.

[Full release →](https://github.com/r3in04ka-prog/purrsonal/releases/tag/v0.2.0)

[MIT license](../../templates/LICENSE)
