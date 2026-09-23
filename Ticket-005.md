# Ticket Report: INC-005

## Issue
Perform system updates and verify security definition status in Microsoft Defender.

## User Impact
System may be missing important stability patches and security definition updates.

## Environment
- **OS:** Windows 11 Home
- **Services:** Windows Update, Microsoft Defender Security Center

## Symptoms
- Windows Update had not been run since initial system deployment.

## Investigation
- Opened Windows Update settings and initiated a check for updates.
- Checked Microsoft Defender Security Center for current protection status and definition versions.

## Root Cause
- New system installation required initial update baseline download and security definition updates.

## Resolution
- Triggered manual download and installation of pending Windows updates.
- Applied security intelligence updates for Microsoft Defender.

## Verification
- Confirmed Windows Update displayed "You're up to date" status.
- Confirmed Defender definitions were current.

## Tools Used
- Windows Update GUI
- Microsoft Defender Security Center

## Skills Demonstrated
- Patch management
- Endpoint security maintenance

## Evidence
- `05-Windows-Update-Maintenance/Ticket-005-01.png`
