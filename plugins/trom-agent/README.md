# trom-agent

Trom Agent is your TeensyROM companion inside Claude Code. Type `/trom` and ask for what you want in plain words: play something, build a set, tour your library, or sort out your setup. It does the work through [Trom Terminal](https://github.com/MetalHexx/TeensyROM-Suite/blob/main/docs/trom-terminal.md), and installs [TeensyROM Suite](https://github.com/MetalHexx/TeensyROM-Suite) for you if you don't have it yet.

## What it does

- **Play and shuffle:** games, SID tunes, demos and images on your real C64, by name, artist or theme, with a little about what is playing.
- **Timed sets:** a DJ-style set that runs for the time you choose and moves on by itself.
- **Library tours and curation:** browse your library folder by folder, search it, favorite what you love and ban the stinkers.
- **Copy files and watch folders:** send files to your cart or bring them back, and set up a folder that sends whatever lands in it to your cart.
- **Themes:** set the colors of your C64's menu, from a shipped theme or one of your own.
- **Trom UI and Trom Terminal:** open Trom UI in your browser, or Trom Terminal's guided menu in a new terminal window, with a short tour if you want one.
- **Install and update the suite:** installs TeensyROM Suite from its newest release (with Homebrew on a Mac), and offers the update when a new release is out.
- **Setup doctor:** Virtual Travis, an AI stand-in modeled on the support Travis Smith, who created the TeensyROM, gives its users, checks Trom Terminal, Trom API, Trom UI, your cart and your index, and walks you through the fixes. He is not the real Travis.

## Start it

Install the plugin from the [marketplace](../../README.md), then type:

```
/trom-agent:trom
```

`/trom` starts the same skill where Claude Code accepts the short name. Trom Agent starts only when you run the command; it does not start on its own.

## How it works

The plugin drives your carts only through Trom Terminal (`trom`). It does not talk to the TeensyROM hardware or Trom API directly. Starting a session resets your cart to its menu, which stops whatever is running. It asks before it copies files, changes your setup or installs anything. It knows what is playing only from what it launched itself, not from a report by the device, so it can be out of date if you launch from Trom UI or the menu.

## Where the source lives

This plugin is a copy of the package in TeensyROM Suite at [`src/plugins/trom-agent/`](https://github.com/MetalHexx/TeensyROM-Suite/tree/main/src/plugins/trom-agent), published with each suite release and versioned with it. The copy is not a rewrite: if you want to change the skill, make the change in TeensyROM-Suite first, then copy it here. Keep the two trees identical.
