# Install Moonraker

## Launch KIAUH

```bash
git clone git clone https://github.com/dw-0/kiauh.git
cd ~/kiauh
./kiauh.sh
```

---

## Install

Choose

```
Install
```

Select

```
Moonraker
```

---

## Verify

```bash
systemctl status moonraker
```

Expected output

```text
Active: active (running)
```

---

## Restart

```bash
sudo systemctl restart moonraker
```

Moonraker is now running.