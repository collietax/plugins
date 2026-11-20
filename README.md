# CollieTax plugins

The CollieTax plugin gives your assistant CollieTax's bookkeeping and tax service: https://collietax.com. It brings the CollieTax connector and its skills; what it sends where is in [its README](collietax/README.md).

## Install

- **claude.ai and Claude Cowork**: in Customize > Plugins, choose Add > Add marketplace and enter `collietax/plugins`, and turn on Sync automatically so new versions arrive by themselves. Add the CollieTax plugin, then add and connect CollieTax on its Connectors tab. It reaches Claude Code on the same account too.
- **Claude Code**:

      claude plugin marketplace add collietax/plugins
      claude plugin install collietax@collietax

  Then run `/reload-plugins` and sign in to CollieTax from `/mcp`. To get new versions by themselves, turn on auto-update for the collietax marketplace under `/plugin` > Marketplaces.
- **Codex**:

      codex plugin marketplace add collietax/plugins
      codex plugin add collietax@collietax
      codex mcp login collietax

Any other assistant: https://collietax.com/mcp/START.md.

This repository is built from CollieTax's source; changes made here are replaced by the next release.
