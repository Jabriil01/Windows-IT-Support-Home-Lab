# Ticket Report: INC-008

## Issue
Troubleshoot DNS resolution failure while network link is active.

## User Impact
User cannot open websites using domain names.

## Environment
- **OS:** Windows 11 Home
- **Network Utility:** `nslookup`, IPv4 Adapter Properties

## Symptoms
- Executing domain lookup (`nslookup microsoft.com`) in Command Prompt fails with request timed out / server unreachable error.

## Investigation
- Checked network adapter status; physical link active.
- Ran `nslookup` command to test name resolution against configured DNS server.
- Opened IPv4 properties in Network Adapter settings and inspected DNS entries.

## Root Cause
- Static DNS server was manually set to an invalid/unreachable IP address, breaking domain resolution queries.

## Resolution
- Opened IPv4 Adapter Properties (`ncpa.cpl`).
- Restored the DNS configuration to a valid working configuration.

## Verification
- Re-ran `nslookup microsoft.com` in Command Prompt.
- Verified immediate and successful IP address response from the resolved server.

## Tools Used
- Command Prompt (`nslookup`)
- IPv4 Network Properties GUI

## Skills Demonstrated
- DNS troubleshooting
- TCP/IP adapter configuration

## Evidence
- `08-DNS-Troubleshooting/Ticket-008-01.png`
- `08-DNS-Troubleshooting/Ticket-008-02.png`
