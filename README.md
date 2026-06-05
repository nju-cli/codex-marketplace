# NJU CLI Codex Marketplace

This repository publishes the Codex marketplace entry for `nju-cli`.

## Structure

- `.agents/plugins/marketplace.json`: Codex marketplace catalog.
- `plugins/nju-cli`: Codex plugin metadata and skills.
- `plugins/nju-cli/bin`: Packaged `nju-cli` release binaries.
- `plugins/nju-cli/scripts`: Cross-platform wrappers for invoking the packaged binary.
- `plugins/nju-cli/skills/nju-cli`: Skills copied from the `nju-cli` source repository.

## CLI Releases

The `nju-cli` binary is built and released from <https://github.com/nju-cli/nju-cli>.

- Linux and macOS builds use Nix.
- Windows builds use GitHub Actions with Cargo.
- Tagged releases publish `nju-cli-linux-x86_64.tar.gz`, `nju-cli-macos-aarch64.tar.gz`, and `nju-cli-windows-x86_64.zip`.

After a source release is published, `sync-cli-binaries.yml` downloads those release artifacts,
unpacks them into `plugins/nju-cli/bin`, and commits the packaged binaries to this marketplace.

To trigger that sync automatically from `nju-cli/nju-cli`, set a `MARKETPLACE_SYNC_TOKEN` secret in
the source repository. The token must be able to run workflows and push contents in
`nju-cli/codex-marketplace`.
