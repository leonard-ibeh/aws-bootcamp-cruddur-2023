# Week 0 — Billing and Architecture Setup

## Objectives
- Configured local WSL2 development environment (replacing Gitpod to avoid paid tiers).
- Provisioned AWS CloudWatch Billing Alarms and SNS Notification Topics via AWS CLI.

## Key Technical Tasks Completed
1. **Local CLI Configuration:** Resolved system Python 3.14 package conflicts by installing the standalone AWS CLI v2 binary.
2. **Billing Alarm JSON:** Created `aws/json/alarm_config.json` with metric target `EstimatedCharges` and threshold set to `$1`.

## Obstacles & Solutions
- **Issue:** AWS CLI threw `badly formed help string` due to Ubuntu system-packaged Python conflicts.
- **Fix:** Purged `awscli` via APT and deployed the official standalone binary to `/usr/local/bin/aws`.