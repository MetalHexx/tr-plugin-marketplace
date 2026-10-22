# tr-plugin-marketplace

Plugins that turn your coding agent into a companion for your C64 and [TeensyROM](https://github.com/SensoriumEmbedded/TeensyROM). This marketplace collects them in one place, so you can add it once and install what you want.

## Install in Claude Code

1. Add the marketplace:

   ```
   /plugin marketplace add MetalHexx/tr-plugin-marketplace
   ```

2. Install a plugin, for example `trom-agent`:

   ```
   /plugin install trom-agent@tr-plugin-marketplace
   ```

3. Start it by typing `/trom` (or `/trom-agent:trom`).

## Plugins

| Plugin | What it does | Needs |
|--------|--------------|-------|
| [`trom-agent`](plugins/trom-agent/README.md) | Plays music and demos, tours and curates your library, and checks your TeensyROM setup. | The `trom` CLI. The skill can build it from the [TeensyROM-Web](https://github.com/MetalHexx/TeensyROM-Web) source until a release exists. |

## Contributing

Plugins arrive by pull request. Each one is either:

- copied into this repo under `plugins/<name>/<harness>/`, or
- listed in this repo's catalog from its own repository, pinned to a fixed release (a tag or a commit). Never point at a moving branch.

### Layout

The layout is plugin first, then harness. Each plugin owns `plugins/<name>/`, with one subfolder per harness (for example `claude/` today, and `copilot-cli/` later). Each harness's catalog lives at the root path that harness reads.

### Review

`main` changes only by reviewed pull request.

## License

MIT. See [LICENSE](LICENSE).
