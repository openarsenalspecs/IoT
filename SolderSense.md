# SolderSense

**Precision Without Permission.**

SolderSense is an open-source, fully auditable programmable mouse designed for users who want complete control over their hardware — from physical inputs down to firmware execution.

Built for makers, developers, and security-conscious users, SolderSense removes cloud dependency, telemetry, and proprietary lock-in by design.

---

## 🔧 Features (Full Capability Set)

### 🖱️ Core Input System
- Fully open hardware design (KiCad schematics, PCB files, BOM, and assembly documentation)
- Driverless USB HID device (works on Linux, Windows, macOS)
- Low-latency input pipeline optimized for precision workflows
- Adjustable DPI stored directly on-device
- Physical macro disable / safety switch for secure environments

### ⚙️ Macro & Control Engine
- Deterministic macro execution engine (no host dependency for core logic)
- Deep macro scripting support:
  - Timers and delays
  - Key sequences
  - Conditional logic
  - Application-aware behavior
- Multi-profile system with instant switching
- Fully local profile storage (no cloud services)

### 🧠 Local AI Assistance (Non-Agentic)
- Offline AI assistant for:
  - Configuration validation
  - Macro optimization suggestions
  - Firmware audit assistance
- No external communication
- No telemetry or data collection
- No autonomous execution

### 🔐 Security & Privacy Model
- No telemetry
- No accounts
- No background data collection
- No vendor software dependency
- No network stack on-device (physically incapable of sending data)
- Signed firmware updates with explicit user approval
- Cryptographic verification (Ed25519)

### 🧪 Firmware & System Design
- Rust-based embedded firmware (memory-safe core)
- Reproducible builds (bit-for-bit verification support)
- Fully auditable execution from hardware to firmware
- Extensible firmware architecture for community contributions
- Hardware-executed macro engine (independent of host software)

### 💻 Desktop Tools
- Rust CLI tooling (mousectl-style interface)
- Optional lightweight GUI (non-Electron)
- Human-readable configuration formats (TOML/YAML)
- Reproducible build system using Nix/Docker

---

## 🧱 System Architecture

**Hardware Layer**
- ARM Cortex-M / RISC-V microcontroller
- Open optical sensor (public datasheet compatible)
- USB-C wired interface (security-first design)
- Onboard flash for profiles and macros
- KiCad-designed PCB

**Firmware Layer**
- Rust embedded runtime
- Deterministic macro interpreter
- USB HID communication layer
- Secure boot + signature verification

**Tooling Layer**
- CLI configuration manager
- Optional GUI for visualization and setup
- Local AI assistant integration (offline only)

---

## 🛡️ Security Principles

SolderSense is built under strict security constraints:

- No telemetry ever
- No hidden background processes
- No cloud dependencies
- No silent updates
- No external data transmission
- Fully reproducible and auditable builds

Every system behavior is inspectable from source to hardware execution.

---

## 🌍 Why SolderSense Exists

Modern input devices are increasingly closed ecosystems with hidden behavior, cloud dependencies, and opaque firmware.

SolderSense is a return to transparent hardware:

- If you can build it, you can verify it
- If you can read it, you can trust it
- If you can modify it, you truly own it

---

## 📦 Installation (Developer Preview)

> Hardware is currently in design/prototyping phase.

Firmware and tooling can be built using:

- Rust toolchain (embedded targets)
- Nix or Docker reproducible build environments
- Standard USB HID drivers (no proprietary software required)

---

## 🤝 Contributing

Contributions are welcome from developers, hardware engineers, and security researchers.

All contributions must comply with the project license and design principles of transparency, reproducibility, and privacy-first architecture.

---

## Specification Branding License (SBL)
### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/soldersense/](https://roxanneardary.com/soldersense/)  

---

## License & Notice Requirements

SolderSense is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- SolderSense specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
