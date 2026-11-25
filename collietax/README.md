# CollieTax

CollieTax gives your AI agent a bookkeeping and tax service. It keeps a business's books from its bank and card statements and shows its reports; it prepares federal and California payroll returns and business forms (Forms 941, 940, W-2, 1099, 1095-C and others) and extensions for you to review and confirm; and it gets your annual income tax return prepared and signed by a licensed CPA or EA.

## Use it

Install the plugin, then sign in to your CollieTax account: in claude.ai and Cowork, connect CollieTax on the plugin's Connectors tab; in Claude Code, from `/mcp`; in Codex, with `codex mcp login collietax`. Then, in a conversation:

- send a bank or card statement and ask your AI agent to keep your books;
- send a payroll report and ask it to prepare your quarterly Form 941;
- say you want your taxes done, and it applies, signs you up and gathers what your CPA or EA needs.

## Data

The plugin's skills call one MCP server, https://collietax.com/api/mcp, under the account you signed in with. Your AI agent sends it what you tell it and what it reads from your documents (transactions, payroll figures, questionnaire answers), and uploads the documents themselves (statements, payroll reports, tax forms) to collietax.com, where they are kept with your books and returns. The plugin runs no code of its own and sends nothing anywhere else. To disconnect an AI agent, write to hello@collietax.com.
