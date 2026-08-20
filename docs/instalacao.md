# Instalação detalhada

IBGE: Código de Município é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_ibge_codigo_municipio`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_ibge_codigo_municipio` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_ibge_codigo_municipio` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_ibge_codigo_municipio` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.ibge_codigo_municipio` (ou `servers.ibge_codigo_municipio` no VS Code) do config do cliente e reinicie.
