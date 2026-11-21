# SOQVER

**Business facts AI agents can rely on.**

An agent that answers for a customer needs more than a page of text. It needs to know what a fact means, where it applies,
where it comes from and until when it holds. SOQVER publishes business facts that way, in the open format **SO4AG**.

## SO4AG, the open format

[![test](https://github.com/soqvercom/so4ag/actions/workflows/test.yml/badge.svg)](https://github.com/soqvercom/so4ag/actions/workflows/test.yml)

A reader of the format answers one question: **may this fact be used for this task at this time, and if not, why not?**
"Unknown" is a value of its own, never zero and never a guess. The format is free and needs no account.

```bash
git clone https://github.com/soqvercom/so4ag.git && cd so4ag && npm install
node validator/cli.mjs examples/valid/rental-first-party.json
python readers/python/so4ag_reader.py ask examples/valid/rental-first-party.json \
  --property refundableDeposit --scope vehicle_class=economy \
  --scope branch=https://rental.example/branches/prague-airport
```

| | |
|---|---|
| Repository | [soqvercom/so4ag](https://github.com/soqvercom/so4ag): specification, JSON Schema, profiles, validator, readers in JavaScript and Python |
| Guide for developers | https://soqver.com/developers |
| Specification 0.1 | https://soqver.com/spec/so4ag/0.1/ |
| Conformance suite | https://soqver.com/spec/so4ag/0.1/conformance/ (plain JSON, for anyone who writes a reader) |
| JSON-LD mapping | https://soqver.com/spec/so4ag/0.1/jsonld |
| Online validator | https://soqver.com/validator |
| MCP server (read-only) | `https://soqver.com/mcp`, in the official MCP Registry as `com.soqver/so4ag` |
| API (read-only, no account) | https://soqver.com/api/v1/sources |

## For businesses

- [Free website audit](https://soqver.com/audit): what can an agent read on your website today?
- [Prepare a source](https://soqver.com/start): your facts, confirmed by you, published in SO4AG.
- [What works today](https://soqver.com/status), in one table.

## Take part

Found a fact the format cannot express, or two readers that disagree? Open an
[issue](https://github.com/soqvercom/so4ag/issues) or a [discussion](https://github.com/soqvercom/so4ag/discussions).
How the format changes: [CONTRIBUTING](https://github.com/soqvercom/so4ag/blob/main/CONTRIBUTING.md).

[soqver.com](https://soqver.com) · info@soqver.com
