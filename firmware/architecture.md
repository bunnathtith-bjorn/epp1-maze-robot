# Firmware architecture

Status: proposal for discussion, not implemented.

## Suggested responsibilities

| Responsibility | Purpose | Status |
| --- | --- | --- |
| Hardware interface | Map documented ports to motor/sensor operations | Not implemented |
| Sensing | Acquire readings and identify invalid measurements | Not implemented |
| Calibration | Derive and store parameters from measured data | Not implemented |
| Motion | Drive, turn, and stop using verified parameters | Not implemented |
| Navigation | Choose maze actions from observations and task rules | Not implemented |
| Application loop | Coordinate sensing, decisions, and motion | Empty sketch only |

## Decisions still needed

- Exact sensors, ports, and libraries.
- Course maze rules and success criteria.
- Navigation strategy and stopping conditions.
- Timing needs and whether any operations may block.
- Calibration method, units, and parameter storage.

Keep related `.h` and `.cpp` files inside the main sketch folder as the application grows. Keep independent test programs in their own sketch folders.
