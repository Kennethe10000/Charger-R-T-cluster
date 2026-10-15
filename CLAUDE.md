# Charger Cluster: project state
Digital instrument cluster for a 2014 Dodge Charger R/T.
Stack: Raspberry Pi, CAN HAT, Python (cantools, FastAPI), HTML canvas UI.

## Current stage
Stage 1 complete: gauge UI with fake data (speed, RPM, coolant, oil pressure, battery, fuel, oil life, tire pressure).
Next: FastAPI backend streaming fake data over WebSocket. Waiting on hardware (Raspberry Pi 5, CAN HAT, OBD2 cable) for CAN logging.

## Rules
- CAN is listen only. Never send frames to the car.
- Keep the stock cluster stored safely. Do not alter odometer data.
- One screenshot in docs/screenshots/ per significant change.
- Log every session in session_notes.md.
