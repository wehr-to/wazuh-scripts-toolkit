# 🛡️ wazuh-scripts-toolkit

A collection of scripts, helpers, and automation tools for managing, tuning, and integrating Wazuh — an open source security monitoring platform.

This toolkit is designed for SOC analysts, security engineers, and homelabbers who want to automate Wazuh operations, debug rules, parse logs, and forward alerts with minimal friction.

## 📁 Toolkit Overview

| Folder              | Description                                                    |
|---------------------|----------------------------------------------------------------|
| `agent-management/` | Scripts to register, monitor, and maintain Wazuh agents        |
| `rule-debugging/`   | Tools to inject logs and test rule triggers                    |
| `log-parsing/`      | Parsers and search helpers for `alerts.json` and decoded logs  |
| `integrations/`     | Custom scripts for Slack, SIEM push, or webhook integrations   |
| `utilities/`        | Wazuh core management: restarts, clear queues, status checks   |
| `templates/`        | Starter config and rule XML templates                          |
| `docs/`             | Usage notes, API tips, and troubleshooting flows               |

## 🔧 Example Scripts

### 🚀 `agent-management/bulk-register-agents.sh`
Registers a list of hosts via Wazuh API or CLI.

### 🧪 `rule-debugging/test-log-injector.py`
Sends controlled logs into `/var/ossec/logs/active-responses.log` to test rule behavior.

### 🧵 `log-parsing/parse-alerts-json.py`
Pulls out severity, timestamp, rule ID, and message from `alerts.json` for triage.

### 🔔 `integrations/slack-alert-forwarder.py`
Pushes critical alerts to a Slack channel via webhook.

## 🧠 Ideal Use Cases

- Manage 10–500 agents at scale
- Debug Wazuh custom rules and decoders
- Pull insights from large alert files quickly
- Hook Wazuh into your existing alerting pipelines
- Build automation into a homelab or production SOC

## 📌 Requirements

- Python 3.8+
- Wazuh Agent or Manager (tested on v4.x)
- Access to `/var/ossec` and/or Wazuh API
- Optional: Slack webhook, ELK stack

## 🔐 Security Reminder

These scripts are meant for controlled environments and operational tuning. Always test in non-production systems before rolling changes live.

## 🤝 Contributions

Pull requests welcome — whether you’re adding decoders, API helpers, rule testers, or integrations.



