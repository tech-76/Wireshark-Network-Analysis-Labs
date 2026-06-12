# Wireshark Installation Guide

## Objective

Install Wireshark safely and confirm that packet capture is working.

## Windows

1. Download Wireshark from the official Wireshark website.
2. Run the installer.
3. Keep the default components unless a lab requires otherwise.
4. Install Npcap when prompted.
5. Complete the installation.
6. Launch Wireshark.
7. Select the active Ethernet or Wi-Fi interface.
8. Start a short capture.
9. Generate traffic by running `ping 8.8.8.8` or opening a test website.
10. Stop the capture and confirm packets were recorded.

## Linux

Installation commands vary by distribution.

### Debian or Ubuntu

```bash
sudo apt update
sudo apt install wireshark
```

During installation, choose whether non-root users may capture packets based on the security requirements of the system.

### Fedora

```bash
sudo dnf install wireshark
```

## macOS

Install Wireshark using the official installer or a trusted package manager. Confirm that required capture permissions are granted.

## Verification Checklist

- [ ] Wireshark opens without errors
- [ ] The active network interface is visible
- [ ] Packets appear during a test capture
- [ ] Display filters can be applied
- [ ] Captures can be saved locally
- [ ] Sensitive captures are not uploaded publicly

## Troubleshooting

### No interfaces are visible

- Confirm packet-capture components were installed
- Restart Wireshark
- Restart the computer if required
- Check operating-system permissions

### Packets are not appearing

- Confirm the correct interface is selected
- Generate network traffic
- Disable capture filters temporarily
- Check whether a VPN or virtual adapter is carrying the traffic
