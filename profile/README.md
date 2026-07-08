<p align="center">
  <img src="profile/images/kinnector_banner.jpg" alt="**kinnector** Advanced Cyber Security Banner" width="100%">
</p>

# **kinnector**: Open-Source Runtime Security & Telemetry

---

## Why Kinnector exists

The security landscape is changing. Actors target software supply chains (npm, PyPI), exposed web application entrypoints, and developer environments. Attacks are no longer limited to compiled binaries on disk—adversaries execute fileless payloads, abuse container permissions, and hijack browser sessions to harvest credentials.

Traditional antivirus relies on static signatures, failing to stop zero-day exploits or memory-only payloads. Enterprise EDR platforms are closed-source, heavy, and depend on reactive cloud detection that allows payloads to run before containment begins.

Kinnector solves this by providing modular, low-overhead runtime protection. By capturing OS-level events directly via native kernel telemetry (BPF LSM, ETW, EndpointSecurity), Kinnector evaluates behavioral rules in real-time, executing containment actions before a compromise propagates.

---

## The Kinnector Platform

The ecosystem is split into three target environments:

### 💻 Endpoint EDR (Kinnector Desktop)
Protects client workstations and developer environments from client-side threats like browser credential theft, wallet hijackers, and malicious dependencies.
* **Target Subsystems**: [kinnector-core](https://github.com/kinnector/kinnector-core) (telemetry engine) and [kinnector-agent](https://github.com/kinnector/kinnector-agent) (rules engine).
* **Interface**: [kinnector-desktop](https://github.com/kinnector/kinnector-desktop) (Tauri/Svelte dashboard) and [kinnector-cli](https://github.com/kinnector/kinnector-cli) (terminal administration).

### 🛡️ Server EDR (Kinnector Warden)
Protects exposed server workloads, database interfaces, and container fleets from remote code execution (RCE) and container escapes.
* **Target Subsystems**: [kinnector-warden](https://github.com/kinnector/kinnector-warden) (coordinator daemon) and [kinnector-docker](https://github.com/kinnector/kinnector-docker) (instrumented containers and sidecars).

### 🌐 Web Application Shielding (wpwarden)
Protects WordPress environments from SQL injection and parameter exploitation.
* **Target Subsystem**: [kinnector-wordpress](https://github.com/kinnector/kinnector-wordpress) (PHP helper plugin).

---

## Codebase Repositories

### Host Security & Telemetry
* **[kinnector-core](https://github.com/kinnector/kinnector-core)**: Low-level C++ telemetry collector (ETW, eBPF, ESF).
* **[kinnector-agent](https://github.com/kinnector/kinnector-agent)**: Rust EDR daemon for local behavior monitoring and containment.
* **[kinnector-desktop](https://github.com/kinnector/kinnector-desktop)**: Visual Tauri/SvelteKit client dashboard.
* **[kinnector-cli](https://github.com/kinnector/kinnector-cli)**: Command-line utility for local EDR administration.
* **[kinnector-installer](https://github.com/kinnector/kinnector-installer)**: Setup scripts and packages for Linux deployments.
* **[kinnector-jvmti](https://github.com/kinnector/kinnector-jvmti)**: Dynamic JVM class inspection agent.

### Server & Container Workloads
* **[kinnector-warden](https://github.com/kinnector/kinnector-warden)**: Server EDR aggregator and payload validation service.
* **[kinnector-docker](https://github.com/kinnector/kinnector-docker)**: Dockerfiles and sidecar configurations for container environments.
* **[kinnector-collect](https://github.com/kinnector/kinnector-collect)**: Audit-only deployment tools for baseline telemetry gathering.

### Rules & Integration
* **[kinnector-config](https://github.com/kinnector/kinnector-config)**: Rule parsing and cryptographic validation library.
* **[kinnector-protect-community](https://github.com/kinnector/kinnector-protect-community)**: Public repository of rules, exclusions, and allowlists.
* **[kinnector-wordpress](https://github.com/kinnector/kinnector-wordpress)**: Custom query-vetting plugin for WordPress.
* **[kinnector-wild-analysis](https://github.com/kinnector/kinnector-wild-analysis)**: Threat intelligence reports on active in-the-wild campaigns.

---

## Contributing

We welcome contributions to any part of the project. Please read the developer guidelines in [kinnector-docs](https://github.com/kinnector/kinnector-docs) to learn more about our coding standards, schema definitions, and pull request workflows.
