# Ticket Report: INC-004

## Issue
Partition unallocated drive space into a new secondary volume (`D:`) and extend the primary system partition (`C:`).

## User Impact
Unused storage space on the hard drive was invisible and unusable in File Explorer.

## Environment
- **OS:** Windows 11 Home
- **Console:** Disk Management (`diskmgmt.msc`)

## Symptoms
- User has unallocated disk space that is not accessible as a usable drive volume.
- Attempting to extend drive `C:` was initially unavailable because non-contiguous space or unpartitioned layout blocked immediate expansion.

## Investigation
- Opened Disk Management (`diskmgmt.msc`) and inspected the physical disk partition map.
- Identified unallocated disk segments.

## Root Cause
- The disk contained unallocated space that had not yet been formatted into an NTFS partition.

## Resolution
- Used the **New Simple Volume Wizard** in Disk Management to create and format a secondary NTFS partition assigned drive letter `D:`.
- Reconfigured unallocated space adjacent to `C:` and selected **Extend Volume** on drive `C:`.

## Verification
- Opened File Explorer to confirm drive `D:` was mounted and accessible.
- Confirmed in Disk Management that drive `C:` reflected increased total capacity.

## Tools Used
- Disk Management (`diskmgmt.msc`)
- File Explorer

## Skills Demonstrated
- Storage administration
- NTFS volume creation and disk extension

## Evidence
- `04-Storage-Partition-Management/Ticket-004-01.png`
- `04-Storage-Partition-Management/Ticket-004-02.png`
- `04-Storage-Partition-Management/Ticket-004-03.png`
