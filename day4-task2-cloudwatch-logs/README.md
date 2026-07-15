# Day 4 - Task 2: Monitoring CloudWatch Logs

## Objective

Set up CloudWatch alarms, a custom metric dashboard, and CPU
threshold-based logs.

## Setup

- Instance: devops-intern-monitoring (t3.micro), detailed monitoring enabled
- SSH restricted to operator's IP only

## Alarm

devops-intern-high-cpu - triggers when average CPU > 70% over 2  
consecutive 5-minute periods.

## Dashboard

devops-intern-dashboard - CPU utilization widget.

## Verification

Generated artificial CPU load (`yes > /dev/null &`) to confirm the
alarm correctly transitions to ALARM state.

## Screenshots

See `/screenshots` folder.

## Key Takeaway

Detailed monitoring plus a realistic evaluation window (2 consecutive
periods, not a single spike) balances catching real sustained load
against false-positive alerts.