# Ticket Report: INC-001

## Issue
Perform a clean installation and initial disk setup of Windows 11 Home on a virtual workstation.

## User Impact
A new computer setup is required. The system is unusable until the operating system is fully installed.

## Environment
- **Platform:** Oracle VM VirtualBox
- **Target OS:** Windows 11 Home
- **Storage:** `VBOX HARDDISK` (Unallocated Virtual Disk Space)

## Symptoms
- The virtual machine boots into an unconfigured state without an operating system loaded.

## Investigation
- Booted the virtual machine using the Windows 11 Home installation ISO.
- Navigated to the regional configuration settings (Language, Time/Currency format, Keyboard layout).
- Advanced to the activation step and selected the option to skip product key entry for testing purposes.
- Reviewed available drive targets in the Windows Setup disk selection screen.

## Root Cause
- Fresh installation scenario; no operating system was previously installed on the assigned virtual hard disk.

## Resolution
- Selected language and keyboard preferences.
- Bypassed product key entry to proceed with standard setup.
- Selected unallocated space on Drive 0 (`VBOX HARDDISK`) and allowed Windows Setup to create required default partitions and copy installation files.

## Verification
- Confirmed that the installer successfully expanded files and progressed past the primary installation phase.

## Tools Used
- Windows Setup Wizard
- VirtualBox Manager

## Skills Demonstrated
- Operating system installation
- Storage partition selection during setup

## Evidence
- `01-Windows-Installation-Setup/Ticket-001-01.png`
- `01-Windows-Installation-Setup/Ticket-001-02.png`
