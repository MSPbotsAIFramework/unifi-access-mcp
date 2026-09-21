# unifi-access-mcp

Status: **empty scaffold** — created for [PRD-18940](https://app.clickup.com/t/PRD-18940).
Nothing is implemented yet; the design has not been written.

## What this repo is for

UniFi Access 门禁系统的 MCP server：供 agent 读取门禁数据/状态、执行开门等动作，注册进 mcp-service-gateway 的 vendor fleet

## The constraint that must not be lost

读写都要支持（read + action），且需求方明确要求一次性交付，不分阶段

This is recorded here because it is the part of the requirement most
easily lost between the ticket and the implementation.

## Branches

`main` only, on purpose — vendor MCP repos in this org are consumed by
`mcp-service-gateway`'s `vendor_deploy.py`, which clones the default
branch and never names a ref. Merging to `main` is what ships. Do not add
`INT` / `release` here without deciding what would deploy from them.
