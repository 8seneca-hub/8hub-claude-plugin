# 8hub for Claude

Use Claude as your 8hub assistant: ask in plain words, and Claude reads and acts in
[8hub](https://app.hub-test.8seneca.com/hub) (People, Hub, Finance) as you, with your own permissions.

## Set up (2 minutes, once)

1. In Claude Code, add the marketplace and install the plugin:

   ```
   /plugin marketplace add 8seneca-hub/8hub-claude-plugin
   /plugin install 8hub@8seneca-hub
   ```

2. Run `/reload-plugins`.
3. Run `/mcp`, pick **plugin:8hub:8hub**, choose **Authenticate**.
4. Your browser opens 8hub. Sign in with your 8seneca Google account.
5. On the consent page keep the boxes ticked (read **and** make changes) and press **Allow**.
   Untick an area only if you don't want Claude to touch it.
6. Back in Claude Code you see `Authentication successful. Connected to plugin:8hub:8hub.`

Check it worked: ask Claude **"who am I in 8hub?"**

## Try it

Just ask. Examples:

| You say | Claude does |
|---|---|
| "How many leave days do I have left?" | Reads your balance |
| "Request leave on 30/10, full day, I got sick" | Checks the types, previews, asks you to confirm, sends |
| "Show my pending requests" | Lists them with status and approver |
| "Withdraw my leave request L-2026-0314" | Confirms, then withdraws |
| "Who is off in my team this week?" | Reads the team calendar |
| "What demands are waiting for me?" | Lists them |
| "Approve Lan's leave for Friday" (team lead) | Shows the request, asks you to confirm, approves |
| "Void invoice INV-0042" (finance) | Prepares it, then gives you the 8hub link to confirm the void yourself |

Claude asks every choice as a question with options (leave type, approver, CC, final "Send it").
Press **Enter** to take the recommended option, or pick another with the arrow keys.

Nothing is sent before you confirm. After sending, Claude gives you the code (for example `L-2026-0314`) and
where to see it in 8hub. Leave requests are under **My leave**, not My attendance.

## What Claude can and cannot do

- It acts as you: it can do what your 8hub account can, in the areas you ticked, and nothing more.
- Hard stops (final approvals, releasing money, hiring, leavers, closing a project): Claude prepares them and gives
  you a link; you finish them in 8hub with your own confirmation.
- It never sees salary, pay, bonus or cost.
- Disconnect any time in 8hub: **Connected apps** ([/settings/me/apps](https://app.hub-test.8seneca.com/settings/me/apps)). Access ends after 90 days at most.

## Troubleshooting

| Problem | Fix |
|---|---|
| Claude says it can only read | You signed in before writes existed, or unticked "make changes". `/mcp` → **plugin:8hub:8hub** → clear authentication → **Authenticate** again |
| `Authentication failed` / tools missing | `/plugin marketplace update 8seneca-hub`, `/reload-plugins`, then `/mcp` → Authenticate |
| `marketplace name already exists` | Remove the old one: `/plugin marketplace remove <name>`, then add again |
| A request is not in 8hub | Ask Claude "show my leave requests"; look in **My leave** |

It connects to the test environment (`https://app.hub-test.8seneca.com`).

## Update

```
/plugin marketplace update 8seneca-hub
/reload-plugins
```
