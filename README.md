# 🛡️ ShieldGuard

**ShieldGuard** is a real-time Windows security monitoring system that combines a modern web dashboard with a local security agent to provide visibility into system activity, network connections, threats, and security risks.

The project is designed to make local security monitoring easier to understand through a centralized and intuitive dashboard.

## 🚀 Features

* 🔍 **Process Monitoring** – Monitor running processes on the Windows system.
* 🌐 **Network Monitoring** – Inspect active network connections.
* ⚠️ **Threat Detection** – Identify and display potential security threats.
* 📊 **Security Score** – Present an overall view of the system's security status.
* 📡 **Real-Time Events** – Display security-related events from the local machine.
* 🖥️ **Web Dashboard** – Modern interface for viewing system security information.
* 🤖 **Local Security Agent** – Python-based agent running directly on the Windows machine.
* 📦 **Standalone Agent** – Can be packaged as a Windows executable using PyInstaller.

## 🏗️ Architecture

```text
                    ┌─────────────────────┐
                    │   ShieldGuard Web   │
                    │   Next.js Dashboard │
                    └──────────┬──────────┘
                               │
                               │ HTTP API
                               ▼
                    ┌─────────────────────┐
                    │ ShieldGuard Agent   │
                    │   Python / Windows  │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             ▼                 ▼                 ▼
        Processes        Network Connections   Events
             │                 │                 │
             └─────────────────┼─────────────────┘
                               ▼
                    ┌─────────────────────┐
                    │ Threat & Risk Data  │
                    └─────────────────────┘
```

## 🛠️ Technology Stack

### Web Dashboard

* Next.js
* React
* JavaScript / TypeScript
* Vercel

### Local Agent

* Python
* Flask
* psutil
* Windows APIs / system information
* PyInstaller

## 📁 Project Structure

```text
ShieldGuard/
│
├── web/
│   └── Next.js Dashboard
│
└── agent/
    └── ShieldGuard Python Agent
```

## 🔌 Local Agent API

The local ShieldGuard agent runs on:

```text
http://127.0.0.1:8765
```

Available API endpoints include:

```text
/api/status
/api/connections
/api/events
/api/threats
```

These endpoints provide the dashboard with information collected from the local Windows system.

## 🌐 Dashboard

The ShieldGuard web dashboard is built with Next.js and can be deployed using Vercel.

**Live Dashboard:**

https://shieldguard-ten.vercel.app

## 🎯 Project Goal

ShieldGuard aims to provide a simple and accessible way to monitor the security state of a Windows computer by combining **local system-level monitoring** with a **modern web-based interface**.

Instead of requiring users to interpret raw system information, ShieldGuard presents processes, network activity, threats, events, and risk information through a unified dashboard.

## 🔐 Privacy & Architecture

ShieldGuard is designed around a **local-agent architecture**. System-level information is collected by the agent running on the user's Windows machine rather than by the public web dashboard directly.

The web interface communicates with the locally running agent through its API.

## 🚧 Future Improvements

* Advanced threat detection
* More detailed process risk analysis
* Network anomaly detection
* Security alerts and notifications
* Historical security analytics
* Automatic threat response
* Improved authentication and access control
* Cross-platform agent support

## 📜 Project Status

**Development / Prototype**

ShieldGuard is an evolving cybersecurity monitoring project focused on combining local Windows monitoring with a modern web-based security dashboard.

---

### 🛡️ ShieldGuard

**Monitor. Detect. Understand. Protect.**
