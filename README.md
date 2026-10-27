# Matcha Fucker

Finds the **Matcha** Roblox client on a Windows machine — by what it is, not what it's called.

Rename it, move it, update it, put it on a USB, bury it in a fake photo folder, or delete it.
It still gets found.

## Run it

Double-click `Matchafinder.exe`. It scans, prints a verdict, and writes the full report to a
`.json` (the path is shown at the end).

| verdict | meaning |
| --- | --- |
| `FUCKED` | Matcha is here — binary, payload, or execution record |
| `SUSPECT` | traces, a partial footprint, or a layer that couldn't fully see |
| `CLEAN` | nothing |

It pulls down the real `yara64.exe` automatically the first time it runs (recommended); without
it the built-in rules still work through a native fallback.

## What it checks

```
identity      sha256 · imphash · import-set          survives rename and rebuild
structure     the packer profile
filesystem    every volume, matched by content
runtime       running image + memory markers
injection     reflective loaders, hollowing, patched code
forensics     prefetch · amcache · bam · usn journal
persistence   autoruns · tasks · services · wmi
yara          built-in rule pack, real engine when available
```

## Credits

made by **@egotisticald1** (discord) · **github.com/ozrd**

DM me on discord for questions, or to add any other external client.

## Demo

<!-- demo video -->
