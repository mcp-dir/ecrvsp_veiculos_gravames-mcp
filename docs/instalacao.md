# Instalação detalhada

ECRVSP Veículos: Gravames é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_ecrvsp_veiculos_gravames`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_ecrvsp_veiculos_gravames` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_ecrvsp_veiculos_gravames` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_ecrvsp_veiculos_gravames` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.ecrvsp_veiculos_gravames` (ou `servers.ecrvsp_veiculos_gravames` no VS Code) do config do cliente e reinicie.
