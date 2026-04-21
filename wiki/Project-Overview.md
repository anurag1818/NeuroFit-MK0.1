# Project Overview

## Mission

NeuroFit targets continuous personal wellness monitoring by combining physiological sensing, edge inference primitives, and user-facing guidance workflows in a wearable form factor.

## High-Level Objectives

1. Capture biosignals and vital signs from a headband form factor.
2. Stream real-time telemetry over BLE to a web experience.
3. Derive interpretable signal features (EEG band percentages).
4. Detect emergencies and trigger escalation workflows.
5. Support longitudinal trend analysis and mindfulness sessions.

## Scope in Current Repository

| Domain | Implemented | In Progress / Planned |
|---|---|---|
| Embedded firmware | BLE service + characteristics, EEG FFT, battery estimation, fall logic | Sensor driver completion for MAX30102, robust sampling scheduler |
| Web app | Flask routes, auth flow, dashboard templates, emergency API | Production auth hardening, richer analytics API |
| Data persistence | SQLAlchemy models (`User`, `HealthData`) | Historical query implementation and indexing |
| Alerts | Email (Apps Script) + SMS (TextBee) dispatch | Retry policy, observability, secure key storage |
| Meditation | Session UI + audio + simple charting | Biofeedback-driven adaptive session engine |

## Biomedical Context

NeuroFit currently implements *wellness-grade* telemetry logic. It is **not** a certified medical device and must not be used for diagnosis, treatment, or emergency triage decisions without clinical validation.

See [[Safety Considerations|Safety-Considerations]] for detailed guidance.

## Related Pages

- [[System Architecture|System-Architecture]]
- [[Sensor Modules|Sensor-Modules]]
- [[Signal Processing|Signal-Processing]]
- [[Testing and Validation|Testing-and-Validation]]
