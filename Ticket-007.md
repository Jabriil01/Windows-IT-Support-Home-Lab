# Ticket Report: INC-007

## Issue
Troubleshoot complete loss of web connectivity on workstation.

## User Impact
User cannot access web pages or network resources (`ERR_INTERNET_DISCONNECTED`).

## Environment
- **OS:** Windows 11 Home
- **Network Interface:** Virtual Network Adapter
- **Tools:** Command Prompt (`cmd`), `ipconfig`, Network Connections (`ncpa.cpl`)

## Symptoms
- Web browser displays connectivity error page (`ERR_INTERNET_DISCONNECTED`).
- System tray indicates network interface disconnected or inactive.

## Investigation
- Opened Command Prompt and ran `ipconfig`.
- Observed that the local Ethernet adapter was not returning a valid address or interface was disabled.
- Opened Network Connections (`ncpa.cpl`) to inspect physical adapter state.

## Root Cause
- Network adapter was disabled in network connections control panel.

## Resolution
- Right-clicked network interface in `ncpa.cpl` and enabled adapter.
- Verified interface initialization and IP address acquisition via `ipconfig`.

## Verification
- Ran `ipconfig` in Command Prompt and confirmed a valid private IPv4 address was successfully assigned.
- Opened web browser and verified active internet connectivity.

## Tools Used
- Command Prompt (`ipconfig`)
- Network Connections (`ncpa.cpl`)
- Web Browser (Edge)

## Skills Demonstrated
- Layer 1/2 Network troubleshooting
- Network interface enabling and IP verification

## Evidence
- `07-Network-Troubleshooting/Ticket-007-01.png`

> **Note on Screenshot Security (Ticket 007):**
> To prevent public exposure of internal lab network details, the screenshot showing the restored `ipconfig` console output is retained in the private project documentation only and excluded from the public GitHub evidence folder.
