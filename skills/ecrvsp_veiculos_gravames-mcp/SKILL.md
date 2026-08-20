---
name: ecrvsp_veiculos_gravames-mcp
description: Skill da REST API do ECRVSP Veículos: Gravames na MCP.AI: 1 endpoint em /api/ecrvsp_veiculos_gravames. ECRVSP Veículos: Gravames, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# ECRVSP Veículos: Gravames — REST API skill

Você tem acesso à **ECRVSP Veículos: Gravames** REST API na MCP.AI.

> ECRVSP Veículos: Gravames, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/ecrvsp_veiculos_gravames
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/ecrvsp_veiculos_gravames/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"a3":"...","a3_pin":"...","login_cpf":"...","login_senha":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/ecrvsp_veiculos_gravames/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `ecrvsp_veiculos_gravames_consultar`

ECRVSP Veículos: Gravames, consulta em fonte oficial. _(POST /api/ecrvsp_veiculos_gravames/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `a3` | string | Sim | Parâmetro de consulta "a3". |
| `a3_pin` | string | Sim | Parâmetro de consulta "a3_pin". |
| `login_cpf` | string | Sim | Parâmetro de consulta "login_cpf". |
| `login_senha` | string | Sim | Parâmetro de consulta "login_senha". |
| `chassi` | string | Não | Parâmetro de consulta "chassi". |
| `placa` | string | Não | Parâmetro de consulta "placa". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_ecrvsp_veiculos_gravames` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
