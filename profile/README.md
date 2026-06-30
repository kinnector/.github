# Kinnector

An open-source, telemetry-driven security platform for real-time monitoring and runtime protection.

Kinnector decouples low-level telemetry gathering from active policy enforcement and user interfaces. This creates a lightweight security layer that doesn't impact application performance.

## Repositories

### Desktop Users
*   **[kinnector-core](https://github.com/kinnector/kinnector-core)** – Low-level telemetry engine that captures system events.
*   **[kinnector-agent](https://github.com/kinnector/kinnector-agent)** – Local daemon that receives telemetry from the core and forwards it to wardens or backends.
*   **[kinnector-desktop](https://github.com/kinnector/kinnector-desktop)** – Cross-platform desktop dashboard for visual administration.
*   **[kinnector-cli](https://github.com/kinnector/kinnector-cli)** – Terminal-based dashboard for checking logs and configuration.

### Backend & Servers
*   **[kinnector-warden](https://github.com/kinnector/kinnector-warden)** – Active runtime protector that blocks malicious activities and enforces security rules.
*   **[kinnector-protect](https://github.com/kinnector/kinnector-protect)** – Security rules and policies used by the warden.
*   **[kinnector-wordpress](https://github.com/kinnector/kinnector-wordpress)** – Integration plugin for protecting WordPress environments.
*   **[kinnector-docker](https://github.com/kinnector/kinnector-docker)** – Compose configuration for running the stack locally.
*   **[kinnector-installer](https://github.com/kinnector/kinnector-installer)** – Setup scripts and packages for Linux deployments.

### General & Shared
*   **[kinnector-docs](https://github.com/kinnector/kinnector-docs)** – Developer and user documentation.
*   **[kinnector-design](https://github.com/kinnector/kinnector-design)** – UI/UX resources, design assets, and architectural blueprints.

## Contributing

We welcome contributions to any part of the project. Please read the [Documentation](https://github.com/kinnector/kinnector-docs) to learn more about our coding guidelines and development workflows.
