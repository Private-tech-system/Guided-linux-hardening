
# 🛡️ Snort Lab Setup Guide (VPN + Local Testing)

This guide helps you configure and safely run Snort as an IDS (Intrusion Detection System) on your own machine — including support for VPN (tun0) and standard Wi-Fi (wlo1) interfaces. Includes ethical usage, test rules, and confirmation steps.

---

## ✅ Step 1: Confirm Interfaces Are Safe

Check your active interfaces:

```bash
ip a
```

Check your Wi-Fi interface is NOT in promiscuous mode:

```bash
ip link show wlo1
```

You should see:

```
state UP mode DEFAULT
```

---

## ✅ Step 2: Create or Edit Local Snort Rules

```bash
sudo nano /etc/snort/rules/local.rules
```

### 📌 Basic Content-Based Rule:

```snort
alert tcp any any -> any 80 (msg:"Test Rule - suspicious domain"; content:"malicious.test"; sid:1000001; rev:1;)
```

### 🧪 Optional Catch-All Rule (for testing):

```snort
alert ip any any -> any any (msg:"Test ANY traffic"; sid:1000002; rev:1;)
```

---

## ✅ Step 3: Confirm Your Rules Are Being Loaded

Make sure this line is uncommented in `/etc/snort/snort.conf`:

```snort
include $RULE_PATH/local.rules
```

---

## ✅ Step 4: Run Snort on Interface

### 🔌 For Wi-Fi (unencrypted, great for rule testing):

```bash
sudo snort -A console -q -i wlo1 -c /etc/snort/snort.conf
```

### 🔐 For VPN (secure tunnel monitoring):

```bash
sudo snort -A console -q -i tun0 -c /etc/snort/snort.conf
```

---

## ✅ Step 5: Trigger a Test Rule

If you're using the `malicious.test` rule:

```bash
curl -H "Host: malicious.test" http://example.com
```

If you're using the catch-all:

```bash
ping -c 1 1.1.1.1
```

You should see something like:

```
[1:1000002:1] Test ANY traffic
```

or

```
[1:1000001:1] Test Rule - suspicious domain
```

---

## ✅ Step 6: Confirm Snort Is Running

In another terminal:

```bash
ps aux | grep snort
```

Look for your Snort process showing the interface and config file.

---

## 🔁 When to Use Each Interface

| Interface | Best For |
|-----------|----------|
| `wlo1` | Learning, lab testing, unencrypted rule matching |
| `tun0` | Real-world VPN traffic, outbound IP/port analysis |

---

## ⚖️ Ethical Usage Checklist

✅ Monitor only your own device  
✅ Do not enable promiscuous or monitor mode  
✅ Do not sniff other people’s traffic (public Wi-Fi included)  
✅ Use Snort for learning, labs, and self-defense only  
✅ Respect all local laws and network policies  

---

## 🧠 Pro Tip

Once comfortable, try enabling official Snort community rules and write your own threat signatures based on your browsing, lab, or challenge activity.

