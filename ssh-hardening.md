SSH Hardening (Linux Mint)

This section documents the full process of hardening the SSH service on a personal Linux Mint system. All changes were performed manually, with each step guided by ChatGPT for learning and clarity.

      Goal: Lock down SSH to prevent unauthorized remote access.

      Risk if ignored: Weak SSH settings can allow brute-force login attempts, unauthorized access, or remote exploits — especially if your system is exposed to the internet.

 Step-by-Step Walkthrough


1. Changed the default SSH port

The default SSH port (22) is commonly scanned by attackers. Changing it helps reduce random brute-force attempts.

sudo nano /etc/ssh/sshd_config

Changed this line:

#port22

To something like:

#Port 58223

Then restarted SSH:

sudo systemctl restart ssh

  Why: Obscuring the port is not foolproof but helps reduce noise from automated attacks.


2. Disabled root login over SSH

Allowing root login is risky — if credentials are compromised, attackers get full control. Disabling it forces use of non-root accounts with sudo.

sudo nano /etc/ssh/sshd_config

Find this line:

PermitRootLogin yes

And change it to:

PermitRootLogin no

Then restart SSH:

sudo systemctl restart ssh

  Why: Reduces the attack surface and enforces the principle of least privilege.

  Step 3: Enforce Key-Based Authentication

Why:
Password logins are vulnerable to brute-force attacks. Using SSH keys is far more secure — they're nearly impossible to guess or crack.

What We Did:

  1.  Opened the SSH configuration file:

sudo xed /etc/ssh/sshd_config

  2. Found and modified (or added) the following line:

PasswordAuthentication no

  3. Saved the file.

  4. Restarted the SSH service to apply changes:

    sudo systemctl restart ssh

  5. How to Confirm It Worked:

    Run:

sudo sshd -T | grep passwordauthentication

  6. You should see:

    passwordauthentication no

This confirms SSH password logins are disabled, and only key-based authentication is allowed.

  
  Step 4: Restart SSH and Confirm It’s Working

Why:
Changes to the SSH configuration don’t take effect until the SSH service is restarted. This final step ensures all hardening measures are live and functioning properly.

 What We Did:

   1. Restarted the SSH service:

sudo systemctl restart ssh

   2.  Verified that the service is active and running:

sudo systemctl status ssh

   3.  You should see:

    Active: active (running)

    (Optional but recommended): Used a second terminal or device to test SSH login using your key — this ensures you won’t get locked out.

   Final Result for SSH Hardening

You now have a hardened SSH setup that includes:

    ✅ Custom port to reduce noise from automated scans

    ✅ Root login disabled

    ✅ Password authentication disabled

    ✅ Key-based login enforced

    ✅ SSH confirmed running and secure






