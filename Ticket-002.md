# Ticket Report: INC-002

## Issue
Configure initial local user account and privacy preferences during Out-Of-Box Experience (OOBE).

## User Impact
The user cannot access the desktop until initial account setup and device settings are completed.

## Environment
- **OS:** Windows 11 Home
- **Account Type:** Local Account

## Symptoms
- System is paused at the post-installation OOBE prompt awaiting user setup.

## Investigation
- Reviewed user provisioning options presented during the OOBE workflow.

## Root Cause
- Standard post-installation user setup step required before first desktop login.

## Resolution
- Created a local user account (`ITSupportLab`).
- Completed required setup prompts.
- Reviewed and configured default device privacy settings (location, diagnostics, telemetry options).

## Verification
- Confirmed successful login and loading of the initial Windows 11 Home desktop environment.

## Tools Used
- Windows Out-Of-Box Experience (OOBE) GUI

## Skills Demonstrated
- Local user provisioning
- Initial operating system setup

## Evidence
- `02-User-Account-Management/Ticket-002-01.png`
- `02-User-Account-Management/Ticket-002-02.png`
