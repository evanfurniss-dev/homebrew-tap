# Evan Furniss Homebrew packages

## Customer MCP Router

A local Glide connection manager for Claude Code and Codex. Each customer has a separate saved authorization. Each person signs in with their own Glide account.

Requires macOS and [Homebrew](https://brew.sh).

```sh
brew install evanfurniss-dev/tap/mcp-customer-router
mcp-customer-router service install --open
```

The second command starts the local dashboard and enables startup at login. Homebrew installs Node and the application. Customer data stays in `~/.mcp-customer-router`.

Update:

```sh
brew update
brew upgrade evanfurniss-dev/tap/mcp-customer-router
mcp-customer-router service restart
```

Start fresh Claude Code and Codex sessions after updating.

Remove the application:

```sh
mcp-customer-router service uninstall
brew uninstall mcp-customer-router
```

Saved customer data remains on disk.

[Source and usage](https://github.com/evanfurniss-dev/mcp-customer-router) · [Releases](https://github.com/evanfurniss-dev/mcp-customer-router/releases)

## Maintainers

Copy the generated formula from a tested router release into `Formula/mcp-customer-router.rb`. Review the release URL and SHA-256 before pushing. Follow the [release procedure](https://github.com/evanfurniss-dev/mcp-customer-router/blob/main/docs/RELEASING.md).
