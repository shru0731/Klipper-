# SSH Setup

## What is SSH?

SSH (Secure Shell) is a network protocol that allows you to securely access and control your Raspberry Pi remotely from another computer using a terminal.

---

## Prerequisites

Before connecting, ensure that:

- SSH is enabled on the Raspberry Pi.
- Your Raspberry Pi and computer are connected to the same network.
- You know either the Raspberry Pi's **hostname** or **IP address**.
- You know the **hostname** and **username** of your Raspberry Pi.
- You know the **password** of your Raspberry Pi.

---

## Method 1: Connect Using the Hostname

Open a terminal and enter:

```bash
ssh username@hostname
```

### Example

```bash
ssh pi@pi
```

> Replace `pi` with your own username and hostname.

---

## Method 2: Connect Using the Hostname (.local)

If your network supports mDNS (enabled by default on Raspberry Pi OS), you can connect using:

```bash
ssh username@hostname.local
```

### Example

```bash
ssh pi@pi.local
```

> Replace `pi` with your own username and hostname.

---

## Method 3: Connect Using the IP Address

First, find your Raspberry Pi's IP address.

Example:

```text
192.168.0.120
```

Open a terminal and run:

```bash
ssh username@IP_ADDRESS
```

### Example

```bash
ssh pi@192.168.0.120
```

---

## First-Time Connection

The first time you connect, you'll see a message similar to:

```text
The authenticity of host '192.168.0.120' can't be established.
ED25519 key fingerprint is SHA256:xxxxxxxxxxxxxxxxxxxxxxxx.
Are you sure you want to continue connecting (yes/no/[fingerprint])?
```

Type:

```text
yes
```

Press **Enter**.

---

## Enter Your Password

When prompted, enter your Raspberry Pi password.

```text
pi@192.168.0.120's password:
```

> **Note:** The password will not be visible while typing. This is normal behavior in Linux terminals.

---

## Successful Connection

If the connection is successful, you'll see a prompt similar to:

```text
carb@carb:~ $
```

You are now connected to your Raspberry Pi via SSH and can execute commands remotely.

---

## Troubleshooting

### Connection Refused

SSH may not be enabled.

Enable SSH using Raspberry Pi Imager before flashing the SD card, or connect a keyboard and monitor to enable it manually.

---

### Host Not Found

If `hostname.local` doesn't work, try:

- `ssh username@hostname`
- `ssh username@IP_ADDRESS`

---

### Permission Denied

Verify that:

- The username is correct.
- The password is correct.
- Caps Lock is off.

---

## Useful Commands

### Display the Hostname

```bash
hostname
```

### Display the IP Address

```bash
hostname -I
```

### Display the Current User

```bash
whoami
```