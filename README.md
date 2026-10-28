# 8hub for Claude

Claude Code plugin that connects Claude to [8hub](https://app.hub-test.8seneca.com/hub).

Tools: `feedback.list`, `feedback.get`, `feedback.setStatus`.

## Install

```
/plugin marketplace add 8seneca-hub/8hub-claude-plugin
/plugin install 8hub@8seneca
```

Claude Code asks for two values on enable:

- **8hub URL** — defaults to the test environment.
- **Access token** — an 8hub admin creates one in *Settings > Feedback > Claude access*. Tokens are scoped and expire (max 90 days).

Change them later with `/config`.
