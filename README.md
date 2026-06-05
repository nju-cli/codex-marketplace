# NJU CLI Codex Marketplace

This repository publishes the Codex marketplace entry for `nju-cli`.

## Structure

- `marketplace.json`: Codex marketplace catalog.
- `plugins/nju-cli`: Codex plugin metadata and skills.
- `plugins/nju-cli/skills/nju-cli`: Skills copied from the `nju-cli` source repository.

## CLI Releases

The `nju-cli` binary is built and released from <https://github.com/nju-cli/nju-cli>.

- Linux and macOS builds use Nix.
- Windows builds use GitHub Actions with Cargo.
- Tagged releases publish `nju-cli-linux-x86_64.tar.gz`, `nju-cli-macos-aarch64.tar.gz`, and `nju-cli-windows-x86_64.zip`.
