# Instalação rápida

Prefeitura SP São Paulo: Recursos de Multas é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_pref_sp_sao_paulo_recursos`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Prefeitura SP São Paulo: Recursos de Multas` / `https://api.mcp.ai/p_pref_sp_sao_paulo_recursos`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "pref_sp_sao_paulo_recursos": { "type": "http", "url": "https://api.mcp.ai/p_pref_sp_sao_paulo_recursos" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=pref_sp_sao_paulo_recursos&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wcmVmX3NwX3Nhb19wYXVsb19yZWN1cnNvcyJ9)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "pref_sp_sao_paulo_recursos": { "url": "https://api.mcp.ai/p_pref_sp_sao_paulo_recursos" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=pref_sp_sao_paulo_recursos&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_pref_sp_sao_paulo_recursos%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "pref_sp_sao_paulo_recursos": { "type": "http", "url": "https://api.mcp.ai/p_pref_sp_sao_paulo_recursos" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_pref_sp_sao_paulo_recursos
```

Dúvidas? [pref_sp_sao_paulo_recursos@mcp.ai](mailto:pref_sp_sao_paulo_recursos@mcp.ai)
