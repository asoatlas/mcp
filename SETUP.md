---
name: aso-atlas-setup
description: Connect the ASO Atlas MCP server. Use when the aso-atlas plugin was just installed, when ASO Atlas tools return 401 or 402, or when the user asks how to sign in to ASO Atlas.
---

# Connecting ASO Atlas

The plugin points at `https://asoatlas.com/mcp`. Nothing to install: the server is hosted.

1. On first use the client opens an ASO Atlas consent screen in the browser (OAuth 2.1). Sign in or create an account, approve, done.
2. If the client runs on a server or in a container where the OAuth callback cannot reach it, create a personal access token under **Settings → Connect your AI** on asoatlas.com and send it as `Authorization: Bearer <token>` instead.
3. A `402` reply means the account has no active subscription. Tell the user so and that the subscription is managed on asoatlas.com; do not push an upgrade.

Full guide: https://asoatlas.com/docs/connect-your-ai
