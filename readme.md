# Windows Wi-Fi Management using Netsh

This repository demonstrates how to manage Wi-Fi connections in Windows using `netsh` and WPA2-PSK XML profiles.

The lab includes:
- Wireless interface control
- Wi-Fi profile import using XML
- WPA2-PSK authentication
- Static and DHCP IP configuration
- Network troubleshooting commands

---

## Files

- [Wi-Fi Setup Guide](./wifi-setup.md)
- [Wi-Fi Profile XML](./BlueMatrix.xml)

---

## Important (Before Using XML Profile)

Before importing the XML file, the following values must be updated based on the Wi-Fi network:

### 1. Wi-Fi Name (SSID)
Change ALL occurrences of:

```text id="xml_change1"
BlueMatrix
```

to the Wi-Fi network name.

---

### 2. Wi-Fi Password (PSK)

Update this field:

```text id="xml_change2"
<keyMaterial>28:06:42:12</keyMaterial>
```

Replace with actual Wi-Fi password.

---

### 3. Profile Name

This must match SSID:

```text id="xml_change3"
<name>BlueMatrix</name>
```

Keep consistent across:
- Profile name
- SSID name
- netsh connect command

---

## Requirements

- Windows 10 / Windows 11
- Administrator Command Prompt
- Wireless adapter
- WPA2-PSK network access

