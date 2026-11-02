# Firmware

## Current status

All four sketches are empty starter placeholders. They contain only `setup()` and `loop()`; they do not control motors, read sensors, calculate calibration, or solve a maze. No board build or hardware test has been performed.

## Setup to confirm

| Setting | Value |
| --- | --- |
| Hardware | Standard mCore robot |
| Arduino IDE version | TBD |
| Board selection / FQBN | TBD — confirm from the team's working setup |
| Board package and version | TBD |
| Required libraries and versions | TBD |
| Serial port | Select the connected board on each computer |
| Serial monitor baud rate | TBD when logging is implemented |

## Sketches

- [maze_robot](maze_robot/maze_robot.ino): main application placeholder.
- [motor_test](tests/motor_test/motor_test.ino): independent motor-test placeholder.
- [sensor_test](tests/sensor_test/sensor_test.ino): independent sensor-test placeholder.
- [sensor_calibration](calibration/sensor_calibration/sensor_calibration.ino): calibration placeholder.

Open the desired `.ino` in Arduino IDE. Keep each primary file inside its matching folder. Choose the verified board, install documented dependencies, and Verify before Upload.

Once hardware control is implemented, record actual robot tests in [tests/TEST-LOG.md](tests/TEST-LOG.md).

## Design and data

- [Proposed architecture](architecture.md)
- [Test procedure](tests/README.md)
- [Calibration records](calibration/README.md)
- [Electronics port map](../electronics/wiring/port-map.md)
- [Git upload instructions](../CONTRIBUTING.md)
