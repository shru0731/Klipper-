# Wi-Fi Configuration

## Overview

This guide explains how to verify that your Raspberry Pi is connected to the Wi-Fi network and has internet access.

> **Important**
>
> - After powering on the Raspberry Pi, wait **2–5 minutes** for it to boot completely and connect to the Wi-Fi.
> - Make sure your **computer and Raspberry Pi are connected to the same Wi-Fi network**. Otherwise, SSH and the web interface (Mainsail/Fluidd) will not be accessible.
> - If you're using a **mobile hotspot**, open your hotspot settings and verify that the Raspberry Pi appears in the list of connected devices.

---

## Check Wi-Fi Status

Run the following command to verify that the wireless interface is connected:

```bash
iwconfig
```

If the Wi-Fi is connected, you should see details such as:

- Network Name (ESSID)
- Signal Strength
- Access Point

---

## Check the IP Address

To find your Raspberry Pi's IP address, run:

```bash
hostname -I
```

Example output:

```text
192.168.29.105
```

You will use this IP address to connect to the Raspberry Pi via SSH or to open Mainsail in a web browser.

---

## Test Internet Connectivity

Check whether the Raspberry Pi has internet access:

```bash
ping google.com
```

If everything is working correctly, you will receive replies similar to:

```text
64 bytes from google.com...
```

Press:

```text
Ctrl + C
```

to stop the test.

---

## Update the System

Before installing Klipper and other software, update the package list and upgrade installed packages:

```bash
sudo apt update
sudo apt upgrade -y
```

This may take several minutes depending on your internet speed.

---

## Verify Network Interfaces

To view detailed network information, run:

```bash
ip addr
```

Look for the `wlan0` interface. It should have an assigned IP address if the Wi-Fi connection is successful.

---

## Troubleshooting

### No IP Address

- Check that the Wi-Fi password is correct.
- Ensure the Raspberry Pi is within range of the Wi-Fi router.
- Restart the Raspberry Pi:

```bash
sudo reboot
```

### Unable to Ping Google

- Verify that your Wi-Fi network has internet access.
- Check if your router or hotspot is connected to the internet.

### Cannot Connect via SSH

- Ensure your computer and Raspberry Pi are on the **same network**.
- Verify the Raspberry Pi's IP address using:

```bash
hostname -I
```

---

## Next Step

Once your Raspberry Pi is connected to the internet, proceed to the next guide:

**04-KIAUH.md** – Installing KIAUH.