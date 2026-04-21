# NeuroFit Wiki

Welcome to the NeuroFit technical wiki. This documentation describes the full wearable stack: embedded firmware, biosignal pipeline, BLE transport, web application, safety constraints, and contributor workflows.

NeuroFit is a wearable mind and health tracker that combines:

- EEG-style biosignal capture (BioAmp EXG input)
- Heart-rate and SpO2 monitoring (planned MAX30102 integration)
- On-device fall/emergency detection (IMU-assisted)
- BLE streaming to a web dashboard
- Alert escalation via email/SMS

## Quick Navigation

### Start Here

- [[Project-Overview|Project Overview]]
- [[System-Architecture|System Architecture]]
- [[Roadmap|Roadmap]]

### Architecture and Engineering

- [[Hardware-Architecture|Hardware Architecture]]
- [[Software-Architecture|Software Architecture]]
- [[Sensor-Modules|Sensor Modules]]
- [[Circuit-Diagram|Circuit Diagram]]
- [[Pinout|Pinout]]
- [[Data-Flow|Data Flow]]
- [[Signal-Processing|Signal Processing]]
- [[BLE-Communication|BLE Communication]]
- [[Power-Management|Power Management]]

### Setup and Operations

- [[Firmware-Installation|Firmware Installation]]
- [[Build-Instructions|Build Instructions]]
- [[Safety-Considerations|Safety Considerations]]
- [[Testing-and-Validation|Testing and Validation]]
- [[Troubleshooting|Troubleshooting]]

### Community and Governance

- [[Contributing|Contributing]]
- [[License|License]]
- [[FAQ|FAQ]]

## Repository-at-a-Glance

| Path | Purpose |
|---|---|
| `Hardware/01-first-firmware/NeuroFit/NeuroFit.ino` | Firmware: BLE, EEG processing, emergency/fall logic |
| `Web (flask)/app.py` | Flask backend, auth, APIs, emergency alert routing |
| `Web (flask)/templates/` | Dashboard, health data, meditation UI pages |
| `Web (flask)/static/js/` | Web Bluetooth, dashboard logic, location, meditation controls |
| `Web (flask)/requirements.txt` | Python package dependencies |
| `Web (flask)/Dockerfile` | Containerized runtime configuration |
| `Docs/` | Additional project documentation assets |

## Current Maturity Summary

- Firmware has real FFT-based EEG band analysis and BLE characteristic writes.
- Frontend and firmware BLE profiles are partially misaligned and require harmonization.
- Some sensor streams are still simulated in software placeholders.
- Security hardening (credentials, password hashing, secrets management) is required before production use.

For implementation gaps and planned upgrades, see [[Roadmap|Roadmap]].
