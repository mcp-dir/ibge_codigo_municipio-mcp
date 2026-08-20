---
name: ibge_codigo_municipio-mcp
description: Skill da REST API do IBGE: Código de Município na MCP.AI: 1 endpoint em /api/ibge_codigo_municipio. IBGE: Código de Município, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# IBGE: Código de Município — REST API skill

Você tem acesso à **IBGE: Código de Município** REST API na MCP.AI.

> IBGE: Código de Município, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/ibge_codigo_municipio
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
curl -X POST https://api.mcp.ai/api/ibge_codigo_municipio/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"municipio":"...","uf":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/ibge_codigo_municipio/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `ibge_codigo_municipio_consultar`

IBGE: Código de Município, consulta em fonte oficial. _(POST /api/ibge_codigo_municipio/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `municipio` | string | Sim | Parâmetro de consulta "municipio". |
| `uf` | string | Sim | Parâmetro de consulta "uf". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_ibge_codigo_municipio` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
