# TimeFabric

**Scheduling, simplified.**

---

## 🌐 Overview

TimeFabric is a fully open-source, self-hostable scheduling platform designed to give businesses complete control over how they manage time, services, and appointments. It is built to be modular, extensible, and privacy-respecting, with deep support for automation, voice control, weather intelligence, and printable calendar generation.

Unlike traditional scheduling tools, TimeFabric is designed as a **complete time orchestration system**, not just a booking interface.

It is released under the **AGPL 3.0+ license**, ensuring that all improvements and network-deployed versions remain open and attributable.

---

## ⚙️ Core Features

### 📅 Scheduling System
- Dynamic time slot generation per service
- Adjustable service durations and buffers
- Staff and resource assignment per booking
- Conflict detection and prevention (no double-booking)
- Public and private service visibility controls
- Recurring appointment support
- Multi-location scheduling support

---

### 🌐 Website Integration
- Embeddable booking widgets
- Full public booking pages
- API-first architecture for integrations
- Webhook support for external systems
- CRM and POS compatibility layer (plugin-based)

---

### 🔐 Authentication & Access Control
- Role-based access (admin, staff, client)
- OAuth2 / OpenID Connect support
- Secure session handling
- Optional multi-factor authentication
- Device-level trust management

---

### 🎙️ Universal Voice Scheduling
- Wake-word activation (“Hey TimeFabric”)
- Natural language scheduling commands
- Full system voice control (not just bookings)
- Voice-driven service management and edits
- Offline/online hybrid voice processing support
- Mobility mode for hands-free use while driving

---

### 🌦️ Weather Intelligence Module
- Event-linked weather forecasting
- Location-specific weather tracking per appointment
- Weather risk scoring (low to critical)
- Automated conflict detection for outdoor events
- Real-time weather change monitoring
- Smart rescheduling suggestions based on conditions
- Weather-triggered notifications (email, SMS, push)

---

### 🔔 Notifications System
- Email confirmations and reminders
- SMS notifications (optional)
- Push notifications (web/mobile)
- Event-based alerts via webhook system
- Weather-related disruption alerts
- Schedule change notifications

---

### 🔌 Integrations Module
- Google Calendar / iCal synchronization
- External CRM integration support
- POS system connections
- Payment gateway support (optional)
- Plugin-based extension system
- Event-driven webhook architecture

---

### 🧠 AI & Smart Scheduling Layer (Optional)
- Natural language understanding for text and voice
- Smart scheduling suggestions
- Conflict prediction and avoidance
- Optimization of booking density
- Optional local LLM support (Ollama / llama.cpp)

---

### 🖨️ Print & Calendar Export Module
- Personalized yearly calendar generation
- Monthly and custom-range calendar exports
- Image import for branding and customization
- Automated inclusion of:
  - Appointments
  - Birthdays
  - Anniversaries
  - Holidays
- Highlighting of recurring annual events
- Export formats:
  - PDF (print-ready)
  - PNG / JPEG
  - Multi-page calendar books
- Digital sharing and downloadable calendar packages
- Website-embeddable calendar previews

---

### 🌍 Cross-Device Sync System
- Real-time synchronization across all devices
- WebSocket-based live updates
- Offline-first queue synchronization
- Multi-device continuity (mobile, desktop, voice, embedded)
- Conflict resolution engine
- Secure device pairing and identity management
- Event-driven architecture for system-wide updates

---

## 🧩 Architecture Philosophy

TimeFabric is designed as a:

> **Modular scheduling and time orchestration system**

It can operate as:
- A single self-hosted application (MVP)
- A modular monolith
- A distributed system (advanced deployments)

All modules communicate through a shared event-driven architecture.

---

## 🔁 System Event Model

Everything in TimeFabric is event-based:

- `appointment.created`
- `appointment.updated`
- `weather.risk_detected`
- `voice.command_executed`
- `calendar.exported`
- `notification.sent`

This ensures real-time synchronization across all modules.

---

## 🧱 Tech Stack (Recommended)

- **Frontend:** SvelteKit (or Next.js)
- **Backend:** FastAPI (Python)
- **Database:** PostgreSQL
- **Cache:** Redis (optional)
- **Auth:** Keycloak or Supabase Auth
- **Voice:** Whisper + intent parser (spaCy / LLM optional)
- **Realtime:** WebSockets / SSE
- **Deployment:** Docker + GitLab CI/CD

---

## 🚀 Deployment

TimeFabric is designed for self-hosting:

- Docker Compose (MVP setup)
- GitLab CI pipelines for automated builds
- Optional Kubernetes support for scaling

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
  - [https://roxanneardary.com/timefabric/](https://roxanneardary.com/timefabric/)

---

## 📜 License & Notice Requirements

TimeFabric is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- TimeFabric specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's `notice.md` file tracks attribution requirements and contributor acknowledgments. Any updates that add contributors or modify attribution must update `notice.md`.
- Pull requests must maintain attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, see the AGPL-3.0+ license and `notice.md`.

---

## 🧭 Philosophy

TimeFabric is built on a simple principle:

> Time should be structured by you—not controlled by platforms.

---

## 🌟 Project Goal

To create a fully open, voice-enabled, weather-aware, cross-device scheduling system that replaces fragmented SaaS scheduling tools with a single unified open-source platform.  
