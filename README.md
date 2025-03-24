# Infrastructure Security

**Purpose:** Provide examples and tools for securing both cloud and on-premises infrastructure. This repository is for IT security professionals and system administrators seeking to harden servers, network configurations, and other infrastructure components against threats.

**Technologies & Tools:** Bash scripting, Linux/Windows configuration, firewall and network policy, Ansible (for automation, optional).

**Use Cases:**
- Harden default server configurations (e.g., disable insecure defaults in SSH or RDP).
- Automate the application of security baseline settings across multiple servers.
- Provide configuration snippets for network security (firewall rules, segmentation) and system security (OS-level settings).

## Examples

- **Linux SSH Hardening:** The script [`harden-ssh.sh`](scripts/harden-ssh.sh) in `scripts/` automates disabling root login and password auth in an SSH config, as shown in [`secure-ssh.conf`](configs/secure-ssh.conf).
- **Configuration Snippets:** The `configs/` directory contains example settings like a hardened SSH configuration and could be extended to other services (web server configs, etc.).

## Usage

Review and run the provided script on a test system:
```bash
# Example: Harden SSH on current machine (ensure you have sudo privileges)
bash scripts/harden-ssh.sh
```
After running, you can open `secure-ssh.conf` or `/etc/ssh/sshd_config` to verify that the intended settings (no root login, no password auth) are in place. Always test changes in a safe environment before rolling out to production.
