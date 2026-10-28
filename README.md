# 8hub for Claude

Claude Code plugin that connects Claude to [8hub](https://app.hub-test.8seneca.com/hub): People, Hub and Finance.

Tools: `whoami`, `list_operations`, `call_operation` (read), `change_operation` (write).

## Install

```
/plugin marketplace add 8seneca-hub/8hub-claude-plugin
/plugin install 8hub@8seneca-hub
```

Then run `/mcp`, pick **8hub** and sign in with your 8seneca Google account. 8hub shows what Claude asks to
read; untick anything you don't want to share.

## What Claude can and cannot do

- It acts as you: it sees and does only what your 8hub account can, in the areas you ticked on the consent page
  (for example, request leave, answer a demand).
- Claude Code asks before each `change_operation` call unless you allow it.
- It never passes a hard stop (final approvals, releasing money) and never sees salary, pay, bonus or cost.
- Disconnect any time in 8hub: *My settings › Connected apps*. Access ends after 90 days at most.

It connects to the test environment (`https://app.hub-test.8seneca.com`).
