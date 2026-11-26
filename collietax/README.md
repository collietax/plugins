# CollieTax

CollieTax gives your AI agent a bookkeeping and tax service. It keeps a business's books from its bank and card statements and shows its reports; it prepares federal and California payroll returns and business forms (Forms 941, 940, W-2, 1099, 1095-C and others) and extensions for you to review and confirm; and it gets your annual income tax return prepared and signed by a licensed CPA or EA.

## Use it

Install the plugin, then sign in to your CollieTax account: in claude.ai and Cowork, connect CollieTax on the plugin's Connectors tab; in Claude Code, from `/mcp`; in Codex, with `codex mcp login collietax`. Then, in a conversation:

- send a bank or card statement and ask your AI agent to keep your books;
- send a payroll report and ask it to prepare your quarterly Form 941;
- say you want your taxes done, and it applies, signs you up and gathers what your CPA or EA needs.

## What it runs

The plugin holds three skills, which are instructions your AI agent reads, and the address of one MCP server, https://collietax.com/api/mcp. It has no scripts, hooks or programs. The skills tell your AI agent to:

- call the CollieTax MCP server's tools, under the account you signed in with;
- upload a document, when it has a shell that reaches collietax.com, by an HTTP PUT (for example with `curl`) to an upload URL on collietax.com that a CollieTax tool returned; without one, it gives you a CollieTax page where you pick the file yourself;
- read CollieTax's price list, https://collietax.com/pricing.md, when you ask what a service costs;
- update this plugin when a CollieTax tool result names a newer version of the skills, with the plugin commands of the app it runs in (in Claude Code, `claude plugin marketplace update` and `claude plugin update`; in Codex, `codex plugin marketplace upgrade` and `codex plugin add`), and tell you the steps it cannot do itself.

## Data

Your AI agent sends the CollieTax MCP server what you tell it and what it reads from your documents (transactions, payroll figures, questionnaire answers), and uploads the documents themselves (statements, payroll reports, tax forms) to collietax.com. The plugin sends nothing anywhere else.

CollieTax keeps your books until you delete them or close your account, and your tax returns, filed forms, their documents and your payment records for at least seven years. It sends a form or a return to the IRS, the Social Security Administration or a state agency only after you confirm or sign it. Its privacy policy, https://collietax.com/privacy, says what it collects, who receives it and how long it keeps it. To disconnect an AI agent, write to hello@collietax.com.

## Money

No CollieTax tool moves money. Money moves only when you act on a CollieTax page, signed in to your account:

- **Forms**: you read a batch of forms on its review page and select Confirm. Confirm sets aside the batch's fee, if it has one, from your CollieTax credits: a form the agency accepts spends its part, and a form it rejects, or a batch you withdraw, gives it back. Only a confirmed batch is filed. A tax payment by bank withdrawal that a return carries, to the IRS or to California's EDD, uses the bank account you gave, and the agency takes it only after the return you confirmed is filed.
- **A tax return**: signing your engagement letter, which states the fee, the retainer and the final invoice, makes the retainer due. Your credits pay what they can, and an invoice asks for the rest; the final invoice comes as the letter says.
- **A bookkeeping plan**: you start or upgrade a plan on your Billing page, where the confirmation shows the price and that the plan renews each month, or CollieTax's team sets a plan you asked for there.
- **Credits**: you add them by paying an invoice, by card or by bank transfer.
