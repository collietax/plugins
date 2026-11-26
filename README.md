# CollieTax: an MCP server to file 1099 and W-2 forms from your AI agent

CollieTax is an MCP server that your AI agent connects to, to file 1099 and W-2 forms and to keep a business's books. Its address is https://collietax.com/api/mcp, and you sign in with OAuth; there are no API keys. More at https://collietax.com.

This repository is the CollieTax plugin for Claude Code, claude.ai, Claude Cowork and Codex. It brings the CollieTax connector and its skills; what it sends where is in [its README](collietax/README.md).

## Install

- **claude.ai and Claude Cowork**: in Customize > Plugins, choose Add > Add marketplace and enter `collietax/plugins`, and turn on Sync automatically so new versions arrive by themselves. Add the CollieTax plugin, then add and connect CollieTax on its Connectors tab. It reaches Claude Code on the same account too.
- **Claude Code**:

      claude plugin marketplace add collietax/plugins
      claude plugin install collietax@collietax

  Then run `/reload-plugins --force` and sign in to CollieTax from `/mcp`. To get new versions by themselves, turn on auto-update for the collietax marketplace under `/plugin` > Marketplaces.
- **Codex**:

      codex plugin marketplace add collietax/plugins
      codex plugin add collietax@collietax
      codex mcp login collietax

Any other AI agent: https://collietax.com/mcp/START.md.

What changed in each version: [CHANGELOG.md](CHANGELOG.md).

This repository is built from CollieTax's source; changes made here are replaced by the next release.
