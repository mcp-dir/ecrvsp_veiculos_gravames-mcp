# Instalação rápida

ECRVSP Veículos: Gravames é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_ecrvsp_veiculos_gravames`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `ECRVSP Veículos: Gravames` / `https://api.mcp.ai/p_ecrvsp_veiculos_gravames`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "ecrvsp_veiculos_gravames": { "type": "http", "url": "https://api.mcp.ai/p_ecrvsp_veiculos_gravames" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=ecrvsp_veiculos_gravames&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9lY3J2c3BfdmVpY3Vsb3NfZ3JhdmFtZXMifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "ecrvsp_veiculos_gravames": { "url": "https://api.mcp.ai/p_ecrvsp_veiculos_gravames" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=ecrvsp_veiculos_gravames&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_ecrvsp_veiculos_gravames%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "ecrvsp_veiculos_gravames": { "type": "http", "url": "https://api.mcp.ai/p_ecrvsp_veiculos_gravames" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_ecrvsp_veiculos_gravames
```

Dúvidas? [ecrvsp_veiculos_gravames@mcp.ai](mailto:ecrvsp_veiculos_gravames@mcp.ai)
