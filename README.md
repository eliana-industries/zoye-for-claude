# Zoye for Claude

Work with your Zoye business data from Claude: contacts, leads, deals, tasks, meetings, notes and invoices. This plugin connects Claude to Zoye's own MCP server and adds skills that teach Claude the everyday Zoye flows.

It works in Claude (web, desktop and mobile), Cowork and Claude Code.

## What you get

- **Zoye connector** (`zoye-data`): Zoye's remote MCP server at `https://api.zoye.io/mcp`. You sign in on Zoye's consent screen and choose which workspaces Claude may use.
- **Skills:**
  - `working-with-zoye`: read the schema first, stay in the approved workspaces, and never make a change without your approval.
  - `daily-briefing`: today's meetings, due tasks, deals that need a move, and new leads.
  - `pipeline-review`: totals per stage, stuck deals, and proposed next steps.
  - `meeting-to-records`: meeting notes or a transcript into contacts, a deal, tasks and a linked note.
  - `follow-up`: a follow-up message drafted from the real history, sent from Zoye after you approve it.

## Setup

1. Install the plugin.
2. When Claude first uses a Zoye tool, sign in to Zoye and approve the workspaces to share.
3. Ask, for example: "What is on my plate today in Zoye?" or "Log this call in Zoye" with your notes.

You need a Zoye account. Create one at https://www.zoye.io.

## Data and safety

- The plugin contains no code: only skills (text) and the address of Zoye's connector. It runs no hooks, no local server and no scripts.
- Data moves only between Claude and Zoye's API at `api.zoye.io`, over HTTPS, under the sign-in you approved. Zoye's privacy policy: https://www.zoye.io/privacy
- Anything that deletes, sends, spends or changes access first shows you a preview and runs only after you approve it.
- You can revoke Claude's access at any time in Zoye.

## Support

hello@zoye.io · Documentation: https://www.zoye.io/docs/sync-users/claude · Terms: https://www.zoye.io/terms

## License

MIT, see [LICENSE](LICENSE).
