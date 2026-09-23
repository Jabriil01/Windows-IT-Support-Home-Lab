# Ticket Report: INC-010

## Issue
Inspect Event Viewer logs to evaluate system warning logs (Event ID 10016).

## User Impact
Routine diagnostic check; user experienced no immediate crash, but system log review requested for stability audit.

## Environment
- **OS:** Windows 11 Home
- **Console:** Event Viewer (`eventvwr.msc`)

## Symptoms
- Warning logs generated in System log during OS boot sequence.

## Investigation
- Opened Event Viewer (`eventvwr.msc`).
- Navigated to `Windows Logs > System`.
- Applied log filter for **Warning** level events.
- Selected Event ID 10016 (DistributedCOM) and read detailed log event description.

## Root Cause & Interpretation
- Event ID 10016 (DistributedCOM) was identified in the System log.
- No user-facing fault was reproduced during the lab, so the event was documented rather than modified.

## Resolution
- Evaluated event details against standard troubleshooting guidelines.
- Determined event was non-critical and documented baseline findings without making unnecessary registry or DCOM permission modifications.

## Verification
- Verified log details logged correctly and confirmed machine operates normally without functional issues.

## Tools Used
- Event Viewer (`eventvwr.msc`)
- Log Filtering Utilities

## Skills Demonstrated
- Log analysis
- System event filtering and prudent diagnostic evaluation

## Evidence
- `10-Event-Viewer-Log-Analysis/Ticket-010-01.png`
