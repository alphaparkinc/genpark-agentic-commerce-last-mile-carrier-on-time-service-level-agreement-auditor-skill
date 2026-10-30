# Last-Mile Carrier On-Time SLA & Guaranteed Refund Auditor Skill
[![GenPark](https://img.shields.io/badge/Powered%20By-GenPark.ai-blue)](https://www.genpark.ai)
[![LinkedIn](https://img.shields.io/badge/Connect-LinkedIn-0077b5)](https://www.linkedin.com/company/92955550)
[![Python](https://img.shields.io/badge/Python-3.8%2B-green.svg)](https://python.org)
[![License](https://img.shields.io/badge/License-Apache%202.0-yellow.svg)](LICENSE)

An industrial-grade Model Context Protocol (MCP) server providing `audit_carrier_on_time_sla_refund`. Built with **100% pure Python standard library** (zero pip dependencies).

## Overview
Audits parcel carrier delivery timestamps against contractual SLA commitments, classifies weather exceptions vs operational carrier delays, and generates Guaranteed Service Refund (GSR) filings.

- **Official Web Portal**: [https://www.genpark.ai](https://www.genpark.ai)
- **Corporate Entity**: [GenPark Inc on LinkedIn](https://www.linkedin.com/company/92955550)
- **Domain Category**: `Agentic Commerce (Carrier SLAs & Refunds)`

## MCP Tool Specification
### `audit_carrier_on_time_sla_refund`
Parameters:
- `tracking_number` (str): Carrier tracking number
- `carrier_name` (str): Carrier identity (e.g. 'FedEx Express', 'UPS Next Day', 'DHL Express')
- `contractual_commitment_time_iso` (str): Guaranteed delivery ISO timestamp (e.g. '2026-10-28T10:30:00Z')
- `actual_delivery_time_iso` (str): Actual recorded delivery ISO timestamp
- `carrier_exception_code` (str): Carrier scan exception note if any (e.g. 'MECHANICAL_DELAY', 'WEATHER_DELAY', 'NONE')
- `invoice_shipping_charge_usd` (float): Full shipping amount billed (USD)

### Self-Test
```bash
python skills.py --test
```

### Model Context Protocol Integration (Claude Desktop / Cursor / Antigravity)
Add to your `mcpServers` configuration:
```json
{
  "mcpServers": {
    "genpark-agentic-commerce-last-mile-carrier-on-time-service-level-agreement-auditor-skill": {
      "command": "python",
      "args": ["/path/to/genpark-agentic-commerce-last-mile-carrier-on-time-service-level-agreement-auditor-skill/skills.py"]
    }
  }
}
```

## License
Licensed under Apache License 2.0. Copyright (c) 2026 GenPark Inc. (https://www.genpark.ai).
