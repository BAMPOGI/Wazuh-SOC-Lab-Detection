# Wazuh-SOC-Lab-Detection
Implementation of a SOC Lab using Wazuh SIEM for real-time threat detection and forensic analysis of Windows endpoints.

# SOC Lab: Real-Time Threat Detection with Wazuh SIEM

## Project Overview
This project involves the implementation of a functional Security Operations Center (SOC) Laboratory. The goal was to centralize security telemetry, establish real-time monitoring, and simulate a cyber-attack to validate detection capabilities.

## Technical Stack
* **SIEM:** Wazuh (Manager & Dashboard)
* **OS:** Ubuntu 22.04 LTS (Manager), Windows 11 (Agent)
* **Virtualization:** Oracle VM VirtualBox
* **Networking:** Bridged Adapter Mode

## Project Phases
### Phase 1: SIEM Server Deployment
* Provisioned an Ubuntu server with 3GB RAM and 2 vCPUs.
* Verified `wazuh-manager` service health and dashboard API connectivity.

### Phase 2: Agent Enrollment
* Integrated a Windows 11 host as a monitored endpoint.
* Utilized administrative PowerShell for agent deployment and service initialization.

### Phase 3: Attack Simulation & Forensic Analysis
* Simulated a Brute Force attack (5 failed logon attempts).
* Successfully triggered **Rule ID 60122** for real-time alerting.
* Conducted forensic analysis using **Windows Event ID 4625**.

## Troubleshooting & Key Learnings
* **Resource Optimization:** Managed a Wazuh Indexer service failure caused by memory constraints (3GB RAM) through manual service orchestration and sequencing.
* **Network Connectivity:** Configured bridged networking to enable cross-platform communication between virtualized and physical environments.
