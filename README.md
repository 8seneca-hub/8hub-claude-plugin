# 8hub for Claude

Claude Code plugin that connects Claude to [8hub](https://app.hub-test.8seneca.com/hub): People, Hub and Finance.

Tools: `whoami`, `list_operations`, `call_operation`.

## Install

```
/plugin marketplace add 8seneca-hub/8hub-claude-plugin
/plugin install 8hub@8seneca-hub
```

Then run `/mcp`, pick **8hub** and sign in with your 8seneca Google account. 8hub shows what Claude asks to
read; untick anything you don't want to share.

## What Claude can and cannot do

- It sees only what you can see in 8hub, and only to read.
- It never approves, pays or changes anything, and never sees salary, pay, bonus or personal documents.
- Disconnect any time in 8hub: *My settings › Connected apps*. Access ends after 90 days at most.

The **8hub URL** option (default: the test environment) can be changed with `/config`.
