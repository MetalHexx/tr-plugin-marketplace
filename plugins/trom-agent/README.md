# trom-agent

A Claude Code plugin that turns your coding agent into a companion for your C64 and TeensyROM. It plays music and demos on your device, tours and curates your library, and checks your setup.

## What it does

- **DJ and timed sets:** play music by artist or theme, or build a set that runs for a given length of time.
- **Library tours and curation:** browse your library folder by folder and pick what to play next.
- **Light doctor:** check that the `trom` CLI, the engine, and a device are online, and walk through common setup problems.
- **Install from source:** until a `trom` release exists, the skill can build `trom` from the TeensyROM-Web source.

## Start it

Install the plugin from the [marketplace](../../README.md), then type:

```
/trom-agent:trom
```

`/trom` starts the same skill where Claude Code accepts the short name. The companion starts only when you run the command; the agent does not start it on its own.

## How it works

The plugin drives the device only through the `trom` CLI. It does not talk to the TeensyROM hardware or the engine directly. It knows what is playing only from what it launched itself, not from a report by the device.

## Where the source lives

This plugin is a copy of the package in TeensyROM-Web at [`src/plugins/trom-agent/`](https://github.com/MetalHexx/TeensyROM-Web/tree/main/src/plugins/trom-agent). The copy is not a rewrite: if you want to change the skill, make the change in TeensyROM-Web first, then copy it here. Keep the two trees identical.
