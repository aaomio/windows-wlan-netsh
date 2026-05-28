# Windows Wi-Fi Setup using Netsh

This guide explains how to connect to a WPA2-PSK wireless network using `netsh`.

---

## 1. Show Network Interfaces

```cmd
netsh int show int
```

Displays available network adapters.

---

## 2. Enable Wi-Fi Adapter

```cmd
netsh int set int Wi-Fi enable
```

---

## 3. View Available Networks

```cmd
netsh wlan show network
```

---

## 4. View Saved Profiles

```cmd
netsh wlan show profile
```

---

## 5. Delete Existing Profile (if needed)

```cmd
netsh wlan delete profile name="BlueMatrix"
```

---

## 6. Add Wi-Fi Profile

```cmd
netsh wlan add profile filename="C:\WiFiProfiles\BlueMatrix.xml"
```

---

## 7. Connect to Wi-Fi

```cmd
netsh wlan connect name="BlueMatrix"
```

---

## 8. Show Profile Details

```cmd
netsh wlan show profile name="BlueMatrix" key=clear
```

---

## 9. Set DHCP

```cmd
netsh interface ipv4 set address name="Wi-Fi" source=dhcp
netsh interface ipv4 set dns name="Wi-Fi" source=dhcp
```

