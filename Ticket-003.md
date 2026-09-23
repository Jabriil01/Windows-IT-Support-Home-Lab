# Ticket Report: INC-003

## Issue
Perform post-installation system verification and baseline hardware inspection.

## User Impact
Quality check to ensure system specs, computer name, drivers, and storage are correctly recognized before putting the workstation into service.

## Environment
- **OS:** Windows 11 Home
- **System Consoles:** System Settings, Device Manager, Disk Management

## Symptoms
- Routine audit following clean installation.

## Investigation
- Ran `winver` to inspect OS version and build information.
- Opened System Settings (`sysdm.cpl` / About page) to check machine name and installed RAM.
- Opened Device Manager (`devmgmt.msc`) to check for missing device drivers.
- Opened Disk Management (`diskmgmt.msc`) to review disk layout and drive letter assignments.

## Root Cause
- N/A (Routine system audit).

## Resolution
- Confirmed Windows 11 Home edition and system memory in System Info.
- Identified unrecognized system devices in Device Manager marked for driver troubleshooting.
- Verified disk partitioning layout in Disk Management.

## Verification
- All diagnostic consoles (`winver`, System Settings, Device Manager, Disk Management) opened and documented without errors.

## Tools Used
- System Information (`winver`)
- System Settings (`sysdm.cpl`)
- Device Manager (`devmgmt.msc`)
- Disk Management (`diskmgmt.msc`)

## Skills Demonstrated
- Post-installation system auditing
- OS version and hardware verification

## Evidence
- `03-System-Verification/Ticket-003-01.png`
- `03-System-Verification/Ticket-003-02.png`
