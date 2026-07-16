# Install Klipper

## Launch KIAUH

```bash
git clone git clone https://github.com/dw-0/kiauh.git

cd ~/kiauh
./kiauh.sh
```

---

## Installation

Choose

```
Install
```

Select

```
Klipper
```

KIAUH installs Klipper automatically.

---

## Verify Installation

```bash
systemctl status klipper
```

You should see

```text
Active: active (running)
```

---

## Restart Klipper

```bash
sudo systemctl restart klipper
```

Klipper installation is complete.