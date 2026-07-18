# 🚀 VPS Infrastructure as Code

A complete, battle-tested Ansible collection to deploy a modern, secure, and lightweight self-hosted infrastructure.

## 🔥 Key Highlights

### ⚡ Ultra-Light Matrix & VoIP Stack (Tuwunel)
Forget heavy Synapse. We run a highly optimized communication stack:
- **Conduit (Tuwunel):** The Rust-based Matrix homeserver. Blazing fast, super low memory footprint.
- **LiveKit:** High-performance WebRTC SFU for crystal clear audio/video calls.
- **Element Call Integration:** Full support for **Element X** native calls via a dedicated JWT-provider service.
> **Result:** A private Discord/Telegram alternative with video calls that runs on a $5 VPS.

### 🔐 Zero-Touch Identity (SSO)
A fully automated authentication chain protecting your services:
- **LLDAP:** Lightweight backend for users.
- **PocketID:** Beautiful OIDC Provider (Passkeys support).
- **TinyAuth:** Middleware that protects any web service with a login screen.
> **Magic:** The playbook automatically wires everything. It bootstraps LLDAP, logs into PocketID (via API), generates secrets, and configures TinyAuth without you touching the UI.

### 🌐 Secure Base Servers & Networking
A fully automated foundation for secondary services and proxies:
- **Netbird Mesh VPN:** Automated deployment of the Netbird Management stack and zero-touch client joining (via setup keys) to securely bridge all nodes.
- **Dynamic SNIProxy:** Automatically binds to the Netbird interface to securely proxy traffic internally across the mesh network.
- **Smart DNS Management:** Fully automated ArvanCloud DNS record lifecycle. The playbook idempotently creates and updates A records (root, panel, and sub domains) only when IP drift is detected.
- **3x-ui, TeamSpeak & Aether:** Containerized proxy panels, self-hosted game communications, and forums configured out-of-the-box.
> **Magic:** You just define a host and run the playbook. DNS records sync, the VPN mesh connects, and internal services bind themselves to the encrypted tunnel automatically.
