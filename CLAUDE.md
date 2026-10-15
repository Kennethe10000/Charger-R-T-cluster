# Charger Cluster: project state
Digital instrument cluster for a 2014 Dodge Charger R/T.
Stack: Raspberry Pi, CAN HAT, Python (cantools, FastAPI), HTML canvas UI.

## Current stage
Stage 1: gauge UI on fake data

## Rules
- CAN is listen only. Never send frames to the car.
- Keep the stock cluster stored safely. Do not alter odometer data.
- One screenshot in docs/screenshots/ per significant change.
- Log every session in session_notes.md.
