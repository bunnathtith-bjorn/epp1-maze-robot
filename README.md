# EPP1 Maze Robot

NUS CG1111A EPP1 maze robot project using mCore — electronics, firmware, testing, and calibration.

## Project status

Repository scaffold only. The robot is a standard mCore robot. An existing wiring diagram will be uploaded by the team. The sketches in this repository are empty placeholders; maze navigation, motor tests, sensor tests, and calibration are not implemented or verified yet.

## Two main components

- [Electronics](electronics/README.md): calculations, wiring diagrams, KiCad projects, datasheets, summaries, and pictures.
- [Firmware](firmware/README.md): Arduino sketches, proposed architecture, component tests, calibration, and test records.

## Start here

1. Read [the team Git guide](CONTRIBUTING.md).
2. Open `firmware/maze_robot/maze_robot.ino` in Arduino IDE.
3. Fill in the board and library details in [firmware setup](firmware/README.md) before implementing hardware code.
4. Upload the existing wiring diagram to `electronics/wiring/` and complete [the port map](electronics/wiring/port-map.md).

## Team

| Member | Responsibility |
| --- | --- |
| Bjorn | To assign |
| Thant | To assign |
| Tushar | To assign |
| Khanh | To assign |

## Organisation

The `electronics/` and `firmware/` folders always belong to the same repository. Git branches are versions of the whole repository, not separate folders. Keep `main` as the shared reviewed version. Use task branches and pull requests for changes.

## Next tasks

- [ ] Add the team's wiring diagram and confirm the port map.
- [ ] Record the Arduino board/core and library versions.
- [ ] Add existing working firmware, if available.
- [ ] Implement and record motor and sensor tests.
- [ ] Collect calibration data.
- [ ] Implement and test maze navigation.
- [ ] Add all team members as GitHub collaborators.
