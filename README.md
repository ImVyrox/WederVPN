# WederVPN

**The ultimate, lightweight, and 100% free solution against VPNs, Proxies, and Alt-Accounts**

[![SpigotMC Resource](https://img.shields.io/badge/SpigotMC-138645-orange?style=flat&logo=spigotmc)](https://www.spigotmc.org/resources/wedervpn-nexu-studios.138645/)

WederVPN is a modern and ultra-optimized security plugin built for Minecraft servers (Paper, Folia, and Velocity). Designed from the ground up to protect your community against malicious users, bot attacks, alt accounts, and VPN or Proxy connections. WederVPN is 100% free: no licenses, no mandatory API keys, and no hidden limitations.

**Official Resource Page:** [SpigotMC - WederVPN](https://www.spigotmc.org/resources/wedervpn-nexu-studios.138645/)

---

## Key Features

* **Zero-Impact Asynchronous Performance:** All network checks and inspections run fully asynchronously and in parallel, guaranteeing untouched TPS even during mass player logins.
* **Full IPv4 and IPv6 Support:** Native next-generation IP address support across all commands and modules.
* **IP Limiter Module (Multi-Account Control):** Limits simultaneous connections from the same IP address and features a time-based reset system (e.g., `30m`) to prevent unfair blocks on shared networks.
* **Multi-API System with Fallback:** Native integration with over 20 free VPN/Proxy detection providers (IP-API, FreeIPAPI, ProxyCheck, IPQualityScore, IPHub, and more) with automatic failover.
* **GeoLocation & Country Gatekeeper:** Whitelist or blacklist specific countries using standard ISO codes (e.g., `US`, `ES`, `MX`).
* **ISP Filter & Bogon IP Blocker:** Blocks connections coming from high-risk ISPs or non-routable private IP ranges.
* **Detailed Real-Time In-Game Alerts:** Staff notifications on player join displaying detailed connection info (Username, Client Brand, Version, IP, Country, City, and linked alt accounts).
* **Passive Mode:** Scans connections in the background without kicking players; ideal for auditing or pairing with external security systems.
* **Database Support:** Save logs, cache, and alert preferences using MySQL, MongoDB, or SQLite.

---

## Commands & Permissions

| Command | Description | Permission |
| :--- | :--- | :--- |
| `/wvpn` | Displays the main help menu and plugin status | `wvpn.command` |
| `/wvpn lookup <player\|ip>` | Performs a real-time deep security analysis on an IP or player | `wvpn.command.lookup` |
| `/wvpn alerts` | Toggles in-game security notifications on or off | `wvpn.command.alerts` |
| `/wvpn allowlist <add\|remove\|info\|purge>` | Manages the allowlist for IP addresses/players to bypass checks | `antivpn.command.allowlist` |
| `/wvpn clearcache` | Clears the local cached API responses | `wvpn.command.clearcache` |
| `/wvpn reload` | Reloads all configuration files and modules | `wvpn.command.reload` |

---

## Modular Directory Structure

Upon initial startup, an organized directory structure is automatically generated for easy customization:

* `/plugins/WederVPN/cache/` ➜ Local temporary response cache.
* `/plugins/WederVPN/modules/` ➜ Settings for IP Limiter, ISP Filter, Bogon, etc.
* `/plugins/WederVPN/services/` ➜ Independent API service configurations.
* `/plugins/WederVPN/languages/` ➜ Customizable i18n translation files.

---

## Installation

1. Download `WederVPN.jar` from [SpigotMC](https://www.spigotmc.org/resources/wedervpn-nexu-studios.138645/).
2. Place the `.jar` file into your server's `/plugins` directory.
3. Restart your server or proxy.
4. Configure your desired modules in `/plugins/WederVPN/`.

---

## Requirements

* **Server Software:** Paper, Folia, or Velocity Proxy
* **Java Version:** Java 21+
