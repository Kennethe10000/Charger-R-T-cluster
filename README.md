# Charger-R-T-cluster
Custom digital instrument cluster for a 2014 Dodge Charger R/T. Raspberry Pi, CAN bus decoding in Python, and a live gauge UI.

## Progress

### Stage 1: Gauge UI (fake data)
![Stage 1 gauge UI](docs/screenshots/stage1-gauge-ui.png)

### Stage 1b: More gauges (fake data)
Added coolant, oil pressure, battery, fuel, oil life, and tire pressure.

![Stage 1b more gauges](docs/screenshots/stage1b-more-gauges.png)

## Architecture (planned)

```mermaid
flowchart LR
    A[Car CAN bus via OBD port] --> B[CAN HAT, listen only]
    B --> C[Raspberry Pi]
    C --> D[Python decoder, cantools + DBC file]
    D --> E[FastAPI WebSocket server]
    E --> F[Gauge UI on bar LCD]
```