# Ticket Report: INC-009

## Issue
Identify and resolve missing hardware driver on unrecognized system device (Code 28).

## User Impact
Unrecognized virtual device causes warning icon in Device Manager and hardware features are unavailable.

## Environment
- **OS:** Windows 11 Home Workstation
- **Hypervisor:** VirtualBox
- **Console:** Device Manager (`devmgmt.msc`)

## Symptoms
- Device Manager displays "Base System Device" under "Other devices" marked with a yellow exclamation icon.
- Device status shows Error Code 28 (The drivers for this device are not installed).

## Investigation
- Opened Device Manager (`devmgmt.msc`).
- Opened properties for "Base System Device" and selected **Details > Hardware IDs**.
- Identified Hardware Vendor and Device string (`PCI\VEN_80EE&DEV_CAFE`) corresponding to VirtualBox Guest Integration hardware.

## Root Cause
- Missing vendor driver software required to recognize guest integration hardware.

## Resolution
- Mounted VirtualBox Guest Additions ISO media to virtual optical drive.
- Executed Guest Additions setup installer to install required driver files.

## Verification
- Re-inspected Device Manager.
- Confirmed yellow warning flag was resolved and hardware listed as operating normally.

## Tools Used
- Device Manager (`devmgmt.msc`)
- Hardware IDs Inspection (`VEN`/`DEV`)
- VirtualBox Guest Additions Installer

## Skills Demonstrated
- Hardware diagnostics
- Hardware ID extraction and driver remediation

## Evidence
- `09-Driver-Troubleshooting/Ticket-009-01.png`
- `09-Driver-Troubleshooting/Ticket-009-02.png`
