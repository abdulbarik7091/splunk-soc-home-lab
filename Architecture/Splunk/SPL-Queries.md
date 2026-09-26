# Splunk SPL Queries

## 1. Find Failed Logins

Query:

index=* EventCode=4625

This finds failed Windows login attempts.

## 2. Find Failed Logins by User

Query:

index=* EventCode=4625 | stats count by Account_Name

This shows which user accounts had failed logins.

## 3. Find Failed Logins by IP

Query:

index=* EventCode=4625 | stats count by IpAddress

This shows which IP addresses caused failed logins.

## 4. See Failed Logins Over Time

Query:

index=* EventCode=4625 | timechart count

This shows failed logins over time.
