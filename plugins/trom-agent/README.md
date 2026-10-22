# trom-agent

Trom is your TeensyROM companion, a suite of tools to help you get the most out of your cart. This Claude Code plugin brings it into your coding agent, so you can run your C64 and TeensyROM setup by asking.

## What it does

- **Launch and shuffle:** play games, SID tunes, demos and images on your real C64, by name, artist or theme.
- **Timed sets:** build a DJ-style set that runs for a given length of time and advances on its own.
- **Library tours and curation:** browse your library folder by folder, search it, favorite what you love and ban the stinkers.
- **The web UI:** open the TeensyROM web UI in your browser, with a short tour of what it can do if you want one.
- **The command line:** a quick tour of `trom`, including its guided menu, which the agent can open in a separate terminal window.
- **Setup doctor:** Virtual Travis, an AI stand-in modeled on the support Travis Smith, who created the TeensyROM, gives its users, checks `trom`, the engine, the web UI, your device and your index, and walks you through the fixes. He is not the real Travis.
- **Install from source:** until a `trom` release exists, the skill can build `trom` and the web UI from the TeensyROM-Web source.

## Start it

Install the plugin from the [marketplace](../../README.md), then type:

```
/trom-agent:trom
```

`/trom` starts the same skill where Claude Code accepts the short name. Trom starts only when you run the command; the agent does not start it on its own.

## How it works

The plugin drives the device only through the `trom` CLI. It does not talk to the TeensyROM hardware or the engine directly. It opens the web UI in your browser, and the `trom` menu in a new terminal window when you ask. It knows what is playing only from what it launched itself, not from a report by the device, so it can be out of date if you launch from the web UI or the menu.

## Where the source lives

This plugin is a copy of the package in TeensyROM-Web at [`src/plugins/trom-agent/`](https://github.com/MetalHexx/TeensyROM-Web/tree/main/src/plugins/trom-agent). The copy is not a rewrite: if you want to change the skill, make the change in TeensyROM-Web first, then copy it here. Keep the two trees identical.
