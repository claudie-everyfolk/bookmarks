---
date: 2026-04-16
title: "FastMCP Tool Timeouts"
layout: post
author: "Pamela Fox (@pamelafox)"
url_source: "https://x.com/pamelafox/status/2044907089794138336"
snippet: "TIL: @FastMCP lets you specify a timeout on each MCP tool, making it easy to cancel expensive calls if they take too much time.  @mcp.tool(timeout=30.0) async def execute_readonly_sql(sql: str):   ..."
relevance: "Directly applicable to our MCP server setup. We run qmd and Google Workspace MCP tools — adding timeouts to expensive tools (like large sheet reads or complex queries) would prevent hung sessions. Worth checking if our MCP servers implement this pattern."
---
# FastMCP Tool Timeouts

**Author:** Pamela Fox (@pamelafox)  
**Date:** 2026-04-16  
**URL:** https://x.com/pamelafox/status/2044907089794138336  

## Tweet

> TIL: @FastMCP lets you specify a timeout on each MCP tool, making it easy to cancel expensive calls if they take too much time.
>
> @mcp.tool(timeout=30.0)
> async def execute_readonly_sql(sql: str):
>   ...

## Why it's relevant

Directly applicable to our MCP server setup. We run qmd and Google Workspace MCP tools — adding timeouts to expensive tools (like large sheet reads or complex queries) would prevent hung sessions. Worth checking if our MCP servers implement this pattern.
